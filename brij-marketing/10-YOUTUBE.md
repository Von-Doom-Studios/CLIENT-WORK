# 10 - YOUTUBE: Brij Marketing

YouTube strategy across multiple formats. The channel is not just the podcast - it's also where demos, founder talks, x402 explainers, and build-in-public videos live. Each format runs as its own track.

**Owner:** VD-Marketing
**Related files:** [02-STRATEGY.md](./02-STRATEGY.md), [04-ACCOUNTS-AUDIT.md](./04-ACCOUNTS-AUDIT.md), [06-CAMPAIGNS.md](./06-CAMPAIGNS.md)
**Last updated:** 2026-05-22

---

## Why YouTube matters for Brij

- **Discovery surface.** YouTube is search. "How do AI agents pay for things" returns nothing useful today. We can own it.
- **Proof asset.** A 30-second clip of an agent booking a flight is the single most thumb-stopping content we will ever produce.
- **Long-tail compounds.** A good explainer can drive emails for 12+ months. Twitter posts vanish in 24 hours.
- **Builder trust.** Devs use YouTube to evaluate technical claims. Going there means showing the work.

## Formats (each is its own track)

### Format 1 - Product demos (highest priority)

**What:** short (30s-3min), high-polish recordings showing the product doing something real. No talking head needed. Captions + screen capture + sometimes a voiceover.

**Frequency:** 1-2 per month minimum. Every meaningful product update gets a demo.

**Roster of demos to produce:**
- The 30-second flight booking (campaign 02, week 4 in [06-CAMPAIGNS.md](./06-CAMPAIGNS.md))
- Agent funding itself via on-ramp (60s)
- x402 endpoint call - the smallest possible "this is what 402 looks like" (45s)
- Smart wallet daily limit enforcement (30s, shows a denied tx)
- Refund flow on price mismatch (45s)

**Creative brief format:** delivered to VD-Creative per demo. Includes screen capture source (founder records or marketing instruments), captions copy, background music if any, brand intro/outro card.

### Format 2 - Founder talks (medium priority)

**What:** 5-10 minute talking-head videos. Founder on camera explaining one specific thing. "Why we shipped travel before wallet." "What x402 actually is." "Where the agent-payments problem comes from."

**Frequency:** 1 per month.

**Roster of first few:**
- "Why Brij" - founder origin / why we converted Espresso (8 min)
- "What x402 is, in 10 minutes" - founder explains the protocol simply
- "Why agents need their own wallets" - the thesis

**Production:** founder records on phone or webcam, Creative edits with chapters, lower-thirds, b-roll of the product UI.

### Format 3 - x402 / agent-payment explainers (medium priority)

**What:** 3-7 minute educational videos. Whiteboard or screen-share style. Aimed at builders who want to understand the protocol layer.

**Frequency:** every 6-8 weeks.

**Roster of first few:**
- "What HTTP 402 actually does"
- "Solana escrow PDAs for agent payments"
- "Pay-per-call APIs vs API keys vs subscriptions"

**Production:** voiceover + screen-share or animated diagrams. Creative produces visuals. VD-Marketing scripts.

### Format 4 - Build-in-public videos (low frequency, high authenticity)

**What:** 5-15 minute behind-the-scenes. "How we shipped X this week." Loom-style. Lower polish, higher trust.

**Frequency:** monthly when there's something real to show.

**Production:** founder records on Loom or QuickTime, Creative does a light edit + brand bumper.

### Format 5 - Podcast (lower priority, opportunistic)

**What:** 20-30 minute conversational episodes. Founder + one guest from the agent / x402 / Solana ecosystem.

**Frequency:** 1 every 2-3 weeks once launched. Do NOT launch until the first 3 guests are confirmed and episode 1 is fully produced. Empty channels hurt more than no channel.

**Working title:** TBD. Candidates: "402 Receipts" (matches newsletter), "Agents That Transact," "The Payments Layer." Final pick lives in this file once decided.

**Roster of first guests (placeholders for Ops outreach):**
- Someone from Coinbase x402 devrel
- A builder shipping an x402 product (non-competing)
- Someone from a major agent framework (LangChain / CrewAI / Vercel AI)
- A Solana ecosystem voice on agent infra

**Distribution:**
- YouTube primary (full video)
- Audio cut to Spotify + Apple Podcasts (use Transistor or Riverside)
- 60-90 second clips repurposed for X and LinkedIn (this is where most of the reach comes from)
- Show notes linked in newsletter

**Production:** Riverside or similar for recording. Light edit. Single cover-art template for all episodes (Creative produces).

## Channel setup checklist (week 1-2 work)

- [ ] Create channel under brij.fi domain ownership
- [ ] Handle: @brij or @brij_fi (whichever is available)
- [ ] Avatar: same as X profile image (Creative brief in [04-ACCOUNTS-AUDIT.md](./04-ACCOUNTS-AUDIT.md))
- [ ] Banner: 2560x1440, brand layout (Creative brief in 04)
- [ ] Channel description (drafted in [07-CONTENT-LIBRARY.md](./07-CONTENT-LIBRARY.md))
- [ ] Channel trailer: the 30-second flight booking demo, set as featured for non-subscribers
- [ ] First upload: same demo, with full long-form description, timestamps, brij.fi link
- [ ] Playlists created (placeholder, populated as content arrives): Demos, Founder Talks, x402 Explainers, Build-in-Public, Podcast

## Description and SEO standards

Every upload follows the same description template:

```
[1-2 sentence what this video shows]

What is Brij?
Brij is the payments layer for AI agents on Solana. Smart wallet + on-ramps + pay-per-call APIs over the x402 protocol.

Try it:
brij.fi
travel.brij.fi

[Timestamps if long-form]

Follow:
X: https://x.com/brij_fi
LinkedIn: [link]
Newsletter: brij.fi

#agents #x402 #solana #usdc #cryptopayments [other relevant tags per video]
```

Title pattern: `[Action verb] - [Object] - [60-char hook]`
Example: `Watch an AI agent book a real flight with USDC over x402`

## Measurement

For YouTube specifically, tracked in [11-ANALYTICS.md](./11-ANALYTICS.md):
- Views per video (7-day and 30-day)
- Watch time / avg view duration
- Subscribers gained per upload
- Click-through to brij.fi (via UTM)
- Emails captured from YouTube-sourced traffic (Loops `utm_source=youtube`)

## Open items for Anthony

1. Confirm YouTube channel handle preference.
2. Confirm founder is on-camera comfortable for Format 2 and Format 5 (talking-head and podcast).
3. Pick podcast working title from candidates above (or propose alternative).
4. Confirm budget allocation for production tooling (Riverside, editing) - lives in [03-BUDGET.md](./03-BUDGET.md).
5. Seed list: 5 people you'd want as podcast guests in the first 90 days.
