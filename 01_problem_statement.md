# 01 — Problem Statement

**Team:** 3 · **Agent:** ClassPass Smart Class & Booking Assistant · **Last updated:** 23 October 2026

*Evidence convention: Measured = published data or internal data; Analogy = external research; Guess = proposed target to validate through a pilot.*

## 1. The problem in one sentence

ClassPass partner studios spend time resolving platform questions and managing under-occupied classes, creating support costs and missed booking opportunities. ClassPass reports that 85% of fitness classes do not sell out, while generative AI offers potential to improve customer-care productivity. The proposed assistant aims to reduce support handling time by **20%** and increase occupancy in targeted classes by **3 percentage points** versus a control group.

| Number in the statement | Value | Evidence type | Source or test |
|---|---|---|---|
| Fitness classes that do not sell out | 85% | Measured — ClassPass data | ClassPass Partner FAQs, based on integrated partner data from 2025 |
| Studio capacity filled through studios' own channels | Less than 36% | Measured — ClassPass data | ClassPass Partner page, July 2025–June 2026 |
| Potential customer-care productivity value from GenAI | 30–45% of current function costs | Analogy — industry estimate | McKinsey, *The Economic Potential of Generative AI* |
| Reduction in support handling time | 20% | Guess — pilot target | Compare median handling time before and after the pilot |
| Increase in target-class occupancy | +3 percentage points | Guess — pilot target | Compare eligible classes with a control group |

## 2. Problem tree — from symptom to cause

- **Symptom:** Partners need help with platform features and struggle to identify classes with unsold capacity.
- **Problem:** Support is largely reactive, while occupancy decisions require manual monitoring and intervention.
- **Root cause — 5 Whys:**
  1. Why? Partners spend time finding answers and monitoring bookings.
  2. Why? Guidance, booking data, and recommendations are not necessarily available in one workflow.
  3. Why? Support processes focus on answering requests rather than proactively identifying opportunities.
  4. Why? Booking patterns are not always translated into timely, actionable recommendations for partners.
  5. Why? Support automation and occupancy optimization need to be connected through shared data, permissions, and approval processes.

- **What fixes the cause?** Build an AI assistant combining platform support, occupancy forecasting, and last-minute offer recommendations, with studio approval before publication and human escalation for financial issues.

**Fix type:** GenAI + predictive machine learning + business rules + workflow integration.

## 3. Is AI the right tool?

| Question | Answer |
|---|---|
| Can rules solve 80% of the problem? | Rules and FAQs may handle repetitive questions, but the 80% coverage hypothesis must be tested against historical tickets. |
| Is this prediction, generation, or an organizational decision? | All three: GenAI answers questions and drafts offers; ML forecasts occupancy; studios decide whether to publish offers. |
| Do we have the data? | Required: platform documentation, support tickets, class schedules, capacity, booking and cancellation history, and offer performance. Availability and quality must be confirmed with ClassPass. |
| What does an error cost, and who pays? | Incorrect guidance creates operational work; poor forecasts or discounts may reduce studio margins. ClassPass bears support and trust costs; studios bear potential commercial losses. Financial issues remain human-managed. |

**Technology choice:** A bounded AI agent combining GenAI, predictive ML, and deterministic rules.

**Why not a simpler solution?** A scripted chatbot can handle fixed FAQs but cannot flexibly interpret questions or generate contextual recommendations. A fully autonomous agent would create unnecessary operational and commercial risks.

**Three-level support framework**

| Level | Capability | Access and autonomy |
|---|---|---|
| L3 — Platform Support | Answer questions and guide class setup, booking, and platform workflows | Free; automate permitted, low-risk tasks |
| L2 — Occupancy Intelligence | Forecast occupancy, flag at-risk classes, and draft targeted offers | Paid Pro; studio approval required before publication |
| L1 — Financial Support | Billing, payments, refunds, and financial disputes | Human-only resolution |

**Task-level trust framework:** L4 — autonomous ticket classification and forecasting; L3 — platform explanations and forecast explanations; L2 — offer proposals requiring approval; L1 — human-only financial support.

These are separate frameworks: the first describes product capabilities; the second describes task-level autonomy.

## 4. Why this agent? — Four selection criteria

