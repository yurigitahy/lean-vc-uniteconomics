# Metrics reference

Definitions, formulas, and the point at which each metric stops being trustworthy. All figures are in the operator's reporting currency. Every derived indicator is a ratio or a time period, so nothing here depends on a specific market.

## Contents

- [Revenue and ticket](#revenue-and-ticket)
- [Retention and churn](#retention-and-churn)
- [Acquisition cost](#acquisition-cost)
- [Lifetime value](#lifetime-value)
- [Cost of delivery](#cost-of-delivery)
- [Break-even and payback](#break-even-and-payback)
- [Concentration](#concentration)
- [Where these metrics break](#where-these-metrics-break)

---

## Revenue and ticket

**Average ticket (ARPA)** = monthly recurring revenue ÷ active paying customers.

Use active *paying* customers only. Free users, trials, and pilots inflate the denominator and understate the ticket, which then corrupts every downstream ratio.

**MRR** = sum of contracted monthly revenue, normalized. Annual contracts divide by twelve. One-off implementation fees are excluded from MRR and tracked separately, because including them makes growth look repeatable when it is not.

**Net new MRR** = new + expansion − contraction − churned.

Break this into its four components before diagnosing growth. A business with strong new MRR and equally strong churned MRR has an acquisition machine feeding a leaking bucket, and adding acquisition spend makes the problem worse, not better.

---

## Retention and churn

**Logo churn (monthly)** = customers lost in the month ÷ customers at the start of the month.

**Revenue churn (monthly)** = revenue lost from cancellations and downgrades ÷ revenue at the start of the month.

Track both. When logo churn is high and revenue churn is low, small customers are leaving and the base is concentrating, which is a concentration risk disguised as a retention success. When the reverse is true, large accounts are leaving, which is usually a value delivery failure at the top of the base.

**Gross revenue retention (GRR)** = (starting revenue − contraction − churn) ÷ starting revenue. Caps at 100%.

**Net revenue retention (NRR)** = (starting revenue + expansion − contraction − churn) ÷ starting revenue.

NRR is the single most informative retention number. NRR above 100% means the existing base grows on its own, and the business compounds even with acquisition paused. NRR at or below 100% means every unit of growth must be bought.

---

## Acquisition cost

**CAC (fully loaded)** = total acquisition spend in the period ÷ new customers acquired in the period.

Total acquisition spend includes: paid media, sales and marketing payroll with employer costs, sales tooling and CRM, events and travel, agency and contractor fees, and referral or partner commissions. It excludes: product engineering, customer support for existing accounts, and general management overhead.

The most common error in this metric is counting only paid media. That version of CAC is typically 40–70% below the real number in a sales-assisted business, which makes payback look short and justifies spend that is actually destroying cash.

**Blended CAC** uses all new customers including organic. **Paid CAC** uses only customers attributable to paid channels. Report both. Blended CAC hides deterioration in paid efficiency for as long as organic volume holds.

**CAC by channel** is required before any channel reallocation decision. Aggregate CAC averages a good channel and a bad one into a mediocre number that supports no decision at all.

---

## Lifetime value

Two methods. Use both and compare them.

**Method 1 — margin-based projection**

```
LTV = (average ticket × gross margin %) ÷ monthly revenue churn %
```

Always use gross margin, never gross revenue. Revenue-based LTV overstates value by exactly the cost of delivery, which is the entire quantity the diagnostic is trying to examine.

This formula assumes constant churn, which is almost never true. It is a ceiling estimate, not a measurement.

**Method 2 — cohort realization**

Take a cohort of customers acquired 12 or 24 months ago. Sum the actual gross profit they have produced to date. Divide by cohort size. This is realized LTV, and it is a fact rather than a projection.

When Method 1 exceeds Method 2 by more than roughly 50%, the churn assumption in Method 1 is wrong, usually because churn is front-loaded into the first months.

**LTV/CAC** = LTV ÷ fully loaded CAC.

Common reference band is 3x or above for a healthy model. Below 1.5x, each acquired customer destroys cash over its life. Above 5x is not necessarily good news: it often signals underinvestment in acquisition in a market that is still open, meaning the business is leaving the market to a competitor who is willing to spend.

---

## Cost of delivery

**Variable delivery cost** is everything that scales with usage: model inference and API calls, cloud compute and bandwidth, payment processing fees, per-transaction costs, per-seat licenses for tools embedded in delivery, marginal logistics.

**Cost to serve** is the human cost of keeping a customer alive: support and success hours, recurring meetings, manual renewals, manual onboarding, escalations. Calculate it as (fully loaded hourly cost of the people involved × hours consumed per customer per month).

Cost to serve is the number most often left out of unit economics entirely, and it is the one that most often explains why a business with apparently healthy gross margin cannot generate cash.

**Gross margin** = (revenue − variable delivery cost − cost to serve) ÷ revenue.

**Contribution margin per customer** = ticket − variable delivery cost per customer − cost to serve per customer.

If contribution margin is negative, growth accelerates cash burn. This is the single most important number in the diagnostic and it must be established before anything else is discussed.

---

## Break-even and payback

Never report "break-even" without qualifying which break-even is being calculated:

1. Structural break-even - covers the operating structure with acquisition paused.
2. Operating break-even - covers the company's current monthly operating and acquisition spend.
3. Maintenance break-even - covers the operating structure plus the acquisition required to replace churned customers and keep the customer base flat.

Do not describe structural break-even as company profitability.

Structural break-even customers =
fixed operating costs excluding acquisition spend
÷ contribution margin per customer

Operating break-even customers =
(fixed operating costs + current monthly acquisition spend)
÷ contribution margin per customer

Maintenance break-even customers =
fixed operating costs
÷ (contribution margin per customer - logo churn × CAC)

**Break-even in customers** = total monthly fixed cost ÷ contribution margin per customer.

Fixed cost includes all payroll not already counted in cost to serve or CAC, plus rent, non-variable software, insurance, accounting, and general overhead.

When contribution margin is zero or negative, break-even is undefined. No customer count reaches profitability. State this plainly rather than producing a large number.

**CAC payback (months)** = CAC ÷ contribution margin per customer per month.

Reference bands: under 12 months is comfortable, 12–18 months is workable when retention is strong, over 18 months is a severe cash risk because it exceeds the point at which churn has usually removed a meaningful share of the cohort.

**Marginal hire break-even** = fully loaded monthly cost of the hire ÷ contribution margin per customer.

This is the number to run before any headcount decision. It converts a hiring question into a customer-count question, which is the form in which it can actually be answered.

---

## Concentration

**Customer concentration** = revenue from the top 3 customers ÷ total revenue.

Above 40%, the business does not have unit economics, it has a small number of relationships. Averages across the base become meaningless and the correct analysis is account by account.

**Channel concentration** = new customers from the largest channel ÷ total new customers.

Above 70%, acquisition is a single point of failure exposed to platform policy changes, algorithm changes, or one partner relationship.

**Vendor concentration** = spend with the largest vendor ÷ total variable delivery cost.

High vendor concentration combined with high variable delivery cost as a share of revenue means an external party effectively sets the business's gross margin.

---

## Where these metrics break

- **Fewer than 30 customers.** Averages are dominated by individual accounts. Run account-level analysis instead of ratios.
- **Under 12 months of operation.** Churn has not had time to express itself. Any LTV figure is a projection built on a projection.
- **Rapid growth.** Period churn is understated because the denominator is inflated by recent customers who have not had time to leave. Use cohort retention curves rather than period churn.
- **Usage-based pricing.** Ticket varies by month per customer, so a single average ticket hides the distribution. Use median plus interquartile range, and separate expansion from base.
- **Long sales cycles.** CAC in a period does not correspond to customers acquired in that period. Lag acquisition spend to match the average cycle length before dividing.
- **Services-heavy delivery.** Gross margin depends on utilization, not on the price list. Model margin per delivery hour before modeling margin per customer.
