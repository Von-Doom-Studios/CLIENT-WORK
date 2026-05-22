# 11 - ANALYTICS: Brij Marketing

What we track weekly. What we track per campaign. The format of the report that goes to founders. If a number isn't tracked here, it isn't real to us.

**Owner:** VD-Marketing
**Related files:** [02-STRATEGY.md](./02-STRATEGY.md), [05-CALENDAR.md](./05-CALENDAR.md), [06-CAMPAIGNS.md](./06-CAMPAIGNS.md)
**Last updated:** 2026-05-22

---

## Core metrics

Trended week over week. Compared to the 90-day and 12-month targets in [02-STRATEGY.md](./02-STRATEGY.md).

### Followers and reach

| Metric | Source | Frequency |
|---|---|---|
| X followers (total + delta) | X analytics | Weekly |
| X impressions (7d) | X analytics | Weekly |
| X profile visits (7d) | X analytics | Weekly |
| X link clicks (7d) | X analytics + Loops UTM | Weekly |
| LinkedIn followers (total + delta) | LinkedIn page analytics | Weekly |
| LinkedIn impressions (7d) | LinkedIn page analytics | Weekly |
| YouTube subs (total + delta) | YouTube studio | Weekly once live |
| YouTube watch time (7d) | YouTube studio | Weekly once live |

### Email

| Metric | Source | Frequency |
|---|---|---|
| Total subscribers | Loops | Weekly |
| New subscribers this week | Loops | Weekly |
| Subscribers by source tag | Loops segments | Weekly |
| Welcome email open / click | Loops | Weekly |
| Lifecycle email open / click | Loops | Weekly |
| Newsletter open / click (monthly) | Loops | Monthly |
| Replies to lifecycle (the "what are you building" email) | Inbox count | Monthly |

### Product (proxy for actual traction)

| Metric | Source | Frequency |
|---|---|---|
| Bookings on travel.brij.fi | Founder reports / API | Weekly |
| x402 endpoint calls (any) | Founder reports | Weekly |
| Net USDC settled through Brij | Founder reports | Weekly |

### Engagement (organic growth lever)

From [08-ENGAGEMENT.md](./08-ENGAGEMENT.md):

| Metric | Source | Frequency |
|---|---|---|
| Substantive replies sent (count) | Manual log | Weekly |
| Notable amplifications (T1 accounts reposting/quoting us) | Manual log | Weekly |
| Inbound DMs / replies from builders | Manual log | Weekly |

### Paid (when active)

From [03-BUDGET.md](./03-BUDGET.md):

| Metric | Source | Frequency |
|---|---|---|
| Total paid spend (week) | Ad platforms | Weekly |
| Cost per follower (paid channels) | Computed | Weekly |
| Cost per email (paid channels) | Computed | Weekly |
| Boosted post performance vs organic | Computed | Per boost |

## Weekly report format

Sent in Discord #marketing every Monday by VD-Marketing. Plain text, short, in this exact order:

```
Brij - Marketing Week [N] ([date range])

PROGRESS TO 90-DAY
- X followers: [current] / 500 target  ([delta this week])
- Emails: [current] / 1000 target  ([delta this week])
- Bookings: [current] / 50 target  ([delta this week])

CONTENT
- X posts shipped: [N]   top post: [URL]   ([impressions], [engagements])
- LinkedIn posts shipped: [N]   top post: [URL]   ([impressions])
- Engagement replies: [N]   notable amplification: [account or "none"]

EMAIL
- Subs: [current] (+[delta])
- Top source this week: [source_tag] ([N])
- Welcome email open rate: [%]

PRODUCT
- Bookings this week: [N]
- Notable: [one-line use case or anomaly]

PAID
- Spend: $[N]
- CPF: $[N]   CPE: $[N]

FLAGS
- [Anything off-trajectory, blocked, or needing founder input]

NEXT WEEK
- [3-5 bullet headlines for what's coming]
```

If a number doesn't exist that week, write "n/a" rather than skipping the line. Consistency matters.

## Monthly retro format

Sent in #marketing on the first Monday of each month. Adds:

- Trend lines vs the 12-month target trajectory (are we ahead, on, or behind)
- Best-performing content + theory of why
- Worst-performing content + theory of why
- Campaign retros for any campaigns that closed (see [06-CAMPAIGNS.md](./06-CAMPAIGNS.md))
- Recommended adjustments to strategy, calendar, or budget for the next month

## Per-campaign reporting

Every campaign in [06-CAMPAIGNS.md](./06-CAMPAIGNS.md) gets a retro within 5 days of campaign close. Format:

```
Campaign [N] Retro - [name]

Window: [start] to [end]

Targets vs actuals:
- [metric 1]: [target] / [actual]
- [metric 2]: [target] / [actual]
- ...

What worked: [3 bullets]
What didn't: [3 bullets]
What we'd do differently: [3 bullets]
What we keep doing: [3 bullets]

Budget spent: $[N] vs $[N] allocated
```

## 90-day checkpoint review

The hard gate from [02-STRATEGY.md](./02-STRATEGY.md). On 2026-08-21:

If we are below 250 emails or below 10 bookings: strategy re-cut. Marketing produces a written re-cut proposal for founder review within 48 hours of checkpoint.

If we are between 250-499 emails and 10-49 bookings: strategy continues with mid-course corrections, documented in this file.

If we hit or exceed targets: continue, increase paid spend per [03-BUDGET.md](./03-BUDGET.md), and lock the second-quarter plan within 7 days.

## Tooling

Lightweight to start. Upgrade later only when bottlenecked by data access.

- **X analytics:** native X analytics dashboard. Founder shares weekly screenshot or @brij_fi login access to VD-Marketing.
- **LinkedIn:** native page analytics. Same.
- **YouTube:** native YouTube Studio.
- **Email:** Loops dashboard.
- **UTM tracking:** Loops UTM properties + a simple lookup table in this file for active campaign tags.
- **Engagement log:** plain markdown file or row added to this file's weekly section. Not building a tool for this yet.
- **Bookings / product:** founder reports for now. When volume justifies it, lightweight dashboard.

## Open items for Anthony

1. Confirm access path for founder-only platforms (X analytics, LinkedIn page admin, YouTube Studio) - either share screenshots weekly or give VD-Marketing limited login.
2. Confirm booking and x402 call numbers source - founder report or API access.
3. Approve weekly report format above.
