# Glossary — Strava Activation Squad (Group E)

Vocabulary used in `index.html` and `notes.md`, with disambiguations for terms that can mean different things in different contexts.

---

## Disambiguation

Terms that overlap or get confused. Read these first.

### Activity
- **In Strava (this deck):** a single recorded workout — a run, ride, walk, yoga session, etc. Logged either via GPS tracking, wearable sync, or manual entry.
- **In product analytics generally:** any user action (click, view, session).
- **Here, always means the Strava sense** unless prefixed (e.g. "user activity" in the analytics sense).

### Activation
Three distinct uses in the same deck — keep them separate:
1. **Activation (general PM concept):** the moment a new user experiences enough core value to be likely to retain.
2. **Activation Squad:** the team that owns the first-7-days experience (Group E).
3. **Activation Rate:** the squad's main metric — % of new users who log ≥1 activity AND follow ≥1 friend in their first 7 days.

### Segment
- **In Strava (this deck):** a user-defined stretch of road or trail with a leaderboard. "Segments Crossed / Matched" counts how many a user passes through.
- **In marketing:** a slice of the user base (cohort, persona).
- **In databases / code:** a partition of stored data.
- **In this deck, always the Strava feature.**

### PR
- **In Strava (this deck):** Personal Record — a user's best time/effort on a segment or distance. Metric #25.
- **In software engineering:** Pull Request. Not used in this deck.
- **In statistics:** sometimes "Precision-Recall." Not used here.
- **`pp` (lowercase) ≠ PR:** `pp` means "percentage points" (e.g. "+1pp" = a one-percentage-point lift).

### WAU vs WAL vs DAU vs MAU
All measure "active users" but with different windows and definitions:
- **DAU** — Daily Active Users. Anyone who opened the app on a given day.
- **WAU** — Weekly Active Users. Distinct users active in a 7-day window.
- **MAU** — Monthly Active Users. Distinct users active in a 28- or 30-day window.
- **WAL** — Weekly Active *Loggers*. Stricter than WAU — only counts users who logged ≥1 activity that week. Used here as a depth-vs-breadth pair with the NSM.

### Retention (D1 / D7 / D30 / D90)
All refer to the % of a cohort still active *after N days from sign-up*:
- **D1 retention:** active on day after install.
- **D7 retention:** active in week one (used by the Activation squad).
- **D30 retention:** active in month one (Active Base branch).
- **D90 retention:** active at three months (long-term habit signal).
The number after "D" is the day count from sign-up, not a calendar window.

### NSM vs Main squad metric vs MRR
Easy to conflate — they sit at different levels of the tree:
- **NSM (North Star Metric):** company-wide compass. Here: *Total Activities Logged*.
- **Main squad metric:** what the Activation squad optimizes. Here: *Activation Rate*. It is a leading indicator for the NSM, not the NSM itself.
- **MRR:** the financial output. Explicitly **not** the NSM because it lags and incentivizes paywall aggression.

### Premium / Paid / Subscription
Used near-interchangeably in this deck:
- **Premium** — the product tier name (Strava Premium).
- **Paid** — any user on Premium (vs Free).
- **Subscription** — the billing model. "Free → Paid Conversion" = the rate at which Free users start a Premium subscription.

### Leading vs Lagging indicator
- **Leading:** moves first, predicts future state (e.g. Activation Rate, First Kudos Loop, 7-Day Habit Rate).
- **Lagging:** moves last, confirms past state (e.g. MRR, LTV, Premium Churn). Optimizing lagging metrics directly is the "trap" the deck warns about.

### Funnel
- **In this deck:** the Day 0 → Day 7 sequence of steps a new user passes through (install, sign-up, profile, device pair, first log, first follow, first kudo).
- **In general PM:** any stepwise conversion sequence (acquisition funnel, checkout funnel, etc.).

### Streak
- **In the 7-Day Challenge feature:** the count of consecutive days the user has logged an activity. Resets at zero on a miss.
- **In Goodhart's-Law context:** the thing users will game by submitting empty 1-minute manual logs.

