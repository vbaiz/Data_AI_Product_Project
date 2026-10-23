
# 00 — Bring-your-own pitch

**The company:** An AI-powered B2B SaaS assistant designed for ClassPass partner businesses, including fitness studios, gyms, and wellness facilities. ClassPass publicly reports **88,000+ businesses listed on its platform**, but the number of customers already using our proposed product is not yet established. For the initial business model, assume a **5-person support team** and **2,000 support tickets per month**; both are planning assumptions, not verified company data.

**The pain, as a cost:** ClassPass reports that **85% of fitness classes do not sell out**, highlighting the opportunity to improve the use of available capacity. It also reports that integrated studio partners fill less than **36% of total capacity through their own channels**. These figures indicate an opportunity, but do not establish how much revenue our product could recover. For support costs, assuming 2,000 monthly tickets, 40% repetitive questions, 12 minutes per ticket, and €25 per support hour, the potentially addressable workload is **160 hours or €4,000 per month**. These support-cost figures are hypothetical and must be validated.

**Do-nothing baseline:** Over the next 12 months, studios continue using ClassPass's existing booking tools, SmartTools, and support channels. Routine questions continue through existing workflows, while occupancy optimization benefits from current platform capabilities. Our product must demonstrate additional support savings and partner value beyond these existing tools.

**The agent's job:** When a partner asks a platform question or needs help with an upcoming under-occupied class, the agent answers using approved documentation or analyzes authorized booking data to explain occupancy risk and draft a last-minute offer for partner approval.

**Trust level per step:**
- **L4 — Autonomous:** Classify support tickets and generate occupancy forecasts.
- **L3 — Bounded assistance:** Answer platform questions and explain at-risk class forecasts.
- **L2 — Human approval:** Draft targeted offers; partners must approve before publication.
- **L1 — Human-only:** Escalate billing, payments, refunds, and financial disputes.

**One thing it must never do:** Publish an offer without explicit partner approval or independently resolve financial disputes.

**Why it is a product decision:** The company's Product Lead must decide whether to launch a free Support Agent and paid Pro Intelligence add-on. The decision balances potential support-cost savings and partner value against incorrect answers, ineffective discounts, data-access risks, and low paid adoption. Launch only after a pilot demonstrates reliable answers, useful forecasts, incremental commercial value, and effective safety controls.

## Checklist

- [x] Company type, ticket volume, and team size specified; unverified figures clearly labeled as assumptions.
- [x] Pain expressed as a potential cost, with calculations and external capacity evidence.
- [x] Do-nothing baseline accounts for existing ClassPass tools.
- [x] One clearly defined agent job.
- [x] Trust levels specified, including steps below L4.
- [x] One explicit safety guardrail.
- [x] A named product decision-maker and the risks of shipping.
