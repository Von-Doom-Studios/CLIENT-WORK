# Social Content Bank — BRIJ

Actual posts. Written to stop the scroll.

---

## CAMPAIGN 1: "WE EVOLVED" — Espresso Cash → BRIJ

---

### Thread #1: The Transformation Story (X — Monday, pin to profile)

**Tweet 1:**
We built a wallet.

Then we realized: a wallet isn't a business. It's a feature.

So we built the business. 🧵

**Tweet 2:**
Espresso Cash was fast. Clean. No seed phrases. Real transfers.

But every time an AI agent tried to use it, the same question came up: "I can hold money. Now what?"

It couldn't read a market. It couldn't pay for an API call. It couldn't book a flight. It couldn't convert your dollars into stablecoins without you lifting a finger.

A wallet alone is a dead end for software.

**Tweet 3:**
So we tore it open and built what was missing.

A read layer — your agent queries Jupiter, Orca, Raydium, Solend. One call. Structured data. Sub-100ms.

A write layer — declarative transactions. No SDK installs. No dependencies. The wallet signs autonomously with policy guards you set.

A payment layer — x402. Your agent hits an API, pays in stablecoins, gets access. Per request. No subscription. No API key. No merchant account.

An on-ramp — fiat in, USDC out, best rate across 10+ providers. One call.

**Tweet 4:**
Put it together and you don't have a wallet anymore.

You have an AI agent that reads markets, executes transactions, pays for what it needs, and funds itself.

Without you.

**Tweet 5:**
Espresso Cash didn't die.

It became the first organ of something alive.

We call it BRIJ. The agent layer for Solana.

brij.fi

And if you think that's the announcement — there's something else coming Friday.

---

### Video Script #1: "We Evolved" (45 seconds)

```
[0-3s] Black screen. Espresso Cash logo fades in, clean white.
[3-5s] Logo starts to glitch — digital distortion. Sound: electronic crackle.
[5-7s] Logo fragments scatter, reform into BRIJ logo. Sound: deep bass hit.
[7-10s] Text on screen: "We started as a wallet."
[10-12s] Cut to: clean shot of the Espresso Cash wallet interface. Peaceful. Simple.
[12-14s] Text: "Then we asked a question."
[14-17s] Text appears one word at a time: "What if... software... could do business?"
[17-19s] Hard cut. Fast montage begins. Sound: driving beat kicks in.
[19-20s] Screen: code flying in — "brij.read('jupiter, orca, raydium')" — flash of data
[20-21s] Screen: transaction executing — green confirmation flash
[21-22s] Screen: "HTTP 402 → pay 0.001 USDC → 200 OK" — settled
[22-23s] Screen: "$200 USD → 198.50 USDC" — conversion complete
[23-26s] Quick cuts: agent booking a flight, wallet balance updating, escrow settling
[26-30s] Montage freezes. Silence.
[30-33s] Text: "Read. Write. Pay. Onramp."
[33-37s] Text: "The agent layer for Solana."
[37-40s] BRIJ logo. brij.fi
[40-45s] Text fades in: "Your agent's first flight → travel.brij.fi"
```

**Music:** Dark electronic, builds energy. Think: the sound of something powering up.
**Mood:** Not corporate. Not crypto-bro. Feels like something is waking up.

---

## CAMPAIGN 2: "THE FLIGHT THAT BOOKED ITSELF" — Travel Launch

---

### Thread #2: Travel Launch (X — Monday Week 2, replace pinned)

**Tweet 1:**
I bought a plane ticket and never opened a browser.

No Google Flights. No Kayak. No "checking 400+ sites." No cookie-inflated prices.

I told my AI agent where I wanted to go. It found the flight, booked the flight, and sent me the confirmation code.

This is not a demo. It's live. Here's how. 🧵

**Tweet 2:**
The product is called BRIJ Travel. It's at travel.brij.fi.

Your agent connects via MCP on Grok. It hits the BRIJ Travel API — real airline inventory, real flights, real bookings. Paid in USDC on Solana using x402.

Four API calls: search, reserve, fund, booked.

That's not a simplification. That's the actual architecture.

**Tweet 3:**
Let's talk about what's actually happening to you when you book a flight today.

You search on Google Flights. Then you check Kayak. Then Skyscanner. Then the airline directly.

Every single one of those sites is tracking you. They share data. They see your desperation. And they adjust prices upward.

This isn't a conspiracy theory. Airlines spent $4.2B on dynamic pricing systems last year. The product is you.

**Tweet 4:**
Your AI agent doesn't have cookies.
It doesn't have a browser fingerprint.
It doesn't have search history.
It doesn't panic-refresh at 2am.

