# Business model variants

The three blocks hold for every model. What changes is where the ticket comes from, where margin leaks, and which thresholds need recalibration. Identify the model from the intake before starting, and say which one you are assuming.

---

## Subscription

**Ticket.** Contracted monthly fee, stable and predictable. Average ticket is meaningful.

**Where margin leaks.** Cost to serve. The fee is fixed while support consumption is not, so heavy accounts silently subsidize nothing and light accounts subsidize everything. A single-fee model with high usage variance is a pricing failure that presents as a support problem.

**Retention shape.** Churn concentrates in the first 90 days. Period churn understates the problem during growth; use cohort curves.

**Margin floor.** Roughly 70% gross margin for software delivery. Below 55%, the business is operating like a service company under a software label.

**Priority questions.** `B1.R1` (does pricing track value), `B2.R1` (real cost to serve), `B2.R4` (touch model versus ticket).

---

## Usage-based

**Ticket.** Varies per customer per month. A single average hides the distribution. Report median plus interquartile range, and separate base consumption from expansion.

**Where margin leaks.** The gap between the pricing unit and the cost unit. When you charge per seat but pay per call, or charge per record but pay per compute-second, margin drifts with customer behavior rather than with your decisions.

**Retention shape.** Logo churn understates risk because accounts shrink before they leave. Revenue churn is the operative metric.

**Margin floor.** Depends entirely on the pricing-to-cost unit alignment. Test margin at the account level rather than in aggregate: healthy average margin routinely conceals a set of accounts served below cost.

**Priority questions.** `B3.R1` (variable cost trajectory), `B3.R3` (expensive inputs on cheap work), `B1.R1` (pricing unit versus value unit).

---

## Transactional and marketplace

**Ticket.** Take rate × gross transaction volume. Two independent variables, and they usually move in opposite directions: raising take rate suppresses volume.

**Where margin leaks.** Payment processing, fraud and chargebacks, and the subsidy applied to whichever side of the market is short. Marketplace subsidies are frequently accounted as marketing rather than as cost of revenue, which flatters gross margin.

**Retention shape.** Measure repeat rate and cohort GMV retention, not logo churn. Users rarely cancel, they simply stop transacting, and a dormant account counts as retained until someone checks.

**Margin floor.** Roughly 40% net of processing and subsidy. Below 25%, defensibility of the take rate is the central question, not growth.

**Priority questions.** `B1.R2` (value created versus captured), `B2.P4` (partner becoming competitor, and disintermediation generally), `B1.R4` (which side actually pays).

---

## Services and consulting

**Ticket.** Project fee or retainer. Margin is a function of utilization and scope discipline, not of the price list.

**Where margin leaks.** Unbilled scope, bench time, and senior people doing junior work. Model margin per delivery hour before modeling margin per customer, because the customer-level number is downstream of the hour-level one.

**Retention shape.** Renewal rate on retainers, repeat rate on projects. Churn is often invisible: the client does not cancel, they simply do not commission the next project.

**Margin floor.** Roughly 30% after fully loaded delivery cost. Below 20%, the model is selling hours at cost and funding itself from float.

**Priority questions.** `B3.A1` (time allocation), `B3.A2` (payroll per customer), `B2.R4` (touch model versus ticket).

**Threshold note.** The payroll-per-customer red alert is expected to fire here and is not automatically a finding. Delivery payroll belongs in cost to serve, not in fixed cost, before the test is run.

---

## Hardware with a recurring layer

**Ticket.** Split into one-time equipment revenue and recurring service revenue. Never blend them. The one-time component makes growth look repeatable when it is not.

**Where margin leaks.** Warranty, replacement, and reverse logistics, all of which arrive twelve to twenty-four months after the sale that recorded the revenue.

**Retention shape.** Retention is bounded by hardware lifecycle. Churn spikes at replacement, and the replacement decision is a fresh purchase decision.

**Margin floor.** Negative or thin on hardware, high on the recurring layer. The consolidated number is meaningless. Diagnose each stream separately and then test whether the recurring stream alone clears break-even.

**Priority questions.** `B3.C4` (cost growth shape), `B1.R3` (expansion inside the base), `B3.C1` (break-even on the recurring stream alone).

---

## Choosing when the model is mixed

Most real businesses are two of these at once. Rules for handling it:

1. Diagnose each revenue stream separately through B1. Blended tickets across models produce numbers that describe no actual customer.
2. Consolidate at B3. Fixed cost and break-even are shared regardless of how many streams exist.
3. When one stream exceeds 70% of revenue, treat it as the primary model and note the second as a concentration or distraction question rather than a parallel diagnostic.
4. When streams are near parity, the sharpest question is usually whether both should exist, and it belongs in `B3.A4`.
