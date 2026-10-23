# 01 — Problem statement

**Team:** 3 · **Agent:** own idea · **Last updated:** 2026-10-23

> Every number says where it comes from: **measured**, **analogy** (a comparable, with its source) or **guess** (and how you will test it).

## 1. The problem in one sentence

Independent fitness studios lose potential revenue when classes start with empty spots, while people who want to try activities such as Pilates, boxing or yoga may find regular prices too expensive or struggle to discover available classes. Today, studios often rely on manual promotions or leave spots empty. Success looks like increasing last-minute bookings and revenue per available spot without unnecessarily discounting customers who would have paid full price.

| Number in the sentence | Value | Measured / analogy / guess | Source or test |
|---|---|---|---|
| Empty spots per class | Not yet known | Guess | Interview 10–15 studio owners and collect booking data from pilot studios |
| Share of empty spots filled through offers | Not yet known | Guess | Run a pilot and compare offer bookings with the baseline |
| Revenue impact | Not yet known | Guess | Compare revenue per available spot before and during the pilot, accounting for discounts and fees |

## 2. Problem tree — from symptom to cause

- **Symptom** (what people complain about): Fitness studios have empty places in classes that are about to start. Meanwhile, potential customers may want to try a new sport but find regular prices expensive or available classes difficult to discover.
- **Problem** (what is actually going wrong): Class capacity is perishable inventory. Once a class starts, an empty spot can no longer be sold. Studios often lack a simple, data-informed way to decide which classes to promote, when to publish an offer and what price could attract customers while protecting revenue.
- **Root cause** (5 Whys):
  1. Why? Some classes have unsold places when the session begins.
  2. Why? Demand changes depending on the activity, instructor, location, day and time.
  3. Why? Studios may promote classes manually or too late to reach enough customers.
  4. Why? They may not have an easy way to combine booking pace, remaining capacity, historical demand and promotion results.
  5. Why? Smaller studios may lack the time, data or revenue-management tools needed to optimise last-minute sales.
- **What would fix the cause:** A marketplace where customers can discover and book last-minute sports deals, combined with a studio dashboard that recommends when to publish an offer and what price to propose. Start with transparent rules and studio-approved limits, then introduce machine learning if enough reliable booking data becomes available. This is initially a process and rule-based solution, with a potential ML component.

## 3. Is AI the right tool?

| Question | Our answer |
|---|---|
| Is there a rule that solves 80 % of it? | A simple rule could flag classes below a booking threshold a few hours before they start and suggest a studio-approved discount. This should be tested before building a more complex model. |
| Is it a prediction / generation problem, or an organisational decision? | Primarily a decision-support problem. Predicting final attendance or the probability of booking at different prices could improve recommendations, but studios should remain in control of prices and offers. |
| Do we have the data — which, how much, who owns it? | Not confirmed yet. Useful data includes class schedules, capacity, timestamped bookings, cancellations, attendance, standard prices and past promotion results. Studios would need to provide access. Start by checking data availability and quality with pilot partners. |
| What does one error cost — and who pays it? | A discount that is too generous can reduce revenue or replace a full-price booking; a price that is too high can leave a spot empty. The studio bears the commercial cost. Price floors, discount caps and studio approval can limit the risk. |

**Level chosen:** Rules first, then **classical ML** if the pilot provides enough reliable data. Rules can handle basic cases without training data. ML could later predict booking probability or demand and improve timing and price recommendations. GenAI is not necessary for the core task, and an autonomous agent would be excessive for the first version.

## 4. Why this agent — the four selection questions

| Criterion | Our answer, one line |
|---|---|
| High frequency — is the work done every day or every hour? | Yes. Studios manage bookings and class schedules daily, and last-minute availability can change throughout the day. |
| Bounded decision space — can we list its tools and outcomes on one slide? | Yes. Using class capacity, time until the session, booking pace, historical demand and studio price limits, the system recommends which class to promote, when to publish and what offer price to test. |
| Measurable success — can we say in one sentence whether it succeeded on one ticket? | Yes. Measure whether the offer generates incremental bookings and improves revenue per available spot compared with the baseline, while respecting the studio's minimum price. |
| Recoverable failure — if it is wrong, is the damage limited and reversible? | Mostly. The studio can review, edit or reject a recommendation before publishing. Price floors, discount caps and the ability to stop an offer reduce potential losses. |

## 5. Press release (Working Backwards)

*Paris, 23 October 2026.* Today, **[Product name]** introduces a last-minute fitness marketplace designed to help independent studios fill empty class spots and help customers discover new sports at more accessible prices. Customers can find and book available places in activities such as Pilates, boxing and yoga, while studios receive recommendations on when to publish offers and what price to propose based on booking activity and studio-defined limits. The pilot will measure whether the platform increases last-minute bookings and revenue per available spot compared with the existing process. “We want to fill more places without turning every class into a discount,” said **[pilot studio owner, quote to be validated]**.

## 6. What would have to be true?

| # | Hypothesis | Measured / analogy / guess | How we will test it | Session |
|---|---|---|---|---|
| 1 | Studios experience frequent last-minute empty spots and consider them a meaningful business problem. | Guess | Interview 10–15 studio owners about empty capacity, current solutions and willingness to pilot the product. | S4 prototype |
| 2 | Last-minute deals generate additional bookings instead of mainly discounting customers who would have paid full price. | Guess | Run a limited pilot and compare similar classes or time windows; track bookings, realized revenue and new versus returning customers. | S5 metrics / S6 A/B |
| 3 | Booking history and class details provide enough information to recommend useful offer times and prices. | Guess | Collect schedules, capacity, timestamped bookings and promotion results. Compare simple rules with a historical baseline before testing ML. | S5 metrics / S6 A/B |

## 7. Do-nothing baseline

If nobody builds this product in the next 12 months, studios will likely continue using their existing booking platforms, social media, email, messaging groups or manual discounts to promote classes. Some may improve their processes, but last-minute demand will still fluctuate and empty spots will expire when classes begin. Customers will continue discovering available classes through separate studio channels rather than one marketplace.

This is a hypothesis, not a proven forecast. To establish a baseline, measure the share of class capacity left empty at start time, the number of last-minute bookings, revenue per available spot, discount levels and repeat attendance over 4–8 weeks. Compare these results with the pilot to determine whether the product creates measurable additional value.