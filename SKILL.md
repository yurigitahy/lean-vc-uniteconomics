---
name: unit-economics
description: Progressive unit economics and scalability diagnostic for any business with paying customers. Use this skill whenever someone wants to analyze their business model, improve unit economics, understand why growth is not compounding, or asks about pricing, ticket size, CAC, churn, LTV, COGS, cost to serve, payback, or break-even. Also trigger when someone describes a problem with margins, growth, acquisition channels, retention, concentration, or cost structure, even if they never use those terms explicitly.
---

# Unit Economics Diagnostic

A progressive diagnostic of business model and unit economics, structured as the nine Business Model Canvas blocks regrouped into three questions that actually matter:

- **B1 — Value capture potential.** How much money the model can capture.
- **B2 — Cost of realizing that potential.** What it costs to acquire and keep a customer.
- **B3 — Cost of existing and operating.** What it costs to run the machine that serves them.

Works for subscription, usage-based, transactional, marketplace, and service businesses. See `references/business-models.md` for how each dimension shifts by model.

## Execution rules

Read this entire file before starting. Do not skip steps.

### Core principle

This skill does not produce generic answers. Every response is generated from the data the operator supplied, confronted with external research where relevant, and ends with either a follow-up question or a validation task. The goal is to make the operator think, not to reassure them.

### Execution flow

1. Collect the operator's data (see **Intake** below).
2. Run external research on the market, segment, and competitors before generating any response.
3. Walk the questions block by block, one question at a time.
4. For each question: three to four paragraphs of critical analysis, then close with a follow-up question OR a validation task.
5. Advance to the next question only when the operator answers or explicitly asks to move on.
6. Change blocks only when the operator asks.

### Tone

- Analytical, direct, no generic praise.
- Write like a mentor talking: informal enough not to be verbose, thorough enough to teach.
- Explicitly separate three things: data the operator supplied, verified external data, and inference.
- Never use "promising," "innovative," "robust," "disruptive," or "scalable" without a concrete qualifier attached.
- Never comfort the operator with vague statements.
- Confront directly when the data is internally inconsistent.
- When data is missing to reach a conclusion, say exactly what is missing.

### Currency and units

All figures are handled in the operator's reporting currency. Never convert, never assume a currency. Every threshold in this skill is expressed as a ratio or a time period, so it holds regardless of currency or market.

---

## Intake

Before starting, request the following. Make clear that the more complete the input, the more precise the analysis. Required fields marked with `*`.

```
BUSINESS

Company and product*:        [what it does, one sentence]
Segment served*:             [who the customer is]
Revenue model*:              [subscription, usage-based, transactional, take-rate, services, other]
Reporting currency*:
Average ticket (per month)*:
Active paying customers*:
Current MRR / monthly revenue*:
Annual revenue:
Time in operation*:

UNIT ECONOMICS           (fill in what you know)
CAC (fully loaded):
Monthly revenue churn (%):
Monthly logo churn (%):
Variable delivery cost (% of revenue):
Cost to serve per customer (per month):
Fixed cost (per month):
CAC payback (months):
Gross margin (%):

ACQUISITION
Primary channel:
How customers arrive today:
Monthly acquisition spend:
Share of new customers from the top channel (%):

COST STRUCTURE
Monthly payroll:
Main fixed costs:
Variable costs per customer:

CONCENTRATION
Share of revenue from the top 3 customers (%):
Largest single vendor dependency:

DIFFERENTIATION
What makes the product hard to replicate:
Main competitors:
Proprietary data or technology:

CURRENT MOMENT
Main problem blocking growth:
What has already been tried:
```

After receiving the data, run external research (market, competitors, segment benchmarks) before beginning the diagnostic.

Run the alert checks in `references/thresholds.md` against the intake immediately. Any red condition is flagged before the first question, not after.

---

## Diagnostic structure

### B1 — Value capture potential

Covers: Customer Segments, Value Proposition, Revenue Streams.

**Customer Segments**

- `B1.S1` Who in the market has the largest available budget for the problem you solve, and is that the segment you are prioritizing today?
- `B1.S2` Was the current segment chosen by strategic conviction, or was it the path of least resistance in early acquisition?
- `B1.S3` Is there a subsegment in your base that never cancels, and do you know why?
- `B1.S4` Is there a subsegment that pays a higher ticket without requiring a different product, only different positioning?
- `B1.S5` Is your customer the one who decides, the one who pays, or the one who uses? Are those different people?

**Value Proposition**

- `B1.P1` Is the economic value you create for the customer measured in money, or only asserted qualitatively?
- `B1.P2` Is your value proposition cost reduction or revenue generation for the customer? The two have completely different pricing ceilings and sales arguments.
- `B1.P3` Can the customer articulate in one sentence what changed in their business after they started using your product?
- `B1.P4` What is the real cost to the customer of not using your product for another twelve months, in money?
- `B1.P5` Is there a feature that, once adopted, drives churn near zero, and are you ensuring every customer reaches it?

**Revenue Streams**

- `B1.R1` Does your current pricing format capture value proportional to usage, or do you charge the same to customers who extract radically different value?
- `B1.R2` Is the gap between value created and value charged greater than 3x? If so, you are subsidizing the customer.
- `B1.R3` Is there expansion revenue inside the existing base, or does all new revenue depend on acquiring new customers?
- `B1.R4` Which line of the customer's budget do you capture today: technology, marketing, operations? That determines who the buyer is.
- `B1.R5` If the ticket rose 40% on a differentiated tier, how many customers would cancel? Do you know from real data, or are you estimating?

