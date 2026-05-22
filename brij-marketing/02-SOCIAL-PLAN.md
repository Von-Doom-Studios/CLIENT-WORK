# 02 — SOCIAL MEDIA PLAN

> Companion to `01-THESIS.md`. If anything below contradicts the thesis, the thesis wins.

## Goal (12 months)

- **5,000 social followers** (X primary, LinkedIn secondary, YouTube long-tail)
- **10,000 email signups** on brij.fi

These are the same numbers from the thesis, just stated as the marketing target. The 90-day checkpoints in the thesis still hold: 1,000 emails / 500 X followers by Aug 21, or we re-cut.

## Audience (who we are actually posting for)

Ranked by priority. Every post should serve at least one.

1. **Agent / AI infrastructure builders.** People shipping with LangChain, CrewAI, Mastra, Vercel AI SDK, Letta, Eliza, etc. They hit payment walls. We solve that. Primary buyer of Platform APIs.
2. **x402 / Solana devrel + ecosystem.** Coinbase devrel, Solana Foundation, Helius, Jupiter, Phantom, Magic Eden infra people. Influence amplifiers, not customers. Earned reposts here are worth 10x algorithmic reach.
3. **Crypto-native builders looking for "it actually works" stories.** Bankless / The Rollup / Lightspeed audiences. They share. They drive earned media.
4. **Curious operators and founders outside crypto.** People who hear "agent books a flight with crypto" and want to see it. Lower priority but they convert to emails well because the demo is the hook.

We are **not** posting for retail crypto, memecoin traders, or general AI consumers. If a post would resonate with those audiences, it's probably off-thesis.

## Channels and roles

- **X (@brij or final handle) — primary.** Where the agent / crypto / x402 conversation actually happens. 80% of effort here.
- **LinkedIn — secondary.** Founder POV, hiring, partnership signal, longer "why this matters" pieces. Lower frequency but higher trust signal for enterprise inquiries.
- **YouTube — long-tail / SEO.** Podcast plus demo videos. Discovery and proof, not weekly posting.
- **Farcaster — opportunistic.** If we have bandwidth, cross-post the best X content. Audience overlaps heavily with our buyer. Do not commit to a cadence yet.
- **TikTok / IG — explicitly out for now.** Wrong audience for this thesis. Revisit only if a piece organically breaks out.

## Cadence

Founder-posted manually. 2-3 posts per week per channel to start. No automation until we have proof the content is working (4-6 weeks minimum).

**Per week, baseline:**
- X: 3 posts + active replies daily (replies are the real growth lever, see below)
- LinkedIn: 1 post (founder voice, longer-form)
- YouTube: not weekly. 1 podcast episode every 2-3 weeks once launched.

If founders can only sustain one channel, prioritize X.

## Content pillars (the 4 things we ever post about)

Every post fits into one of these. If it doesn't, don't post it.

**Pillar 1 — Product receipts (40%).**
The thing that just shipped, just worked, or just got measurably better. Booking confirmations, throughput numbers, latency screenshots, new endpoints, demo clips. "Receipts, not takes" from the thesis.

Examples:
- "Agent just booked SFO→LIS in 2.1s. $0.10 search, $0.10 intent, $487 escrow. No IATA, no contract."
- "x402 endpoint hit count this week: [number]. Top caller: [framework]."
- Screen recording of a 30-second flight booking from prompt to PNR.

**Pillar 2 — Features and capability posts (25%).**
The three layers from brij.fi: Smart Wallet, On-Ramps, Service Access. Each gets a recurring drumbeat. Not "here's a feature" marketing - "here's what this unlocks" framing.

Examples:
- Smart Wallet: "Daily limits, policy enforcement, agent-001.wallet style addresses. Your agent has its own checking account."
- On-Ramps: "Fiat in, USDC out, best rate routed automatically. 2.1s settlement."
- Service Access: "402 Payment Required is the new API key. Here's why."

