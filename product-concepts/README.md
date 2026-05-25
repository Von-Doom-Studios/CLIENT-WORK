# Product Concepts Pipeline

A repeatable, agent-driven pipeline for taking a product idea from reference images to factory-ready mechanical files.

---

## Overview

This pipeline is designed to produce physical product prototypes (starting with eyeglass frames) using AI-assisted 3D generation, automated mesh cleanup, and CAD-to-manufacturing file conversion — with minimal human intervention.

**Stack:**
- [Meshy API](https://www.meshy.ai/api) — AI image/text to 3D mesh
- Blender (headless Python `bpy`) — mesh cleanup + scaling
- FreeCAD (headless Python) — mesh → STEP export
- 3D printing service (e.g. JLCPCB, Craftcloud) — prototype validation
- Shenzhen factory — production

---

## Pipeline

```
Reference image/artwork + measurements
            ↓
   [STEP 1] Meshy API → rough 3D mesh (STL)
            ↓
   [STEP 2] Blender (headless) → mesh cleanup + scale to real dimensions
            ↓
   [STEP 3] FreeCAD (headless) → mesh → solid → .STEP export
            ↓
   [STEP 4] Auto-generate spec sheet (PDF/markdown)
            ↓
   [STEP 5] 3D print order → prototype review
            ↓
   [STEP 6] Factory handoff package (Shenzhen)
```

---

## Detailed Step-by-Step

### Step 1 — Meshy API: Image/Text to 3D Mesh

**Goal:** Generate a rough 3D mesh from a reference image or text description.

**Inputs:**
- Reference image (JPG/PNG) — front/side/3/4 view preferred
- OR text prompt describing the frame style, shape, and details
- Style notes (e.g. "rectangular, thin metal frame, flat temples, keyhole bridge")

**Process:**
1. Call `POST /openapi/v1/image-to-3d` with the reference image URL
2. Set `symmetry_mode: "on"` — eyewear is symmetrical
3. Set `should_remesh: false` — preserve highest precision mesh
4. Set `target_formats: ["stl", "obj"]`
5. Poll task status until complete
6. Download STL output

**Automation:** Full API — agent-driven, no UI needed.

**Output:** `frame_raw.stl`

---

### Step 2 — Blender: Mesh Cleanup + Scale

**Goal:** Clean the raw mesh and scale it to real-world dimensions.

**Inputs:**
- `frame_raw.stl`
- Measurement spec (see `specs/measurements-template.md`):
  - Lens width (mm)
  - Bridge width (mm)
  - Temple length (mm)
  - Frame height (mm)
  - Lens-to-lens total width (mm)

**Process (headless Blender Python script):**
1. Import STL into Blender (`bpy.ops.import_mesh.stl`)
2. Apply symmetry mirror modifier along X axis
3. Remove duplicate vertices, fix non-manifold edges
4. Scale mesh to match real-world measurements using reference dimension
5. Apply all modifiers
6. Export cleaned mesh as `frame_clean.stl` and `frame_clean.obj`

**Script:** `scripts/01_blender_cleanup.py`

**Output:** `frame_clean.stl`, `frame_clean.obj`

---

### Step 3 — FreeCAD: Mesh → Solid → STEP Export

**Goal:** Convert cleaned mesh to a CAD solid and export factory-ready `.STEP`.

**Inputs:** `frame_clean.stl`

**Process (headless FreeCAD Python script):**
1. Import mesh via `Mesh.insert()`
2. Run mesh-to-shape conversion (`Part.Shape.makeShapeFromMesh()`)
3. Attempt solid from shell (`Part.makeSolid()`)
4. Validate solid geometry (check for open faces)
5. Export as `frame.step` via `Part.export()`

**Script:** `scripts/02_freecad_to_step.py`

**⚠️ Quality note:** Mesh-to-STEP conversion quality depends on mesh cleanliness. Hinges and screw points should be reviewed before final factory submission.

**Output:** `frame.step`

---

### Step 4 — Spec Sheet Generation

**Goal:** Auto-generate a human-readable spec document to accompany the files.

**Inputs:**
- Measurement values
- Material selection (acetate / metal / TR90)
- Hinge type (standard / spring / hingeless)
- Color/finish notes

**Process:**
- Script fills `templates/spec-sheet-template.md` with values
- Renders to PDF (via `pandoc` or similar)

**Script:** `scripts/03_generate_spec_sheet.py`

**Output:** `[product-name]-spec-sheet.pdf`

---

### Step 5 — 3D Print Order (Prototype Validation)

**Goal:** Physical prototype before factory submission.

**Recommended services:**
- [JLCPCB](https://jlcpcb.com/3d-printing) — fast turnaround, low cost
- [Craftcloud](https://craftcloud3d.com) — price comparison across print services
- Local SLA resin print shop — highest detail for eyewear

**Material:** SLA resin (best surface detail for frame geometry)

**Checklist before ordering:**
- [ ] Frame dimensions match spec sheet
- [ ] Symmetry verified
- [ ] Hinge cutouts present (even if simplified)
- [ ] No non-manifold edges (run mesh check in Blender)

---

### Step 6 — Factory Handoff Package (Shenzhen)

**Goal:** Ship a complete, factory-ready package.

**Package contents:**
```
factory-package/
├── frame.step            ← Primary CAD file
├── frame_clean.stl       ← Backup mesh reference
├── spec-sheet.pdf        ← Measurements + materials + tolerances
├── reference-images/     ← Original inspiration images
└── notes.md              ← Any special instructions
```

**Factory communication checklist:**
- [ ] Confirm material availability (acetate / metal alloy / TR90)
- [ ] Confirm hinge type + supplier
- [ ] Request single prototype before production run
- [ ] Agree on revision cycle (typically 1-2 rounds)

---

## Measurements Template

See `specs/measurements-template.md` for the standard input format.

Standard sizing reference (adult frames):
| Measurement | Typical Range |
|---|---|
| Lens width | 46–58mm |
| Bridge width | 14–22mm |
| Temple length | 135–150mm |
| Frame height | 28–50mm |

---

## File Structure

```
product-concepts/
├── README.md
├── specs/
│   └── measurements-template.md
├── scripts/
│   ├── 01_blender_cleanup.py
│   ├── 02_freecad_to_step.py
│   └── 03_generate_spec_sheet.py
├── templates/
│   └── spec-sheet-template.md
├── products/
│   └── [product-name]/
│       ├── reference-images/
│       ├── meshes/
│       ├── cad/
│       └── factory-package/
└── docs/
    └── pipeline.md
```

---

## Requirements

```bash
# Meshy API
pip install requests

# Blender (headless)
brew install blender   # or download from blender.org

# FreeCAD (headless)
brew install freecad   # or download from freecad.org

# Spec sheet rendering
brew install pandoc
```

**Meshy API key:** Set as env var `MESHY_API_KEY`

---

## Status

- [x] Pipeline designed
- [ ] Blender cleanup script
- [ ] FreeCAD STEP export script
- [ ] Meshy API integration script
- [ ] Spec sheet template
- [ ] End-to-end test with eyeglass frame reference

**First test:** Eyeglass frames — targeting a rectangular thin-metal style
