# Unit Economics Diagnostic

A Claude Skill that runs a progressive unit economics and scalability diagnostic on any business with paying customers.

It is not a calculator and not a template. It is a structured interrogation: it collects your numbers, checks them against a set of failure conditions, and then walks you question by question through where the model leaks. Every response ends with either a question you have to answer or a task you have to go execute. It is designed to make you think, not to reassure you.

[Português](pt-br/SKILL.md)

## What it does

The nine Business Model Canvas blocks, regrouped into the three questions that determine whether a business compounds:

| Block | Question | Covers |
|---|---|---|
| **B1** | How much value can the model capture? | Customer segments, value proposition, revenue streams |
| **B2** | What does it cost to realize that potential? | Channels, customer relationships, partners |
| **B3** | What does it cost to exist and operate? | Key activities, key resources, cost structure |

Before the first question, it runs fourteen automatic checks against your intake data — negative contribution margin, unmeasured churn, payback beyond 18 months, customer concentration, channel concentration, and others — and surfaces anything red before the conversation proceeds.

## What it is not

- Not a benchmark database. External comparisons come from live research at runtime and are labeled as such.
- Not sector-specific. Thresholds are expressed as ratios and time periods, so nothing depends on a currency, a market, or a stage.
- Not a report generator. It runs as a conversation and stops when you stop answering.

## Install

**Claude Code**

```bash
git clone https://github.com/yurigitahy/lean-vc-uniteconomics.git ~/.claude/skills/unit-economics
```

**Claude Desktop and claude.ai**

Zip the repository contents and upload it under Settings → Capabilities → Skills.

**Any other agent**

The skill is plain Markdown with YAML frontmatter. Paste `SKILL.md` into a system prompt and load the files in `references/` when the skill points to them.

## Use

Trigger it by describing the problem, not by naming the skill:

> Our MRR is growing but we still can't hire. Something is wrong with the model.

> Run a unit economics diagnostic on my business.

> Why is CAC payback getting worse while churn stays flat?

It will ask for the intake block first. Fill in what you have. Missing fields are fine — the skill will tell you which gaps prevent which conclusions rather than guessing around them.

## Structure

```
.
├── SKILL.md                        Entry point: rules, intake, question bank, output format
├── references/
│   ├── metrics.md                  Definitions, formulas, and where each metric breaks
│   ├── thresholds.md               Alert table, rationale, and recalibration rules
│   └── business-models.md          Variants: subscription, usage-based, transactional, services, hardware
├── examples/
│   └── worked-example.md           Full diagnostic opening on a synthetic company
└── pt-BR/
    └── SKILL.md                    Portuguese version
```

`SKILL.md` is loaded whenever the skill triggers. The files under `references/` load only when needed, which keeps the working context small enough for the diagnostic to run long without degrading.

## Design principles

**Contribution margin first.** If each customer loses money, nothing else in the diagnostic is worth discussing. That check runs before anything else and gates the rest.

**Fully loaded or nothing.** CAC includes sales payroll, tooling, and events. LTV uses gross margin, never revenue. Cost to serve counts human hours. The most common way unit economics look healthy is by leaving things out.

**Separate data from inference.** Every response labels which parts are the operator's numbers, which are verified external data, and which are the model's reasoning. Confusing the three is how diagnostics become flattery.

**One question at a time.** The skill does not advance until you answer. A diagnostic delivered as a document gets read; a diagnostic delivered as a conversation gets acted on.

**Ratios, not amounts.** Every threshold is a ratio or a time period. The skill works identically in any currency and any market.

## Contributing

Question additions, threshold corrections with stated rationale, and new business-model variants are all welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[CC BY-SA 4.0](LICENSE). Use it, adapt it, run it commercially. Keep the attribution and license derivatives under the same terms.

Built and maintained by [Lean VC](https://github.com/yurigitahy).