It makes a clean API call, gets the real price, and books it.

The airline's $4.2B pricing engine? Irrelevant.

**Tweet 5:**
What it costs:

Search: $0.10
Reserve: $0.10
Book: the ticket price

Total platform fees: twenty cents.

No subscription. No monthly minimum. No merchant account. No IATA accreditation.

You pay for the flight. And twenty cents. That's it.

**Tweet 6:**
Every booking is escrow-backed on Solana.

Your funds go into a per-intent escrow PDA. If the airline's price changed before confirmation — automatic refund. No support ticket. No dispute. No 7–10 business days.

The code handles it.

**Tweet 7:**
This is live. Right now.

→ Book a flight: travel.brij.fi
→ API docs: travel.brij.fi/openapi.json
→ Agent manifest: travel.brij.fi/llms.txt
→ x402 discovery: travel.brij.fi/.well-known/x402

The internet reserved HTTP status code 402 — "Payment Required" — in 1997.

For 29 years, nobody used it.

We did.

**[Attach: 30-sec launch video]**

---

### Video Script #2: "The Flight That Booked Itself" (30 seconds)

```
[0-2s] Split screen. LEFT: real person at laptop, 6 browser tabs visible.
       RIGHT: Grok chat interface, empty.
       Sound: typing, mouse clicking (agitated).

[2-5s] LEFT: Person switches between tabs. Google Flights. Kayak. Airline site.
       Price displayed: $487. They switch tabs. Come back. Price now: $512.
       Person visibly frustrated.
       RIGHT: Still empty. Cursor blinks.

[5-8s] RIGHT: Text appears in Grok: "Find me a flight SFO → Barcelona, June 15."
       LEFT: Still switching tabs. Price now $524.

[8-12s] RIGHT: Results animate in.
       "Flight 1: SFO → BCN | June 15 | 11:20am | $471 | Delta"
       "Flight 2: SFO → BCN | June 15 | 3:45pm | $489 | United"
       "Flight 3: SFO → BCN | June 15 | 9:00pm | $461 | Air France"
       LEFT: Person refreshes. Price: $531. Puts head in hands.

[12-15s] RIGHT: User types: "Book flight 3."
        Processing animation. Quick flash of escrow settling.
        "✓ Booked. Confirmation: AF-7X2K9. SFO → BCN, June 15, 9:00pm."
        LEFT: Person still comparing tabs.

[15-18s] LEFT side dims to black. RIGHT expands to full screen.
         Text overlay: "The flight that booked itself."

[18-22s] Text: "$461. Twenty cents in fees. Zero tabs. Zero tracking."

[22-26s] BRIJ Travel logo. travel.brij.fi

[26-30s] Small text: "BRIJ. The agent layer for Solana."
```

**Music:** Minimal. A single rhythmic pulse that builds subtle tension. Think: a clock ticking, then release when the booking confirms.
**LEFT side audio:** Faint frustration sounds — clicks, sighs, keyboard mashing.
**RIGHT side audio:** Clean, quiet. Just the confirmation chime.

---

### Thread #3: The x402 Origin Story (Antoine — Friday Week 2)

**Tweet 1:**
In 1997, the people designing HTTP created status code 402.

"Payment Required."

They wrote: "This code is reserved for future use."

Then everyone forgot about it. For 29 years.

We remembered. 🧵

**Tweet 2:**
Here's what 402 was supposed to be:

You make an HTTP request. The server says: "This costs money." You pay. You get the response.

No login. No API key. No subscription page. No credit card form. No merchant account.

Payment is the authentication. The internet's original vision for paid access.

**Tweet 3:**
We built x402 to make this real on Solana.

```
→ GET /api/signals/alpha
← 402 Payment Required
→ pay 0.001 USDC
← 200 OK (data returned)
```

Settled on-chain. 340ms. Receipt: 7fA…b21.

That's the entire flow. No auth headers. No billing dashboard. No monthly invoice.

**Tweet 4:**
Then we asked: what's the most complex thing an agent could buy with this?

A flight ticket.

Live airline inventory. Dynamic pricing. Multiple intermediaries. Real money. Real escrow. Real confirmation codes.

If x402 can handle a flight booking, it can handle anything.

**Tweet 5:**
For API providers, x402 means:

List your service. Set a price per call. An agent requests, pays, gets access.

You get USDC per request. We settle the payment.

No billing infrastructure. No auth system. No compliance overhead. Just revenue.

**Tweet 6:**
HTTP 402 waited 29 years for someone to use it.