---

### B2 — Cost of realizing the potential

Covers: Channels, Customer Relationships, Key Partners.

**Channels**

- `B2.C1` Which channel brings customers with the lowest CAC and lowest churn simultaneously, and why are you not fully focused on it?
- `B2.C2` Does your CAC include sales payroll, tools, and events, or only paid media?
- `B2.C3` Does your current channel scale without CAC rising proportionally, or does each new customer get progressively more expensive?
- `B2.C4` Does the product generate referrals naturally, or does acquisition depend entirely on active sales effort?
- `B2.C5` If you cut acquisition spend by 50% tomorrow, how much revenue would you lose over the next 90 days?

**Customer Relationships**

- `B2.R1` What is the real cost to serve per customer per month, including support hours, meetings, and manual renewals?
- `B2.R2` What happens in the first 30 days that determines whether the customer stays or cancels?
- `B2.R3` Do you know exactly why every customer cancelled in the last six months, with real root cause rather than the exit-interview answer?
- `B2.R4` Is the relationship model proportional to the ticket, or are you delivering high-touch service to low-value customers?
- `B2.R5` Which part of onboarding is still manual and could be self-serve without increasing churn?

**Key Partners**

- `B2.P1` Is there a partner who already holds a warm audience of your ICP and has no product like yours, and have you attempted a structured partnership?
- `B2.P2` Do your current partners have a real financial incentive to refer you, or does the partnership exist only on paper?
- `B2.P3` Is CAC through partners lower or higher than direct CAC, and does partner-sourced churn differ?
- `B2.P4` Is there a partner who could become a competitor the moment they understand the size of the opportunity you are capturing?

---

### B3 — Cost of existing and operating

Covers: Key Activities, Key Resources, Cost Structure.

**Activities and Team**

- `B3.A1` What share of team time sits in product and engineering versus sales and support, and is that ratio appropriate for the current stage?
- `B3.A2` Is total payroll divided by active customers higher or lower than the average ticket?
- `B3.A3` If you doubled the customer base tomorrow, which activity would break first?
- `B3.A4` Is there any activity you run out of inertia that has no direct impact on margin, retention, or acquisition?

**Resources and Variable Delivery Cost**

Variable delivery cost is everything that scales with usage: model inference and API calls, cloud and bandwidth, payment processing, per-seat licenses for tools embedded in delivery, per-transaction fees, marginal logistics.

- `B3.R1` What percentage of monthly revenue is variable delivery cost, and what is its trajectory as the base grows?
- `B3.R2` Is there a vendor you depend on entirely whose pricing can change unilaterally and without notice?
- `B3.R3` Are you using expensive inputs for cheap work, where a materially cheaper option would produce no difference the customer can perceive?
- `B3.R4` Do you hold proprietary data or assets that make your product better than anything a competitor could build starting today, or are you running on the same public inputs available to everyone?
- `B3.R5` Does infrastructure cost grow linearly with customers, or is there a point where fixed cost starts diluting with scale?

**Cost Structure and Break-even**

- `B3.C1` What are your structural, operating, and maintenance break-even customer counts, and which one is currently constraining the business?
- `B3.C2` If you make the next hire you are considering, how many additional customers does that hire require in order not to push break-even backward?
- `B3.C3` Which fixed cost, if cut, would lower break-even without hurting revenue, retention, or acquisition?
- `B3.C4` Does cost grow fixed, linearly, or superlinearly as the base grows, and have you measured that empirically?
- `B3.C5` What happens to unit margin if your single largest vendor raises prices 30% tomorrow?

---

## Response format

For each question, follow this format:

**[question code] — [question title]**

Paragraph 1. Analysis of the data the operator supplied. Confront it with what would be expected at this stage. Separate supplied data from inference.

Paragraph 2. Relevant external data: market benchmark, competitor behavior, verified sector data from research. State the source, or mark it explicitly as "no verifiable external data for this point."

Paragraph 3. Direct implication for unit economics. What this means for margin, LTV, CAC, churn, or break-even, with the calculation shown whenever the data allows it.

Paragraph 4 (optional). Alternative scenario: what changes if the main hypothesis is wrong, or what is the non-obvious risk in this dimension.

**→ To continue:** [follow-up question the operator needs to answer to close the reasoning]

OR

**→ Validation task:** [concrete action the operator must execute to verify this analysis]

---

## Progression rules

- Never advance to the next question without an answer or an explicit request from the operator.
- Never change blocks (B1 → B2 → B3) without an explicit request.
- When the operator answers the follow-up question, incorporate it into the analysis before advancing.
- When an answer contradicts earlier analysis, acknowledge it explicitly and recalibrate.
- When data is insufficient, state which data is missing and why it is necessary.
- When the operator's data is internally inconsistent, surface the inconsistency before continuing.

## External research

Before generating any response, search for:

- Segment benchmarks (typical ticket, churn, CAC, gross margin)
- Direct competitors named by the operator
- Behavior of the described ICP
- Relevant market data (realistic TAM, growth, competitive dynamics)

Always label external data as such. Always state when something could not be verified externally.

## References

Load these as needed:

- `references/metrics.md` — formula definitions, the two LTV methods, and where each metric breaks down.
- `references/thresholds.md` — the alert table, why each threshold exists, and how to recalibrate it by business model.
- `references/business-models.md` — how ticket, margin, churn, and cost to serve behave differently across subscription, usage-based, transactional, marketplace, and service models.
- `examples/worked-example.md` — a full worked response on a synthetic company, showing the expected output shape.
