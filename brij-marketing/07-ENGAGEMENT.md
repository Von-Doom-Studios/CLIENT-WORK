# 07 - ENGAGEMENT

X accounts to engage with weekly. Also the input contract for the external X-watcher agent.

**Owner:** VD-Marketing
**Last updated:** 2026-05-26

---

## Rules

1. Replies add value: a code snippet, a counter-example, a sharp extension. No empty "great post!"
2. 15-20 min/day on X. Daily ritual against the X-watcher queue.
3. Quote-post when there's a sharp extension. Reply in-thread otherwise.
4. No DMs. Outreach is Ops.

## Tier 1 - Ecosystem amplifiers

One repost here is worth 50 generic likes.

| Handle | Why | What to reply with |
|---|---|---|
| @CoinbaseDev | x402 protocol team. Top amplifier. | x402 edge cases, performance numbers, builder feedback. |
| @solana | Top of the Solana funnel. | Settlement times, USDC flow numbers, escrow patterns. |
| @SolanaFndn | Foundation. | Tie our shipping to broader Solana narratives. |
| @helius_labs | Solana infra. | How we use their RPC, edge cases. |
| @JupiterExchange | DeFi infra on Solana. | On-ramp routing, best-rate angles. |
| @phantom | Wallet UX leader. | Agent UX and programmatic wallet POVs. |
| @superteam | Solana builder community. | Hackathon angles, builder spotlights. |

## Tier 2 - Agent frameworks (primary buyer audience)

| Handle | Why | What to reply with |
|---|---|---|
| @LangChainAI | Largest agent framework. | Code-level: how Brij + x402 plugs into LangChain. |
| @crewAIInc | Multi-agent. | Payment primitives for multi-agent systems. |
| @vercel | AI SDK heavy use. | "Here's the payment piece you didn't have." |
| @letta_ai | Stateful agents. | Stateful agent + persistent wallet pairing. |
| @ai16zdao | Eliza framework. | Eliza plugin angle. |
| @mastra_ai | Active devrel. | Direct integration in public. |
| @pyautogen | Microsoft framework. | Enterprise / compliance angle. |

## Tier 3 - Peer builders

| Handle | Why | What to reply with |
|---|---|---|
| _Seed list pending_ - x402 builders | From ecosystem listings. | Technical questions, edge cases. |
| _Seed list pending_ - Solana agent builders | From ecosystem. | Solana implementation chat. |
| _Per-event_ - Crypto AI hackathon winners | Track as announced. | Repost wins. Quote-post when Brij would slot in. |

## Tier 4 - Crypto media (infra coverage only)

| Handle | Why | What to reply with |
|---|---|---|
| @BanklessHQ | Cover agent infra. | Substantive replies on agent-payment narratives. |
| @TheBlock__ | Tier-1 trade press. | Source on x402 / agent payments. |
| @LightspeedPod | Solana-focused. | Pitch when there's a real story. |
| @decryptmedia | Broader crypto. | Source on agent / payment stories. |
| @sassal0x | Analyst on infra. | Engage on substance. |

---

## External X-watcher agent - input spec

A separate agent on an external server reads this file daily, scrapes the handles, and produces a ranked engagement queue. This section is its contract.

### Reads

Only this file. Parses every row in the Tier 1-4 tables. Columns: `Handle`, `Why`, `What to reply with`. Rows where the Handle is italic (`_..._`) are placeholders and skipped.

### Does

For each handle, daily:
1. Pull last 24h of original posts (not replies, not reposts).
2. Score each: relevance to Brij thesis (x402, Solana, agent payments, smart wallets, on-ramps, AI agent infra) + recency decay + post traction (likes + reposts + replies).
3. Rank top 5 across all handles into a single queue.

### Writes

One file per day: `Von-Doom-Studios/CLIENT-WORK/brij-marketing/engagement-queue/YYYY-MM-DD.md`. Creates the `engagement-queue/` folder on first run.

Each entry:

```
## [N of 5] @handle - <relative time>

**Post URL:** https://x.com/handle/status/...
**Post text:** <full text, truncated to 280 chars>
**Why it's high-leverage:** <one-line tied to the "Why" column>
**Suggested reply angle:** <one-line derived from the "What to reply with" column>
**Tier:** 1 | 2 | 3 | 4
**Score:** <integer>
```

### Cadence

Run 08:00 ET daily. Commit by 08:30 ET.

### Does NOT

- Post replies.
- Modify this file.
- DM anyone.
- Write outside `engagement-queue/`.

---

## Open items

1. Seed Tier 3 builder list. ~10-20 handles `[client]` already follows.
2. Confirm @brij_fi vs `[client]`-personal handle for Tier 4 media engagement.
3. Confirm the external X-watcher is wired to read this file.
