# Worked example

A full diagnostic opening on a synthetic company, showing the expected shape of the output.

**Everything below is invented.** The company does not exist, the figures are constructed to be internally consistent for illustration, and the external benchmarks shown are placeholders standing in for real research. In an actual run, paragraph 2 of every response comes from live search and is sourced.

Currency is written as `$` throughout and means nothing more than "one unit of the operator's reporting currency."

---

## Intake as submitted

```
BUSINESS
Company and product:      Scheduling and reminder software for veterinary clinics
Segment served:           Independent clinics, 2 to 6 vets
Revenue model:            Subscription
Reporting currency:       $
Average ticket:           $340 / month
Active paying customers:  210
Current MRR:              $71,400
Time in operation:        3 years

UNIT ECONOMICS
CAC (fully loaded):           $3,286
Monthly logo churn:           2.0%
Monthly revenue churn:        2.8%
Variable delivery cost:       11% of revenue ($37 / customer)
Cost to serve:                $34 / customer / month (1.2 support hours at $28 loaded)
Gross margin:                 79%

ACQUISITION
Primary channel:              Regional veterinary association partnership
Monthly acquisition spend:    $46,000
New customers per month:      14
Share from top channel:       78%

COST STRUCTURE
Monthly payroll:              $52,000
Fixed cost (excl. cost to serve): $58,000

CONCENTRATION
Top 3 customers:              9% of revenue
Largest vendor:               Cloud provider, 71% of variable delivery cost
```

---

## Pre-flight alert check

Derived before any question is asked:

- Contribution margin per customer: `340 − 37 − 34 = $269` (79% of ticket). Positive, comfortably.
- CAC payback: `3,286 ÷ 269 = 12.2 months`. Inside the workable band, at its upper edge.
- LTV (margin method): `(340 × 0.79) ÷ 0.028 = $9,593`. LTV/CAC = `2.9x`. Below the 3x reference, above the 1.5x red line.
- Payroll per customer: `52,000 ÷ 210 = $248`, against a $340 ticket. Passes.
- Structural break-even: 58,000 ÷ 269 = 216 customers.
The current base of 210 is six customers below structural break-even.

Operating break-even at the current $46,000 monthly acquisition spend:
(58,000 + 46,000) ÷ 269 = 387 customers.

The current base is 177 customers below operating break-even.

These are different questions. The first asks whether the installed customer base can support the operating structure with acquisition paused. The second asks whether the company is profitable while maintaining its current acquisition effort.

- Customer concentration: 9%. Passes.

**🟡 Single channel > 70% of new customers.** 78% of new customers arrive through one association relationship. This is the only alert firing, and it is the most consequential fact in the intake: the business is roughly one renegotiation away from losing four fifths of its acquisition.

**🟡 Largest vendor > 60% of variable delivery cost.** The cloud provider accounts for 71%. Lower priority given that variable cost is only 11% of revenue, so a 30% price increase moves gross margin by about 2.3 points. Noted, not urgent.

Everything else clears. The installed base is close to covering the operating structure before acquisition spend, but the company is materially below operating break-even at its current growth spend. The distinction matters: the core economics may be close to self-sustaining while the current growth strategy still consumes substantial cash. The diagnostic should spend its time on B2 before B1.

---

## B2.C1 — Which channel brings the lowest CAC and lowest churn simultaneously, and why are you not fully focused on it?

You are already fully focused on it, which is the problem rather than the achievement it looks like. 78% of new customers come through the association, and you have not reported CAC or churn split by channel, so the claim that this is your best channel is currently an inference from volume rather than a measurement. Volume and efficiency are different things, and an exclusive partnership produces volume for reasons that have nothing to do with efficiency. What the data does support: blended CAC of $3,286 against a $340 ticket, which is 9.7 months of gross revenue and 12.2 months of contribution margin to recover.

*[In a real run, this paragraph would carry sourced benchmarks on partnership-led acquisition in vertical SaaS. Treat the following as a placeholder for that research.]* Comparable vertical software businesses selling into fragmented professional practices typically show partnership-sourced CAC 30–50% below direct outbound, with the caveat that the discount is rent, not a moat: it persists exactly as long as the partner has no reason to charge for it.

The implication for unit economics is that your 2.9x LTV/CAC is not a property of the business, it is a property of the contract. Model the downside explicitly: if the association raises its commission or opens the channel to a competitor, and blended CAC rises 40% to $4,600, payback moves from 12.2 to 17.1 months and LTV/CAC falls to 2.1x. You are still above the red line, but you are six customers from break-even with a 17-month payback, which means growth would begin consuming cash faster than the base generates it. The channel risk is not that acquisition stops. It is that acquisition gets expensive at precisely the moment you have no second channel to switch to.

The non-obvious risk sits on the retention side. If association-sourced customers churn lower than direct customers, and you do not know whether they do, then your 2.8% churn is a blended figure that would deteriorate the moment channel mix shifts. That would compound with the CAC increase rather than offsetting it.

**→ Validation task:** Split the last 24 months of cohorts by acquisition source. For each source, calculate fully loaded CAC and 12-month retention separately. Bring back the two-by-two. Until that exists, every channel decision you make is being made on volume data.

---

## B3.C2 — If you make the next hire, how many additional customers does that hire require in order not to push break-even backward?

You are at 210 customers against a break-even of 216.
At 210 customers, the installed base generates $56,490 in monthly contribution margin.
Against $58,000 of operating fixed cost, the core operation is only $1,510 below structural break-even.
But the company is also spending $46,000 per month on acquisition. At the current acquisition level, monthly operating result before other excluded items is approximately -$47,510.
This means the company is close to structural break-even but far from operating break-even. Those are fundamentally different states.

On the current trajectory you cross break-even inside a month. That timing is what makes the next hiring decision unusually consequential: a hire made now does not slow profitability, it postpones it, and the postponement is measured precisely.

*[Placeholder for sourced compensation benchmarks in the relevant market.]* Assume a fully loaded monthly cost of $7,000 for a mid-level support or sales hire, inclusive of employer costs, tooling, and equipment.

The arithmetic: `7,000 ÷ 269 = 26 additional customers` required for that single hire to be neutral. At a net 8 per month, that hire pushes break-even out by roughly three and a quarter months. That is the actual price of the decision, and it is the form in which it should be presented to whoever is making it. The comparison that matters is not "can we afford this person" but "does this person produce more than 26 customers of value, directly or by unblocking something." A support hire that cuts cost to serve from $34 to $22 per customer, for instance, raises contribution margin to $281 and lowers break-even to 207, which pays for a meaningful share of itself and changes the answer.

Worth testing the reverse case as well. If the hire is in sales and raises net acquisition from 8 to 12 per month, break-even moves out three months but is then crossed with a steeper slope, and total cash consumed may be lower than the delay suggests. That is a defensible trade. The version that is not defensible is a hire justified by workload rather than by either of these two mechanisms.

**→ To continue:** Which role is the hire, and which of the two mechanisms is it supposed to move: contribution margin, or net acquisition rate? If the honest answer is neither, that is the finding.