Now an AI agent just used it to buy a plane ticket.

Read the spec: brij.fi/resources/x402-standard
Try the API: travel.brij.fi

The internet should have worked like this from the start.

---

### Standalone Social Posts — Travel Weeks

**"The Experiment" (with screenshots):**
We searched the same flight on Google Flights, Kayak, and BRIJ Travel.

Google: $487
Kayak: $502
BRIJ: $461

Same flight. Same airline. Same seat.

The difference? BRIJ doesn't know you've been searching for 3 days.

[Screenshots of all three]

**"The Receipt":**
One flight booked:
SFO → JFK
$312 USDC
Escrow settled: 0.8 seconds
Platform fee: $0.20
Airline confirmation: DL-4K7N2

That's what a flight booking looks like when software does the work.

**"The Math":**
Google Flights charges you nothing.

But airlines pay Google per click. That cost gets baked into your ticket price. Then the dynamic pricing algorithm sees you searched 3 times and adds more.

You're not the customer. You're the product.

On BRIJ, you pay twenty cents and the ticket price. No tracking premium. No middleman markup baked into the fare.

**"The Dare":**
Pick a flight you've been pricing.

Search it on Google Flights. Screenshot the price.
Now search it on BRIJ Travel.

Reply with both prices.

We dare you.

**"Speed":**
From "I need a flight" to "here's your confirmation code":

Kayak: 37 minutes (average, per their own data)
BRIJ: 30 seconds

We timed it.

**"For builders":**
The entire BRIJ Travel API:

POST /air/search — find flights ($0.10)
POST /air/intents — lock one in ($0.10)
POST /air/intents/{id}/book — pay and book (ticket price)
POST /air/intents/{id}/refund-requests — if price changed ($0.10)

OpenAPI spec: travel.brij.fi/openapi.json

4 endpoints. Full booking lifecycle. No account. No contract.

Build something.

---

## REDDIT POSTS

---

### Reddit #1: r/solana

**Title:** We used HTTP 402 to build the first AI-booked flight on Solana — here's how it works

**Body:**

We just shipped BRIJ Travel — the first flight booking service where an AI agent does the entire booking via x402 on Solana.

**The short version:** Your agent (Grok, via MCP) searches live airline inventory, selects a flight, and books it. Paid in USDC. Escrow-backed per-intent on Solana. Four API calls.

**Why this is interesting for Solana:**

The payment protocol is x402 — HTTP-native. Agent makes a request, server returns 402 Payment Required, agent pays in USDC, server returns 200 OK with the data. Authentication IS payment. No accounts, no API keys, no merchant onboarding.

Each booking creates a per-intent escrow PDA on Solana. Funds are held until the airline confirms. If the upstream price changed, the escrow refunds automatically.

Settlement: sub-second. Fees: $0.20 total for search + reserve. Booking: ticket price in USDC.

**Why this matters beyond flights:**

x402 turns any API into a pay-per-call service on Solana. We built flights first because it's the hardest — live inventory, dynamic pricing, multiple intermediaries, real money. If this works (it does), the protocol works for anything.

Try it: travel.brij.fi
Spec: travel.brij.fi/openapi.json
Agent manifest: travel.brij.fi/llms.txt

Technically this is the first real x402 merchant on Solana. Happy to go deep on the escrow architecture, the payment flow, or anything else.

---

### Reddit #2: r/ChatGPT

**Title:** I booked a real flight without opening a single website — just told my AI agent where I wanted to go

**Body:**

Built something I want to share: BRIJ Travel (travel.brij.fi).

I opened Grok, typed "Find me a flight from SFO to Barcelona on June 15," and got back real airline offers with real prices. Typed "Book flight 3" and got a confirmation code I can use to check in at the airport.

No Google Flights. No Kayak. No airline website. No browser tabs. No price manipulation.

**How it works under the hood:** The agent connects to our API via MCP. It uses a protocol called x402 — basically the agent pays a small amount in stablecoins (USDC) per API call and gets live flight data back. The booking is escrowed on Solana until the airline confirms.

**The interesting AI implication:** When you search flights on Google Flights, the airlines know. They track your cookies, your search frequency, your device. Prices adjust upward the more desperate you look. An AI agent making clean API calls has none of that baggage. It just gets the price.

Right now it requires Grok with MCP support and USDC. We're working on making it accessible to anyone (wallet integration, then credit cards). But wanted to share the current version with this community since it feels like a glimpse of where agent capabilities are heading.

Docs if you want to try it: travel.brij.fi/llms.txt

Happy to answer questions about the experience or the tech.
