# 01 — Problem statement

**Team:** 3 · **Agent:** ML occupancy prediction and last-minute offer recommendation agent · **Last updated:** 23 October 2026

> Every number says where it comes from: measured, analogy (a comparable, with its source) or guess (and how you will test it).

## 1. The problem in one sentence

Partner studios, fitness centres and sports facilities working with **[Company name, same business model as AlbertNative]** lose potential revenue when classes, courts or activity slots remain unbooked close to their start time. The company lacks a reliable, data-driven way to predict occupancy and identify which empty spots should be offered at a last-minute discount, when to publish the offer, and at what price. Success looks like increasing last-minute bookings and partner revenue while reducing unused capacity, without unnecessarily discounting spots that would have sold at full price.

| Number in the sentence | Value | Measured / analogy / guess | Source or test |
|---|---|---|---|
| Current unused capacity | To be established | Guess | Collect historical occupancy and booking data from partner studios and facilities |
| Increase in last-minute bookings | Target to be established | Guess | Compare the agent's recommendations with the current process through a pilot |
| Revenue generated from otherwise empty spots | Target to be established | Guess | Track incremental revenue, discount costs and bookings that would have happened anyway |

## 2. Problem tree — from symptom to cause

- **Symptom** (what people complain about): Partner studios and facilities have empty class places or court slots close to the activity time, while potential customers may be looking for available activities at a lower price.
- **Problem** (what is actually going wrong): The company and its partners cannot consistently predict which sessions will have unused capacity or determine the best timing and discount for a last-minute offer.
- **Root cause** (5 Whys):
  1. Why are spots left empty? Because demand does not always match available capacity.
  2. Why is demand difficult to anticipate? Because occupancy varies by day, time, season, location, activity type and instructor.
  3. Why can't partners respond consistently? Because booking data and operational knowledge may be spread across different studios, courts and booking systems.
  4. Why are last-minute offers not always effective? Because decisions may rely on manual judgement or fixed discount rules rather than predictions of expected occupancy and booking behaviour.
  5. Why is this a problem for the platform company? Because it coordinates multiple partner facilities and needs a scalable way to identify opportunities across its network without harming partners' normal pricing or revenue.
- **What would fix the cause:** An ML-based agent that predicts occupancy and the probability of a slot remaining empty, then recommends which slots to promote, when to publish an offer and what discount or price to propose. The recommendation should respect each partner's pricing rules and be approved by the company or partner before publication. ML handles prediction; business rules handle constraints and authorisation.

## 3. Is AI the right tool?

| Question | Our answer |
|---|---|
| Is there a rule that solves 80 % of it? | Fixed rules, such as offering discounts for slots that remain unbooked a few hours before starting, could provide a simple baseline. However, they may not capture differences between locations, instructors, activities, seasons and booking patterns. |
| Is it a prediction / generation problem, or an organisational decision? | Primarily a prediction problem: estimate occupancy and the probability of a slot remaining empty. Recommending a discount is a decision-support task that combines predictions with business rules and partner preferences. |
| Do we have the data — which, how much, who owns it? | Potentially, the company and its partners hold booking history, capacity, schedules, cancellations, prices, discounts, location, activity type, instructor and timestamps. Data availability, quality, access rights and sufficient historical volume must be verified with the company and its partners. |
| What does one error cost — and who pays it? | Overestimating demand may leave spots empty; underestimating demand may trigger unnecessary discounts for spots that would have sold at full price. Partners may lose revenue or trust, while the platform may lose commissions, bookings or partner relationships. The cost should be measured using booking and revenue data. |

**Level chosen:** Classical ML for occupancy and empty-slot prediction, combined with a rule-based recommendation layer and human approval. This is preferable to a GenAI-only solution because the core task requires structured historical data and measurable predictions. A fully autonomous agent is not necessary for the first version; automatic publication can be considered only after performance, safeguards and partner consent are validated.

## 4. Why this agent — the four selection questions

| Criterion | Our answer, one line |
|---|---|
| High frequency — is the work done every day or every hour? | Yes. Occupancy changes as bookings and cancellations arrive, and the company may need to identify opportunities across many partner facilities every day. |
| Bounded decision space — can we list its tools and outcomes on one slide? | Yes. The agent can analyse booking and schedule data, predict occupancy, rank potentially empty slots, recommend a publication time and discount, and send the proposal for approval. |
| Measurable success — can we say in one sentence whether it succeeded on one ticket? | Yes. Measure prediction accuracy and whether recommended offers generate incremental bookings and revenue compared with the current approach. |
| Recoverable failure — if it is wrong, is the damage limited and reversible? | Mostly, if recommendations require approval, discount limits are enforced, and offers can be withdrawn. Uncontrolled automatic discounting could damage revenue or customer trust, so it should not be part of the initial version. |

## 5. Press release (Working Backwards)

*23 October 2026 — [Company name] is introducing an ML-powered occupancy and last-minute offer recommendation agent to help its partner studios, fitness centres and sports facilities fill otherwise unused class places and court slots. By analysing historical bookings, capacity, time of day, seasonality, location, activity type, instructor and other relevant variables, the agent predicts which sessions are likely to have empty spots and recommends when and at what price to promote them. The goal is to generate incremental bookings and revenue for partners while giving customers more affordable ways to discover activities. “We can now identify opportunities across our partner network earlier and make more informed decisions about last-minute offers,” says [partner or company representative]. Quantified results and the customer quote will be added after a pilot validates the impact.*

## 6. What would have to be true?

| # | Hypothesis | Measured / analogy / guess | How we will test it | Session |
|---|---|---|---|---|
| 1 | Historical booking and schedule data can predict occupancy or empty spots more reliably than a simple fixed-rule baseline. | Guess | Compare ML predictions with a baseline using historical data; evaluate prediction error on unseen dates and facilities. | S4 prototype / S5 metrics |
| 2 | Last-minute offers based on predicted occupancy generate more incremental bookings and partner revenue than the current approach. | Guess | Run a controlled pilot comparing eligible sessions with and without agent-recommended offers; account for discounts and bookings that would have occurred anyway. | S5 metrics / S6 A/B |
| 3 | The company can access sufficiently complete and legally usable data from enough partner facilities to make reliable predictions. | Guess | Audit data coverage, quality, historical depth, partner permissions and contractual restrictions across a sample of studios and facilities. | S4 prototype |
| 4 | Partners are willing to accept recommendations when they retain control over discount limits and offer approval. | Guess | Interview partner managers, test a recommendation mock-up and measure approval rates during the pilot. | S4 prototype / S5 metrics |
| 5 | Customers will discover and book last-minute offers without significantly cannibalising full-price bookings. | Guess | Compare incremental bookings, discount cost, full-price booking changes and net revenue during a controlled pilot. | S5 metrics / S6 A/B |

## 7. Do-nothing baseline

If nobody builds the agent over the next 12 months, the company and its partner facilities will likely continue using their current booking systems, manual judgement, marketing campaigns or fixed discount rules to manage unused capacity. Staff may gradually improve their processes, and existing systems may add better reporting, but the company will still lack a consistent, network-wide way to predict occupancy and recommend targeted offers unless another solution is introduced. Empty slots may continue to represent missed revenue opportunities, while broad or poorly timed discounts may reduce margins on sessions that could have sold at full price. The size of this opportunity is not yet known and should be established from historical occupancy, booking and revenue data.