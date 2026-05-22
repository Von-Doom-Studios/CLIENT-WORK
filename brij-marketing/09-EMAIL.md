# 09 - EMAIL: Brij Marketing

Email capture spec for Dev, ESP recommendation, lifecycle sequence, newsletter plan. Email is the asset we own; followers are rented.

**Owner:** VD-Marketing
**Related files:** [04-ACCOUNTS-AUDIT.md](./04-ACCOUNTS-AUDIT.md), [07-CONTENT-LIBRARY.md](./07-CONTENT-LIBRARY.md), [11-ANALYTICS.md](./11-ANALYTICS.md)
**Last updated:** 2026-05-22

---

## Status

No ESP. No capture forms on brij.fi or travel.brij.fi. Building from zero. Capture in place by end of week 1 is the gate to hitting the 12-month 10,000-email target.

## ESP recommendation

**Pick: Resend + a basic broadcast tool (Loops or Beehiiv).**

Reasoning:
- **Resend** is developer-friendly, has clean React Email primitives, and slots cleanly into the existing brij.fi stack. Best for transactional + lifecycle.
- **Loops** is the cleanest "marketing + transactional in one" option for a dev-tooling brand. Built for SaaS. Solid API. Pair with Resend if Loops alone doesn't cover the broadcast side well.
- **Beehiiv** is the alternative if newsletter is the primary use case and we want a publication-style front end (issue archive, public subscribe page, referrals built in).

If Anthony wants one tool: **Loops** for both lifecycle + newsletter, send transactional through Resend if needed later.
If two tools are fine: **Resend** for transactional/lifecycle + **Beehiiv** for newsletter.

Decision needed from Anthony. Without one, defaulting to Loops in the spec below.

## Capture form spec (brief to VD-Dev)

### Form 1 - brij.fi homepage hero CTA

**Placement:** above-the-fold, after the hero "smart wallet" headline.

**Fields:** email only. No "first name." Single field reduces friction by 30-40% for a list build at this stage.

**Copy:**
> Get early access to Platform APIs and notified when Wallet, On-Ramps, and Service Access ship to the public.

**CTA button:** "Get early access"

**Confirmation behavior:** inline success state ("Thanks. We'll be in touch.") + Loops `subscribed` event fired with `source=site_hero`.

**Source tag:** `site_hero`

### Form 2 - brij.fi mid-page "notify me" per layer

**Placement:** bottom of each product section (Smart Wallet, On-Ramps, Service Access).

**Fields:** email only.

**Copy (varies by section):**
- Smart Wallet: "Notify me when Wallet APIs ship."
- On-Ramps: "Notify me when On-Ramps go live."
- Service Access: "Notify me when Service Access opens to builders."

**CTA button:** "Notify me"

**Source tag:** `site_smartwallet`, `site_onramps`, `site_serviceaccess` (so we can segment which features draw the most interest)

### Form 3 - brij.fi footer

**Placement:** footer.

**Fields:** email only.

**Copy:** "Get the monthly 402 Receipts newsletter."

**CTA button:** "Subscribe"

**Source tag:** `site_footer`

### Form 4 - travel.brij.fi post-booking capture

**Placement:** the booking confirmation response/page. After a successful booking returns.

**Fields:** email only.

**Copy:** "Get notified when more agent-ready services launch on Brij."

**CTA button:** "Notify me"

**Source tag:** `travel_postbooking`

This is the highest-intent surface we have. A user just successfully transacted with an agent over crypto. They convert at 5-8x site-hero baseline.

### Form 5 - travel.brij.fi docs / endpoints

**Placement:** inside the endpoints / "Discovery" section.

**Fields:** email only.

**Copy:** "Get the Platform API early-access list."

**CTA button:** "Get the list"

**Source tag:** `travel_docs`

### Common requirements (all forms)

- All forms POST to the same Loops endpoint with `source` parameter.
- All forms double-opt-in via Loops confirmation email (deliverability and list hygiene).
- All forms respect honeypot field + basic rate-limit (no captcha unless we see abuse).
- All forms log UTM params (`utm_source`, `utm_medium`, `utm_campaign`) alongside the source tag.

### Dev brief format (paste-into-issue)

```
Title: Brij - email capture forms (5 placements)

Spec: brij-marketing/09-EMAIL.md (sections "Capture form spec" and "Common requirements")

Deliverables:
- 5 capture forms across brij.fi (4) and travel.brij.fi (1, plus 1 docs placement = 5 total surfaces, but 5 distinct source tags)
- Loops integration (account setup pending - confirm credentials with marketing)
- Source-tagged event firing
- Inline success state, no page reload
- Confirmation email handled by Loops double-opt-in

Acceptance criteria:
- All 5 forms live, submitting to Loops, source-tagged
- Confirmation email arrives in <60s
- UTM params captured in Loops contact properties

Deadline: end of week 1 (2026-05-31)
Owner: VD-Dev
Related: brij-marketing/04-ACCOUNTS-AUDIT.md, brij-marketing/09-EMAIL.md
```

