# 08 - NEWSLETTER

402 Receipts. Long-form companion to X. Every issue ties to a campaign in [05-CAMPAIGNS.md](./05-CAMPAIGNS.md) and links back to the X posts.

**Owner:** VD-Marketing
**Last updated:** 2026-06-02

---

## Cadence

Monthly. First Wednesday, AM.

Issue 01 ships 2026-06-24, gated on email list ≥500. If short, the slot becomes a teaser and Issue 01 moves to the next first-Wednesday after the threshold.

## Integration rule

- Every campaign declares a Newsletter tie-in field in [05-CAMPAIGNS.md](./05-CAMPAIGNS.md).
- Every newsletter issue ties to ≥1 campaign. Sections that don't tie to a campaign are cut.
- Issue copy links back to the X posts (URLs swapped in after posting) and to @brij_fi.

## Issue sections (minimum)

1. **What shipped on Brij this month** (200-400 words) - long-form of the month's product X post(s).
2. **Five things in agent payments worth knowing** - five short items with source links.
3. **Build of the month** - one builder using x402, Solana agent payments, or Brij. Their X handle linked.
4. **What we're working on next** - 2-4 lines on the next campaign.
5. **Social close** - follow @brij_fi, try brij.fi / travel.brij.fi, reply with what you're building.

## Subject line + sender

- Subject leads with the payload, not "Issue N." 6-9 words. No emoji.
- From: Brij. Reply-to: `hello@brij.fi` (confirm with `[client]`).

## ESP

Defaulting to Loops pending `[client]` decision. Resend + Beehiiv is the alternative if the newsletter is run as a public publication with an archive. Capture form spec for Dev lives separately in a Dev-handoff doc (TBD).

---

## Issue 01 - 2026-06-24

**Ties to:** Campaign 01 (Grok MCP launch + flight contest), Campaign 02 (Smart wallet), Campaign 04 (Newsletter launch + bounty + free flight).
**Subject:** "Book a flight in Grok. Win one too."
**Send:** 2026-06-24 Wed, AM.
**Status:** DRAFT (gated on subs ≥500).

### What shipped this month

The Brij MCP is live in Grok. Open Grok, connect the MCP, search for a flight, book it. Under a minute, no browser, no airline trackers watching your search and raising the price. The X version of this launch: `[link to post-w1-x-2]`. The proof on why that matters: `[link to post-w1-x-3]` and `[link to post-w1-x-4]`.

Alongside the launch we ran a four-week contest: record yourself booking a flight in Grok with the Brij MCP, post the video, and the most-retweeted entry of the week wins $200 toward their next flight. Four weeks, four winners. The X version: `[link to post-w1-x-1]`.

Under travel sits the rest of Brij: a wallet built for software, not humans with thumbs. It pays per API call instead of per subscription. It enforces a rule you wrote before every transaction. It lets an AI spend on your behalf, with limits you set. It funds and exits through a real bank account. The X version: `[link to post-w2-x-3]`.

We chose travel as the wedge because it's one of the hardest payment problems we could pick: regulated industry, live inventory, refunds, real consequences when something breaks. If our wallet can clear travel, it can clear most of what an agent will need to buy next. The X version: `[link to post-w2-x-4]`.

### Five things in agent payments worth knowing

1. _[x402 ecosystem update with source]_
2. _[Solana agent infrastructure update with source]_
3. _[Framework news - LangChain / CrewAI / Mastra / Vercel AI SDK / Letta / Eliza, with source]_
4. _[Payment standards update with source]_
5. _[One builder worth watching - X handle linked, candidate from [07-ENGAGEMENT.md](./07-ENGAGEMENT.md) Tier 3]_

(Filled in from live reading the week of send. Each item 2-4 sentences with a source link.)

### Build of the month

_[Builder spotlight. Name, what they shipped, X handle. Bridge to @brij_fi if they're already on our Tier 2 or 3 engagement list.]_

### What we're working on next

Builder bounty: $500 USDC for the best demo of an agent paying for something real with a Brij wallet. Rules and submission window: `[link to post-w4-x-1]`.

Free flight: first 10 bookings on travel.brij.fi this month, we refund. `[link to post-w4-x-3]`.

After that, Service Access opens to external builders. If you're shipping agents and you've hit the paywall wall, reply to this email.

### Social close

- Follow @brij_fi on X: https://x.com/brij_fi
- Try the product: brij.fi and travel.brij.fi
- Reply with what you're building. We read every one.

---

## Open items

1. Approve ESP (Loops vs Resend + Beehiiv vs other).
2. Confirm ESP budget in [03-BUDGET.md](./03-BUDGET.md).
3. Confirm Issue 01 subscriber gate (≥500) or override.
4. Confirm Issue 01 subject line.
