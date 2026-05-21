# Viral Growth Engine — BRIJ

Based on Dropbox case study (3900% growth in 15 months) and proven viral mechanics from research.

---

## THE CORE LOOP

**Step 1:** User books a flight through BRIJ Travel
**Step 2:** Post-booking email offers referral rewards  
**Step 3:** Referred friend gets discount + referrer gets credits
**Step 4:** New user becomes referrer after their first booking
**Step 5:** Loop accelerates

**Key insight from research:** Referred users convert to referrers themselves. The system feeds itself.

---

## REFERRAL SYSTEM DESIGN

### Double-Sided Rewards (Dropbox Model)

| Action | Referrer Gets | Referred Friend Gets | Trigger |
|--------|-------------|-------------------|---------|
| Friend signs up via referral link | 5 free search credits ($0.50 value) | $5 discount on first booking | Email verification |
| Friend completes first booking | 10 more search credits ($1.00 value) | Receipt confirmation | Booking confirmation |
| Referrer hits 10 successful referrals | $20 BRIJ credit | — | Milestone reached |

### Why These Rewards Work
- **Immediate value:** Credits work instantly for next search
- **Low cost:** Search credits cost BRIJ $0.10 but feel valuable  
- **Viral trigger:** Both parties benefit, both share more
- **Milestone motivation:** Bigger reward at 10 referrals drives volume

---

## INTEGRATION POINTS

### 1. Post-Booking Email (24 hours after booking)
```
Subject: Your flight is confirmed + here's $5 for your next one

[Booking confirmation details]

Want $5 off your next flight? 

Share BRIJ with friends. They get $5 off their first booking, you get search credits for future trips.

Your referral link: https://travel.brij.fi/ref/[USER_ID]

Already shared with 3 people? You've earned $1.50 in search credits.
```

### 2. X Profile Bio Integration
```
Current: "The agent layer for Solana"
New: "The agent layer for Solana. Book flights with AI → travel.brij.fi/ref/brij"
```

### 3. In-App Prompts
- **After 3 successful searches:** "Invite friends and get free credits"
- **When hitting API limits:** "Get more searches: invite a friend or upgrade"
- **Mobile app launch:** Referral as onboarding step 3

### 4. Email Signature (Team)
```
— 
Anthony Emezu
BRIJ
P.S. Your AI agent can book flights now → travel.brij.fi/ref/anthony
```

---

## TECHNICAL IMPLEMENTATION

### MVP Requirements
1. **Unique referral codes** per user (travel.brij.fi/ref/[USER_ID])
2. **Credit system** in user accounts
3. **Tracking** from signup → first booking → referrer reward
4. **Automated emails** for rewards and milestones
5. **Dashboard** for users to see their referral stats

### Advanced Features (Phase 2)
- **Social sharing buttons** with pre-written messages
- **Leaderboards** showing top referrers
- **Bonus weekends** with 2x rewards
- **Team referrals** for companies using BRIJ

---

## VIRAL CONTENT HOOKS

### For X/Twitter
```
"I just booked a flight in 30 seconds. 

Airlines tried to track me across 6 sites to inflate the price. My AI agent has no cookies. No fingerprint. No search history.

It just got the real price.

Try it: travel.brij.fi/ref/[referral_code]"
```

```
"Same flight, 3 different sites:

Google Flights: $487 (tracked me)
Kayak: $502 (shared data with airline)  
BRIJ: $461 (clean API call)

Your AI doesn't get manipulated: travel.brij.fi/ref/[code]"
```

### For Reddit
```
Title: "I saved $40 on a flight because my AI agent doesn't have cookies"

Body: Posted this in r/travel but figured this community would appreciate the tech angle...

Airlines track your searches across sites and raise prices. My AI agent makes clean API calls with no tracking data. Same flight was $40 cheaper through the agent vs manual searching.

Built on x402 (pay-per-call) protocol on Solana. Pretty cool application of crypto infra to solve real problems.

[Link with referral code]
```

---

## SUCCESS METRICS

### Phase 1 Targets (Months 1-2)
- **Referral signups:** 20% of total new users come via referral
- **Referrer activation:** 30% of users make at least 1 referral
- **Viral coefficient:** 0.3 (each user generates 0.3 new users on average)

### Phase 2 Targets (Months 3-6) 
- **Referral signups:** 40% of total new users
- **Referrer activation:** 50% of users make at least 1 referral  
- **Viral coefficient:** 0.6+ (approaching self-sustaining growth)

### Viral Loop Health Checks
- **Time from signup to first referral:** <48 hours
- **Referral-to-conversion rate:** >15% (referred users book flights)
- **Referrer retention:** Users who refer stay active 3x longer

---

## LAUNCH SEQUENCE

### Week 1: Build + Test
- Implement referral tracking system
- Test email flows with team
- Create referral landing pages
- Set up analytics dashboard

### Week 2: Soft Launch  
- Enable for existing users only
- Send referral announcement email
- Monitor for bugs and user feedback
- Optimize based on early data

### Week 3: Full Launch
- Announce on social media
- Add referral hooks to all user touchpoints  
- Begin tracking viral coefficient daily
- Start weekly optimization cycles

### Week 4: Optimize + Scale
- A/B test reward amounts ($5 vs $3 vs $7)
- Test different referral messages
- Add social proof ("1,247 people have earned credits")
- Launch referral leaderboard

---

**This is the foundation.** Everything else (social content, email, ads) supports and amplifies this viral engine.
