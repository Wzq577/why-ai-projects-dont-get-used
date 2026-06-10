# Why AI Projects Don't Get Used

Every day, people launch AI products.

New GPTs.

New agents.

New copilots.

New AI startups.

Most of them work.

Many of them never get used again.

Not because the technology failed.

Because nobody came back.

---

This repository studies a simple question:

> Why do AI projects get built, but fail to become something people repeatedly use?

Most discussions about AI focus on building.

This project focuses on usage.

Not:

* Can it be built?

But:

* Will people return?
* Will it become part of a workflow?
* Will it survive after the first demo?

---

## The Observation

After reviewing public AI products, GPTs, agents, and open-source projects, the same patterns kept appearing.

Many projects fail because:

* The user is too vague.
* The input cost is too high.
* The output never becomes a real result.
* ChatGPT can already do something close enough.

At the same time, successful projects often:

* Serve a very specific user.
* Connect to real systems.
* Produce a result, not just an output.
* Become part of an existing workflow.
* Move from generation to execution.

This repository is an attempt to document those patterns.

---

## Current Dataset

| Source                             | Count |
| ---------------------------------- | ----- |
| Public success / opportunity cases | 4     |
| GitHub low-attention AI projects   | 15    |
| Personal cases (publicly excluded) | 0     |

Important:

GitHub samples are not definitive failures.

They are low-attention public examples used to test and challenge the framework.

---

## Core Question

The framework eventually converged to one question:

> Why would someone come back and use this again?

Everything else is secondary.

---

## Diagnosis Flow

User

↓

Task

↓

Result

↓

ChatGPT substitutability

↓

Failure mode

↓

Smallest useful improvement

---

## Repository Structure

```text
framework/
  failure_modes.md
  diagnosis_process.md
  scoring_system_v0_1.md

autopsies/
  github_public_batch_01.md
  github_public_batch_02.md
  github_public_batch_03.md

findings/
  survival_paths.md
  trust_cost_of_execution_ai.md
  public_success_cases.md

templates/
  case_study_format.md
  submission_template.md
```

---

## Start Here

If you are new to the project:

1. Read `framework/failure_modes.md`
2. Read `framework/diagnosis_process.md`
3. Read `findings/survival_paths.md`
4. Read `findings/trust_cost_of_execution_ai.md`
5. Explore the GitHub autopsies

---

## Research Status

This project is intentionally unfinished.

Current snapshot:

* Framework: v1
* Diagnosis process: v2
* Scoring system: v0.1
* Public GitHub autopsies: 15

The next useful contribution is probably not a new framework.

It is:

* A better case
* A stronger counterexample
* A sharper failure pattern

---

## Contributing

Built an AI project that nobody kept using?

I would love to hear about it.

Counterexamples are especially welcome.

If a project breaks the framework, that is useful data.

Use:

* `templates/submission_template.md`
* `templates/case_study_format.md`
* `CONTRIBUTING.md`

---

## What This Is Not

This is not:

* A startup course
* A prompt engineering collection
* A product teardown service
* A definitive theory of AI products

The autopsies are external observations based only on public information.

They are hypotheses, not verdicts.