**Pillar 3 — Ecosystem engagement (25%).**
Where the growth actually comes from. Replies to and quote-posts of: Coinbase devrel (x402), Solana Foundation, agent framework accounts, crypto infra accounts, builders showing off agent projects.

Not "great post!" replies. Real value: a code snippet, a counter-example, an extension of their point with our infra as the proof. Engagement farming is fine; empty engagement farming is off-brand.

Specific targets to engage with weekly (build this list out in `03-ENGAGEMENT-MAP.md`):
- @CoinbaseDev, x402 protocol accounts
- @solana, @SolanaFndn, major Solana infra (@helius_labs, @jup_dotag, etc.)
- @LangChainAI, @crewAIInc, @vercel (AI SDK), @letta_ai, @ai16zdao / Eliza
- Builder accounts shipping in the agent-payments space
- Notable crypto media and analysts who cover infra (not price)

**Pillar 4 — POV and contrarian takes (10%).**
The "we believe agents need money like websites needed HTTPS" thesis, expressed in new ways. Used sparingly. Only when we have a sharp claim to make. No 8-tweet threads about "the future of agents." Short, opinionated, defensible.

## The 2-3 posts per week template

A typical week looks like:

- **Post 1 — Product receipt.** Something that worked this week. Screenshot or short clip.
- **Post 2 — Feature drumbeat.** One of the three layers, in plain language.
- **Post 3 (optional) — POV or ecosystem quote-post.** Where we plant a flag or build on someone else's signal.

Replies and quote-posts are separate from the 3 posts and happen daily. Founders should be replying in-thread on relevant conversations for 15-20 minutes a day. This is the real growth engine for a small account in a small space.

## Voice (how this all sounds)

From the thesis: "Builders trust receipts, not takes."

- Short. Confident. Dry.
- Code, numbers, screenshots over adjectives.
- Lowercase posts are fine when the content has weight.
- No emojis as decoration. Sparingly for emphasis only.
- Never "excited to announce." Never "thrilled." Never "🚀."
- Engineering blog tone, not crypto Twitter tone.

We are the team that shipped before we talked. The voice should sound like that.

## Workflow (who does what)

1. **Social agent (this agent) — drafts copy.** Writes posts against the pillars and current product state. Drafts go to a `drafts/` folder in this repo by week.
2. **Creative agent (VD-Creative) — designs visuals where needed.** Static images, short clips, demo recordings. Brief includes platform, dimensions, copy overlays, references, deadline.
3. **Founders — review and post manually.** Edit voice if needed, post to X / LinkedIn / etc. on schedule.
4. **Weekly retro (15 min).** What hit, what flopped, what's the next week's draft list. Logged in `weekly-retros/`.

Automation only after 4-6 weeks of manual posts that show what's working. Premature automation kills voice.

## YouTube / podcast plan

Goal: a low-frequency, high-quality "what's actually shipping in agent payments / x402 / agent infra" show. Doubles as a vehicle to feature our own products without it feeling promotional.

