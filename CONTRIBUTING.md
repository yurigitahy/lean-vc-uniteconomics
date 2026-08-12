# Contributing

This skill improves through use. If you ran it on a real business and it missed something, that is the most valuable contribution available.

## What is wanted

**New questions.** A question earns a place if it produces a different decision than the questions already there. Submit it with the code it belongs under, and one sentence on what failure mode it catches.

**Threshold corrections.** Every number in `references/thresholds.md` is a heuristic with a stated rationale. If you have evidence that a threshold is wrong for a class of business, open an issue with the evidence and the class. Do not change a number without changing its rationale.

**Business model variants.** `references/business-models.md` covers subscription, usage-based, transactional, services, and hardware-plus-recurring. Missing models with genuinely different margin mechanics are welcome. Follow the existing shape: ticket, where margin leaks, retention shape, margin floor, priority questions.

**Translations.** Currently English and Portuguese. Translations should carry the full question bank, not a summary.

## What is not wanted

**Real company data.** Every number in this repository is synthetic. Do not submit intake data, transcripts, or figures from an actual business, yours or anyone else's. Examples must be invented and internally consistent.

**Generic startup advice.** If a question can be answered without looking at the operator's numbers, it does not belong here.

**Vocabulary from the banned list.** The skill instructs against "promising," "innovative," "robust," "disruptive," and "scalable" without a concrete qualifier. Contributions should hold themselves to the same rule.

**Scoring, grading, or maturity levels.** The diagnostic deliberately produces findings rather than a score. A score ends the conversation, which is the opposite of the intent.

## Rules for changes to SKILL.md

- Keep it under 500 lines. Content beyond that goes into `references/` with a pointer from the body.
- Every threshold stays a ratio or a time period. No absolute currency amounts anywhere in the skill.
- Imperative voice in instructions.
- The description field in the frontmatter is the trigger mechanism. Changes to it need a note on what phrasing they are meant to catch.

## Process

1. Open an issue describing the change and the failure mode it addresses, before writing it.
2. One concern per pull request.
3. If you change the question bank or thresholds, run the skill on the synthetic company in `examples/worked-example.md` and confirm the pre-flight alerts still resolve correctly.