### Cohort
A group of users defined by a shared event in time — usually sign-up week. "Day-30 Cohort Retention" = "of users who signed up in week W, what % were active on day 30?"

### Goodhart's Law
"When a measure becomes a target, it ceases to be a good measure." In this deck, the rationale for every guardrail metric (GPS-Verified Activity Rate, Median Session Duration, manual-vs-GPS split during streaks).

---

## Definitions

Alphabetical within each section.

### Business model

- **ARPU** — Average Revenue Per User. Total revenue ÷ active users over a period.
- **B2B** — Business-to-business. Here: anonymized commuter routing telemetry sold to urban planners ("Metro").
- **B2C** — Business-to-consumer. Here: Strava Premium subscriptions sold to athletes.
- **CAC** — Customer Acquisition Cost. Marketing + sales spend ÷ new customers acquired.
- **Feature gate** — a Premium-only capability used to convert habituated free users (e.g. segment comparisons, route planner, training load).
- **Freemium** — free core product + paid upgrade tier. The free tier here also acts as the acquisition engine via the social graph.
- **LTV** — Lifetime Value. Expected total revenue from a user across their entire relationship with the product.
- **MRR** — Monthly Recurring Revenue. The monthly run-rate from active subscriptions.
- **Paywall** — the screen / interaction that gates a premium feature behind a subscription prompt.
- **Premium Churn Rate** — % of paying subscribers who cancel in a given period.
- **Social moat** — the defensibility that comes from the size and density of the user network. Hard for a competitor (e.g. Garmin Connect) to replicate.
- **Trial → Paid Retention** — % of trial starts that convert into a paid subscription after the trial window ends.

### Product metrics — acquisition & base

- **App Installs** — total downloads from app stores.
- **Day-30 / Day-90 Cohort Retention** — see Disambiguation.
- **Dormant Base** — users inactive for 1+ months. Pool that Reactivation targets.
- **DAU / WAU / MAU / WAL** — see Disambiguation.
- **Monthly Churned Users** — count of previously-active users who became inactive this month.
- **Profile Setup Completion** — % of sign-ups who fill name, image, location, and athletic type.
- **Reactivation Conversion Rate** — % of dormant users who return to an active state in a given window.
- **Stickiness Ratio** — DAU ÷ MAU. Closer to 1.0 = more frequent return visits.

### Product metrics — engagement & telemetry

- **Activity Density** — average number of workouts per user per week.
- **Commute logs ratio** — % of logged activities tagged as commute. Durable-habit signal because commuting is recurring by nature.
- **GPS-Tracked Activity** — workout recorded via live GPS, contrasted with manual entry.
- **GPS-Verified Activity Rate** — % of total logged activities that were GPS-tracked. Honesty signal against streak-gaming.
- **Manual Activity Submission** — user-entered workout without sensor data.
- **Median Session Duration** — middle value of activity lengths. Guards against many tiny "ghost" logs inflating the count.
- **Telemetry** — sensor data captured during an activity (GPS trace, heart rate, power, cadence). Sold in aggregate as the B2B "Metro" product.
- **Time Spent Recording** — total minutes the app was actively recording an activity.
- **Wearable Integration Sync** — activity ingested from a paired device (Garmin, Wahoo, Apple Watch).

### Product metrics — social & gamification

- **Athletic graph** — Strava's social network. The web of follow / followed-by edges between athletes.
- **Challenges** — opt-in goals (distance, time, segment) that run for a defined period.
- **Clubs / Groups** — communities of users (often local, sport-specific, or brand-affiliated).
- **Feed density** — volume of activity posts visible to a user. Higher density → more kudos exchanged → stronger retention.
- **Follow Graph Density** — average number of follow edges per active user.
- **Follow Graph Opt-in** — % of new users who follow at least one other user within 7 days.
- **Kudos** — Strava's "like" equivalent on an activity. The single strongest D7-retention predictor in this deck.
- **Personal Records (PRs)** — see Disambiguation.
- **Segments Crossed / Matched** — see Disambiguation.

