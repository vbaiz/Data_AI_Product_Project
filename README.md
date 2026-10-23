# iSpot — ClassBook's partner-support agent that fills empty slots

**Course:** Data & AI Product: From Diagnosis to Delivery (MSA-DAT07-04) · Albert School · shared project with Agentic Workflows
**Cohort:** M2-INTER-1

## Team

| Name          | Git handle    | Also in the Agentic Workflows team? |
|---------------|---------------|-------------------------------------|
| Viviam Baiz   | vbaiz         | yes                                 |
| Hoang TRAN    | ntran-creator | yes                                 |
| Miguel Negrón | mnegron-cloud | no                                  |
| Chaume Carla  | carlachm      | no                                  |

## Our agent

- **Starting point:** bring your own (see `00_pitch.md`) — closest proposals: P6 (classical ML + LLM agent) and P8 (analysis requests answered faster)
- **The company:** ClassBook, a B2B booking and distribution platform for fitness studios and sports facilities in France · 3,000 partner venues · 5,000 partner tickets/month · partner-success team of 12 *(invented, labelled as guesses)*
- **The job, in one sentence:** When a partner opens a ticket about the platform, empty slots or last-minute offers, the agent answers it, checking our occupancy forecast when slots are involved, producing a same-hour answer and, where useful, a ready-to-approve offer instead of a 2-day manual reply.
- **Scope:** 3 ticket categories only — platform questions · unsold spots and last-minute offers · billing and payments (human only)
- **Trust level per step:** classify and route L4 (internal) · platform questions L3 (sampled) · occupancy forecast L4 (internal) · explain at-risk slots L3 · propose an offer **L2** (the studio approves before publication) · billing, payments, refunds **L1** (human only)
- **One thing it must never do:** publish an offer without the studio's approval, or below the studio's minimum price.
- **Business model:** the support agent is free for all partners (cost saving for partner success); a paid Pro tier makes it proactive — it flags at-risk slots before the studio asks and pre-drafts offers daily.

## Repository structure

One numbered file per session. Every member authors commits in at least four of the numbered files.

| File                          | Session                                                | Status      |
|-------------------------------|--------------------------------------------------------|-------------|
| `00_pitch.md`                 | before S3 — only if you bring your own idea            | in progress |
| `01_problem_statement.md`     | S1–S2 — Assignment 1                                   | in progress |
| `governance.md`               | created for Assignment 1, one line added every session | in progress |
| `02_sizing.xlsx`              | S2 — Assignment 2                                      | in progress |
| `02_investment_memo.md`       | S2 — Assignment 2                                      | to do       |
| `03_product_brief.md`         | S3                                                     | to do       |
| `04_architecture.md`          | S4                                                     | to do       |
| `05_metrics.md`               | S5                                                     | to do       |
| `06_ab_protocol.md`           | S6                                                     | to do       |
| `07_operations.md`            | S7                                                     | to do       |
| `08_launch_memo.md`           | S8                                                     | to do       |
| `spec.md`, `product_brief.md` | final                                                  | to do       |
| `/prototype`, `/evals`        | from S4                                                | to do       |

## How to run the prototype

To be added in S4 (Streamlit or FastAPI app in `/prototype`).

## Rules

- Commit with your own Git account: the individual question at the oral is about a commit you signed.
- Tag the final version `v1.0` before the first oral of your cohort. No commits after the first oral starts.