| Criterion | Assessment |
|---|---|
| High frequency | Support questions and booking management recur throughout normal studio operations; validate frequency using ticket and booking data. |
| Bounded decision space | Tools are limited to approved documentation, ticket classification, authorized booking data, forecasts, offer drafts, approval requests, and human escalation. |
| Measurable success | Target 20% lower median handling time, at least 90% correct answers on a reviewed test set, and +3 percentage points in occupancy versus control. |
| Recoverable failure | Answers can be corrected, drafts rejected, and cases escalated. No offer is published without studio approval; financial actions remain with humans. |

## 5. Press release — Working Backwards

*Illustrative launch announcement, not a claim that the product has launched.*

**ClassPass introduces Smart Class & Booking Assistant to simplify studio operations**

ClassPass is introducing an AI-powered assistant to help fitness studios resolve platform questions and identify opportunities to fill under-occupied classes. 

- The free Support Agent answers common questions and guides partners through supported workflows. 

- The paid Pro Intelligence add-on forecasts occupancy, flags at-risk classes, and drafts targeted last-minute offers for studio approval. Billing, payments, and refunds remain with human support. 

- The pilot targets a **20% reduction in median support handling time** and a **3-percentage-point increase in occupancy** for eligible classes compared with a control group. Results will be published only after validation.

## 6. What would have to be true?

| # | Hypothesis | Evidence type | How to test it | Session |
|---|---|---|---|---|
| 1 | At least 20% of eligible support tickets can be resolved without human intervention. | Guess — target | Review historical tickets and measure correct, independently verified resolution. | S4 prototype / S5 metrics |
| 2 | AI reduces median handling time by at least 20%, with at least 90% answer correctness. | Guess — target | Compare with the existing workflow using a representative, human-reviewed test set and pilot. | S4 / S5 |
| 3 | Occupancy forecasts outperform a simple historical baseline by at least 10% on the chosen error metric. | Guess — target | Back-test using time-based holdouts; compare mean absolute error against a defined baseline. | S5 metrics |
| 4 | Approved offers increase occupancy by at least 3 percentage points versus control. | Guess — target | Run a controlled pilot and measure incremental bookings, occupancy, discount costs, and contribution margin. | S5 / S6 A/B test |
| 5 | Partners see sufficient value to pay for Pro Intelligence. | Guess — hypothesis | Interview partners and test willingness to pay, conversion, and retention. | S4 / S5 |
| 6 | Approval and escalation controls prevent unauthorized actions. | Guess — acceptance criterion | Test approval workflows; require 100% of published offers to have recorded approval and 100% of test financial cases to route correctly. | S4 / S5 |

**Pilot measurement definitions**

- **Support handling-time reduction:** (Baseline median handling time − pilot median handling time) ÷ baseline median handling time.
- **Answer correctness:** Correct, policy-compliant answers ÷ answers independently reviewed.
- **Forecast improvement:** (Baseline forecast error − model forecast error) ÷ baseline forecast error.
- **Occupancy uplift:** Treatment-group occupancy change minus control-group occupancy change, expressed in percentage points.
- **Commercial value:** Incremental revenue minus discount costs and other incremental costs, accounting for displaced bookings where measurable.

All targets above are **proposed acceptance criteria**, not published ClassPass results. Establish the baseline and sample size before the pilot, and report uncertainty alongside the results.

## 7. Do-nothing baseline

Over the next 12 months, partners will continue using existing platform tools and support channels. Documentation and staff experience may improve, and existing ClassPass SmartTools may continue optimizing availability. Therefore, the assistant must demonstrate incremental value beyond current capabilities, not merely reproduce existing functionality.

**Baseline to collect before launch:**

- Monthly support-ticket volume, median handling time, first-contact resolution, and repeat-contact rate.
- Percentage of eligible tickets resolved correctly without human intervention.
- Class occupancy by class type and lead time, using a consistent definition of available capacity.
- Forecast error and performance of existing scheduling tools.
- Incremental bookings, discount costs, contribution margin, and partner adoption of existing tools.

**Go/no-go decision:** Proceed if ticket analysis identifies a meaningful automation opportunity, forecasts outperform the baseline, and a controlled trial shows positive incremental commercial value without unacceptable accuracy or safety issues. Scale only after the pilot confirms the results.

## 8. Sources

1. ClassPass — Partner FAQs. Reports that 85% of fitness classes do not sell out and explains its SmartSpot inventory-optimization approach.

https://classpass.com/partners/faqs?utm_source=chatgpt.com