- **Format:** 20-30 min episodes. Conversational. Founder + one guest from the ecosystem (a builder, a protocol team, a researcher).
- **Cadence:** 1 episode every 2-3 weeks once launched. Do not start until episode 1 is fully produced. Empty channels hurt more than no channel.
- **Distribution:** YouTube primary, audio cut to Spotify / Apple, 60-90 second clips repurposed for X and LinkedIn. Clips do most of the work.
- **Topics:** what just shipped in x402, agent framework news, "first time an agent did X" stories, occasional deep dives on our own products (when there's news, not on a schedule).
- **Production:** scoped in a separate brief to VD-Creative once we lock the format. Do not start production until thesis answer #2 (founder voice) is settled - the show is a founder vehicle.

Naming and channel setup is a separate decision. Defaulting to "BRIJ" or "The Agent Layer" until we pick.

## Email capture plan

Goal: 10,000 emails in 12 months. Email is the asset we own; followers are rented.

**On brij.fi:**
- Primary hero CTA: a single email field above the fold. Current site implies a wallet/agent feel - the CTA should match. Suggestion: "Get early access to Platform APIs" or "Get notified when Wallet / On-Ramp ships."
- Secondary CTA at the bottom of each product section (Smart Wallet, On-Ramps, Service Access) - "Notify me when this is live."
- Exit-intent or scroll-depth modal on desktop. Light. Not aggressive.

**On travel.brij.fi:**
- Already a working demo. After a successful (or attempted) booking, an email field: "Get notified when more agent-ready services launch on BRIJ."
- A second email field on the docs / endpoints section: "Get the Platform API early-access list."

Both of these are briefs for VD-Dev. Marketing writes the copy and CTA spec, Dev implements. We do not build sites.

**Off-site capture:**
- Every social post that drives traffic points to a single landing page with the email field. Not the homepage if the homepage doesn't convert well - we'll test.
- YouTube video descriptions, podcast show notes, GitHub README all link to the same capture page with UTM tags.
- Conference / event presence (when applicable) - QR code to the same page.

**Newsletter (the outbound side):**
- Once we have ~500 subscribers, start a monthly builder-facing newsletter. Working title: "402 Receipts" or similar.
- Content: what shipped this month on BRIJ, 3-5 notable things happening in agent-payments / x402 / Solana infra, one builder spotlight, one piece of code or pattern worth knowing.
- Format: short. Skimmable. Plain text feel. Substack or Beehiiv depending on Dev preference - this is a Dev call once we're ready.
- Cadence: monthly until we have something worth saying weekly. Do not commit to weekly upfront.

**Other email channels:**
- Targeted developer outreach: when a builder publicly hits an agent-payment wall on X, a founder reply + a follow-up DM with a relevant doc link converts well. This is Ops territory, not marketing automation.
- Partner co-marketing: cross-list with Coinbase x402 devrel, Solana ecosystem newsletters, agent framework newsletters when we have a story worth telling. Ops handles outreach.
- Do NOT buy lists. Do NOT do generic cold email blasts. Off-brand, off-thesis, and doesn't work for this audience.

## Measurement

Tracked weekly. Reported to Anthony in a single block, no fluff.

- Followers per channel (delta vs. prior week)
- Email signups total + delta
- Top-performing post (impressions / replies / clicks)
- Worst-performing post (so we learn)
- Notable engagements (quote-posts from ecosystem accounts, founder DMs from builders)
- Bookings on travel.brij.fi (proxy for actual product traction)

The 90-day checkpoint from the thesis is the hard gate: if we're under 250 emails or under 10 bookings by Aug 21, we re-cut.

## Assumptions I'm making (correct any of these in one pass)

1. **Handle.** Plan assumes @brij or similar X account is the primary handle. Thesis question #1 still open.
2. **Founder voice.** Plan assumes Anthony's personal X is at least partially active and on-thesis. If it's not, social ceiling is lower. Thesis question #2.
3. **Token.** Plan assumes no token narrative for 90 days. Thesis question #3.
4. **Travel capacity.** Plan assumes travel.brij.fi can handle moderate spikes (a viral post sends ~hundreds of visitors). Thesis question #4.
5. **"First" claim.** Plan does not lean on a "world's first" claim until thesis question #5 is answered. Until then, frame as "one of the first" or just show the product.
6. **Email stack.** Plan assumes Dev picks the email capture + newsletter platform (Resend / Beehiiv / Substack / similar). Marketing doesn't pick infra.
7. **Solo or co-founder posting.** Plan assumes 1-2 people doing manual posting. If it's a team of 5+, cadence can scale up.

## What I need from you next

Answer the 5 open questions in `01-THESIS.md` and any of the 7 assumptions above where I got it wrong. Then I'll write `03-ENGAGEMENT-MAP.md` (specific accounts to engage with, week-by-week) and `04-FIRST-30-DAYS.md` (concrete post list for the first month).