## Lifecycle sequence

### Email 01 - Welcome

**Trigger:** any new subscriber, regardless of source.

**Send:** immediately (after Loops double-opt-in confirms).

**Copy:** see [07-CONTENT-LIBRARY.md#email-welcome-01](./07-CONTENT-LIBRARY.md).

### Email 02 - The proof (auto-send, day 3)

**Trigger:** 72 hours after welcome.

**Subject:** "Watch an agent book a flight"

**Body (draft):**

> The fastest way to understand what Brij does is to watch an agent do it.
>
> [30-second flight booking demo - YouTube link, embedded video, or animated GIF if email-safe]
>
> No IATA accreditation. No merchant onboarding. Three HTTP calls.
>
> If you want to try it yourself, the docs are at travel.brij.fi.
>
> If you want to talk to us about your own use case, just reply.
>
> Brij

### Email 03 - Feature deep-dive (auto-send, day 10)

**Trigger:** 7 days after Email 02.

**Subject:** "402 Payment Required is the new API key"

**Body (draft):**

> The HTTP 402 status code sat dormant for 25 years. Then x402 turned it into the cleanest payment primitive on the internet.
>
> Here's what Brij's three layers look like in practice:
>
> Smart Wallet: your agent has its own checking account. Daily limits, policies, signing keys. agent-001.wallet.
>
> On-Ramps: fiat in, USDC out, best rate routed automatically. 2.1s settlement.
>
> Service Access: pay-per-call to any API. No subscriptions. No API keys.
>
> If you're building agents and any of this would save you a month of integration work, reply and tell us what you're shipping.
>
> Brij

### Email 04 - Ask (auto-send, day 21)

**Trigger:** 11 days after Email 03.

**Subject:** "What are you building?"

**Body (short, reply-bait):**

> One question while you're on the list:
>
> What are you building, and what's the biggest payment-related blocker you've hit?
>
> Reply with one sentence. We read every one. The product roadmap moves based on these answers.
>
> Brij

### Email 05+ - Newsletter (recurring)

Monthly broadcast. Format and template in [07-CONTENT-LIBRARY.md#nl-01](./07-CONTENT-LIBRARY.md).

## Segmentation

Loops contact properties:
- `source` - which form/CTA captured them
- `utm_source`, `utm_medium`, `utm_campaign`
- `referrer_url`
- `signup_date`
- `booked_on_travel` - boolean, true if also a travel.brij.fi booker
- `replied_to_lifecycle` - boolean, set true on any inbound reply

Lists/segments to maintain:
- All subscribers (newsletter default)
- High-intent: source ∈ {travel_postbooking, travel_docs, site_serviceaccess}
- Builders: anyone who replied to the lifecycle "what are you building" email
- Cold (no opens in 60 days): re-engagement candidate at month 3

## Off-site capture

- **Social posts that drive traffic** point to brij.fi with `utm_source=x` (or `linkedin`, etc.) so we can segment by channel.
- **YouTube descriptions, podcast show notes** all link to brij.fi with `utm_source=youtube` / `utm_source=podcast`.
- **Partner co-marketing newsletter swaps** use a dedicated `?utm_source=partner_[name]` per swap.
- **Conference / event** QR codes point to a campaign-specific landing page once activated.

## Newsletter plan

**Name (working title):** 402 Receipts

**Cadence:** monthly until we have weekly-worthy content (~6 months minimum).

**Format:**
1. Lead: what shipped on Brij this month
2. Five things in agent payments worth knowing
3. Build of the month (one builder spotlight)
4. What we're working on next
5. Close (links to brij.fi, X follow, reply invitation)

**Production:**
- Drafted on the 25th of each prior month
- Sent first Wednesday of each month
- Both audiences (all subscribers + builders segment) get it; high-intent gets a small bonus paragraph or earlier delivery

**Subscriber growth path:**
- Month 1: ~100 from site capture + Espresso conversion
- Month 3: ~500 subscribers triggers first formal newsletter launch announcement (campaign 04 in [06-CAMPAIGNS.md](./06-CAMPAIGNS.md))
- Month 12: target 10,000

## Off-channel email (outbound)

- **Targeted developer outreach** when a builder hits an agent-payment wall publicly: founder reply on X + Ops follow-up DM with a doc link. Marketing flags the moment. Ops executes. Not automation.
- **Partner co-marketing list swaps** with Coinbase x402 devrel, Solana ecosystem newsletters, agent framework newsletters. Marketing identifies fit. Ops executes outreach.
- **No bought lists. No generic cold blasts.** Off-brand, off-thesis, illegal in some jurisdictions, ineffective for this audience.

## Open items for Anthony

1. Approve ESP pick (Loops, vs Resend+Beehiiv, vs other).
2. Confirm budget allocation for ESP (lives in [03-BUDGET.md](./03-BUDGET.md)).
3. Confirm any recoverable Espresso Cash email list - if yes, that's the import seed for week 1.
4. Approve lifecycle sequence copy above.
