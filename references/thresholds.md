# Alert thresholds

Run these checks against the intake data before the first question. Any red condition is surfaced immediately, before the diagnostic proceeds, because it changes what the rest of the conversation should be about.

Every threshold here is a ratio or a time period. None depends on a currency, a market, or a stage. They are heuristics with a stated rationale, not laws. The recalibration section explains when to move them.

---

## Red

| Condition | Test | Why it matters |
|---|---|---|
| **Negative contribution margin** | variable delivery cost + cost to serve ≥ ticket | Every new customer consumes cash. Growth is the problem, not the solution. Nothing else in the diagnostic matters until this is fixed. |
| **Churn not measured** | no monthly logo or revenue churn figure available | LTV is an assumption, not a metric. Every acquisition decision downstream rests on nothing. |
| **Variable delivery cost > 30% of revenue** | variable cost ÷ revenue | Structural margin exposure. A third party controls a third of the economics and can reprice unilaterally. |
| **Payroll per customer > average ticket** | total payroll ÷ active customers, versus ticket | Either the business is far below its scale threshold or the team is oversized for the moment. Both are solvable, but only one is a growth problem. |
| **CAC payback > 18 months** | CAC ÷ monthly contribution margin | Severe cash risk. Beyond 18 months, churn has typically removed a meaningful share of the cohort before it repays acquisition. |
| **LTV/CAC < 1.5x** | LTV ÷ fully loaded CAC | Each acquired customer destroys cash over its life once delivery and service costs are counted. |
| **Top 3 customers > 40% of revenue** | top 3 revenue ÷ total revenue | The business has relationships rather than unit economics. Averages across the base are not meaningful and the loss of one account is an existential event. |

---

## Yellow

| Condition | Test | Why it matters |
|---|---|---|
| **Cost to serve > 25% of ticket with manual delivery** | cost to serve ÷ ticket | High-touch service on a ticket that cannot fund it. Margin erodes silently as the base grows. |
| **Single channel > 70% of new customers** | largest channel ÷ total new customers | Acquisition is a single point of failure exposed to platform, algorithm, or partner changes outside the operator's control. |
| **NRR at or below 100%** | (start + expansion − contraction − churn) ÷ start | No expansion inside the base. All growth must be purchased, forever. |
| **Gross margin below the model's floor** | see [references/business-models.md](references/business-models.md) | Roughly 70% for software, 40% for transactional, 30% for services-heavy. Below the floor, the model is behaving like a different business than the one it claims to be. |
| **Blended CAC diverging from paid CAC** | paid CAC trending up while blended stays flat | Organic volume is masking deterioration in paid efficiency. The masking ends when organic plateaus. |
| **Largest vendor > 60% of variable delivery cost** | vendor spend ÷ variable cost | An external party effectively sets gross margin and can change it without negotiation. |
| **Fewer than 30 customers** | count | Averages are dominated by individuals. Switch to account-level analysis rather than ratios. |

---

## Order of resolution

When several alerts fire at once, resolve in this order. Working out of order produces analysis that is technically correct and operationally useless.

1. **Negative contribution margin.** Nothing else can be reasoned about while each customer loses money.
2. **Churn not measured.** Without it, no LTV, no payback, no channel decision.
3. **Concentration above 40%.** It invalidates the averages the rest of the analysis would use.
4. **Payback and LTV/CAC.** These determine whether acquisition can be scaled at all.
5. **Variable cost and vendor exposure.** Structural, important, but rarely the binding constraint this quarter.
6. **Channel and expansion.** Growth quality questions, addressed once the model is sound.

---

## Recalibration

The thresholds assume a business selling recurring software or a recurring service to other businesses. Move them deliberately, and say so when you do.

**Move the variable-cost threshold up** for models where delivery cost is inherently high and priced in: hardware with a recurring layer, logistics, payment-heavy flows, inference-heavy products sold at a correspondingly higher ticket. What matters is contribution margin, not the variable cost ratio in isolation.

**Move the payback threshold down** for consumer businesses, low tickets, or any model with monthly cancellation and no contract. Six months is a more realistic ceiling when retention is short and voluntary.

**Move the payback threshold up** for enterprise contracts with multi-year terms, contractual lock-in, and documented NRR above 110%. Twenty-four months can be defensible when the cohort demonstrably survives it. It is defensible on evidence, not on optimism.

**Suspend the payroll-per-customer test** for businesses under twelve months old or with fewer than thirty customers. The team is built for a base that does not exist yet, which is a deliberate choice rather than a failure.

**Tighten the concentration threshold** for businesses seeking outside capital or planning a sale. Above 25%, concentration becomes a diligence finding regardless of how healthy the accounts are.

**Ignore NRR entirely** for models with no expansion surface, such as single-product, single-seat, fixed-price offerings. Instead test whether an expansion surface should exist at all, which is a `B1.R3` question.
