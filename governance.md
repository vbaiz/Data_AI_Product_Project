# Governance — our living file

> Created for Assignment 1, one line added every session. One question at the oral is drawn from this file.
> Answers are provisional: write what you know today, and mark what you still have to check.

## Session 1 — The Six Questions

| # | Question | Our answer (provisional) | To check with |
|---|---|---|---|
| 1 | **EU AI Act:** which risk tier is our agent in, and why? (minimal · limited — transparency: tell the user it is an AI · high-risk · prohibited) | Likely limited-risk transparency obligations for the conversational assistant. Users must be informed they are interacting with AI. Occupancy forecasting is not automatically high-risk; confirm the final classification based on intended use. | Legal / Compliance |
| 2 | **Data:** whose data does it use, and on what legal basis? (GDPR art. 6; what the B2B contract allows) | Uses partner support tickets, questions, class schedules, capacity, and booking history. Apply an appropriate GDPR Article 6 legal basis, minimize personal data, and define data-processing responsibilities in B2B contracts. | DPO / Legal |
| 3 | **Accountability:** who is accountable when it is wrong — and where is the human? | The product company is accountable for its system responsibilities. Partners approve offers before publication. Human support handles billing, payments, refunds, and financial disputes. | Product Lead / Legal |
| 4 | **Never:** what must it never do? (our first guardrail) | Never publish an offer without explicit partner approval, independently resolve financial disputes, or expose one partner's confidential data to another. | Product / Engineering |
| 5 | **Explainability:** explainable to whom — the customer, the support agent, the auditor? | Partners see why a class is flagged and the main forecast factors. Support agents see answer sources and escalation reasons. Auditors can review system logs, permissions, and approval records. | Product / Data Science |
| 6 | **People it cannot serve** | If the AI lacks reliable data or cannot resolve a request, it explains its limitations and offers human support. Financial requests are always escalated to a human. | Support Operations / Accessibility |

## Session 2 — the cost of error
- Which cost-of-error line is a **legal or reputational** risk, not just money? …
- Who in the company **owns** that risk? …

## Session 3 — data (to come)
## Session 4 — human-in-the-loop points and the override switch (to come)
## Session 5 — counter-metrics and the segments we report (to come)
## Session 6 — protected segments and the harm threshold that stops an experiment (to come)
## Session 7 — accountable owner, rollback authority, incident path (to come)