### Funnel & activation (squad-level)

- **Activation Rate** — see Disambiguation. The squad's main metric.
- **Aha moment / Time-to-Aha** — the first moment the user experiences core value. Measured as median hours from sign-up to first upload.
- **Cold start** — the empty-state problem for new users (empty feed, no follows, no synced devices). The squad's mandate is to solve it.
- **Contact Sync Opt-in** — % of new users who share their address book so the app can seed follow suggestions.
- **Device Connection Rate** — % of new users who pair a wearable (Garmin / Wahoo / Apple Watch).
- **First Activity Log Rate** — % of a sign-up cohort that uploads at least one workout within 7 days.
- **First Kudos Loop** — % of new users who receive at least one kudo on their first activity within 24h.
- **Install → Sign-up CR** — Conversion Rate from install event to completed account registration.
- **Push Notification Opt-in** — % of new users who grant push permission.
- **7-Day Habit Rate** — % of new-user cohort that logs ≥3 workouts in their first calendar week. Strongest predictor of D90 retention in the deck.

### Monetization funnel

- **Free → Paid Conversion** — % of free users who start a Premium subscription in a window.
- **Premium Trial Start** — count of users initiating a free trial of Premium.
- **Subscription funnel** — the staged path from free use → trial start → paid retention.

### Frameworks & concepts

- **Constellation (of metrics)** — treating the NSM as a system of paired metrics (NSM + WAL + GPS rate + Session Duration) rather than a single number. The defense against gaming and seasonality.
- **Extrinsic vs intrinsic motivation** — extrinsic = external reward (badge, streak); intrinsic = internal drive (identity, health, community). "The Cliff" risk: extrinsic rewards can crowd out intrinsic motivation when they end.
- **Goodhart's Law** — see Disambiguation.
- **HEART framework** — Google's product-quality framework. Five dimensions:
  - **H**appiness — sentiment, survey scores.
  - **E**ngagement — depth and frequency of use.
  - **A**doption — uptake of a new feature.
  - **R**etention — return over time. (In this deck's HEART slide, "Referral" appears in place of Retention; both R's are common variants.)
  - **T**ask success — completion rate of the target task.
- **Leading vs lagging indicator** — see Disambiguation.
- **NSM (North Star Metric)** — see Disambiguation.
- **Power-user skew** — risk that the top 5% of users hide churn in the median. Counter: pair NSM with breadth metric (WAL).
- **Seasonality** — predictable recurring fluctuations (winter dips for outdoor activities). Counter: 12-week rolling averages and YoY (year-over-year) cohort curves.
- **Self-determination theory** — psych theory cited in the YouTube critique: forced re-engagement of users who deliberately disengaged raises long-term opt-out.
- **Squad** — a cross-functional team owning a slice of the product (here: Activation).
- **YoY** — Year-over-Year. Comparing the same calendar window across consecutive years to neutralize seasonality.

### Risks & guardrails

- **Burnout (push fatigue)** — risk that repeated daily nudges trigger a global push-notification opt-out.
- **The Cliff** — risk that engagement collapses on day 8 when the extrinsic reward of the 7-day streak ends.
- **Gaming** — users hitting the metric target via low-value behavior (e.g. 30-second manual log just to keep a streak).
- **Guardrail metric** — a metric watched to detect harm from optimizing the main metric (e.g. push opt-out rate, GPS share, manual-log share).
- **Mitigation** — the engineered counter to a risk (duration filter, auto-throttle, club recommendation on day 7).

### Miscellaneous

- **CTR** — Click-Through Rate. Of users shown something, % who tap.
- **pp** — percentage points. The arithmetic difference between two percentages (a move from 5% to 6% is +1pp, not +20%).
- **SLA** — Service Level Agreement. A contractual or self-imposed ceiling on a metric (used in the Uber critique re: rematch wait time).
