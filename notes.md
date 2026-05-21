# Presenter Notes — Strava Activation Squad (Group E)

Preparation material for Session 04. Not part of the public deck.

---

## Navigation cheatsheet

- `→` — move to next zone (top-level section)
- `↓` — drill into the current zone's vertical stack
- `S` — toggle speaker notes window
- `Esc` — slide overview grid

---

## Defending our tree

### Q: Why isn't your NSM paid subscriber volume?

**Defend:** paid subs are a lagging output of habit. Targeting them directly destroys the free-network flywheel that feeds the paywall in the first place. A user with 50 logged workouts is dramatically more likely to upgrade than one with 2 — NSM moves money, with lag.

### Q: Won't a 7-day streak burn out beginners?

**Defend:** the challenge accepts any activity — walk, yoga, stretch. The point is the digital habit of logging, not athletic intensity. Push opt-out rate is our safety valve, auto-throttled if delta vs control exceeds 2pp.

### Q: Dual-criteria activation feels arbitrary — why both log AND follow?

**Defend:** Strava lives at the intersection of tracking and community. A user who logs alone (no kudos) churns ~50% faster. A user who only follows but never logs is a passive lurker. Real activation needs both. Optimising for first-run alone produces ghost users; optimising for follows alone produces lurkers.

### Q: How do you know Activation Rate actually moves NSM?

**Defend:** the causal chain is mapped in Zone 3. A +1pp move in Activation Rate propagates into a ~0.4pp lift in D90 retention and a ~0.2pp lift in free→paid conversion six months later. We own the leading indicator; finance owns the lagging one.

---

## Challenges to other teams

### Card A — Uber Matching (one-tap rematch)

- Does the rematch queue cannibalise standard dispatch? If a closer driver is being held for the rematch, are nearby new riders waiting longer?
- Where's the SLA guardrail? You need a ceiling on rematch wait time before falling back to the standard pool.
- What's the rider-side dark pattern risk if rematch keeps returning a worse ETA than the original?

### Card B — Glovo (reject without penalty)

- What stops couriers from rejecting every low-value order with a plausible reason? "Unsafe area" is unverifiable.
- Where's the order-completion guardrail? If rejection rate spikes, average delivery time degrades for everyone.
- Have you instrumented the reason-tag distribution? If "bad weather" trends 5× higher in dense urban areas, that's not weather — that's gaming.

### Card C — Revolut Investments (price improvement alert)

- The alert is decision friction. What's your placement-abandonment rate post-alert?
- Compliance angle: are you legally allowed to characterise a spread as "X% worse" without market-data attestation?
- For the "wait" option — what's your timeout and what happens if the spread never normalises in volatile sessions?

### Card D — Etsy visual search

- User photos are dark, angled, low-res. What's your zero-result rate, and what does the fallback experience look like?
- Search-to-detail CTR vs text search: visual search optimises for "looks like" but Etsy buyers also filter on material, size, shipping. Where's the bridge?
- How do you prevent the feature becoming a copyright scanner for handmade sellers?

### Card F — YouTube weekly digest

- Dormant-user pushes drive uninstalls, not just opens. Where's the uninstall / push-disable guardrail?
- If a user's subscribed channels haven't uploaded in 7 days, what does the digest say? An empty digest is worse than no push.
- 7-day cohort: are you re-engaging users who deliberately took a break? Self-determination theory says forced re-engagement raises long-term opt-out.

---

## Attack/defense strategy summary

- **Defence stance:** stand on network density. The free graph IS the moat. Anything that erodes it (aggressive paywalls, gamed metrics, push fatigue) is an existential risk, not a quarterly tradeoff.
- **Attack stance:** look for unguarded second-order effects — queue cannibalisation (Uber), gaming incentives (Glovo), zero-result UX (Etsy), uninstall blowback (YouTube).
