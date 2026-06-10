# Why AI Projects Don't Get Used

Most AI project discussions focus on building.

This repository studies something else:

```text
Why do so many AI projects get built but never become something people repeatedly use?
```

This is an ongoing, case-based research project about AI product failure analysis.

It looks at AI products, GPTs, agents, tools, and open source projects through one practical question:

```text
What prevents repeated use?
```

## What This Is

- An independent research project
- A growing case library
- A set of diagnosis frameworks
- A place to test failure modes against public examples
- An invitation for counterexamples

## What This Is Not

- Not a definitive theory
- Not a startup course
- Not a prompt engineering collection
- Not a product teardown service
- Not a claim about the real intentions of project authors

The GitHub autopsies are external observations based only on public repository information.

## Current Dataset

| Source | Count | Notes |
| --- | ---: | --- |
| Public success / strong opportunity cases | 4 | Canva GPT, Consensus, Scholar AI, Apify Skills |
| GitHub low-attention AI projects | 15 | Public README-based autopsies |
| Personal/private cases | 0 public | Kept out to avoid author bias |

GitHub samples are not definitive failures. They are low-attention public examples used to test the framework.

## Core Lens

The current framework looks for four common failure modes:

1. The user does not really exist
2. The input cost is too high
3. The output is too far from the real result
4. ChatGPT can directly replace the product

It also tracks survival paths:

1. Narrow the user
2. Lower the input cost
3. Turn output into a result
4. Connect to real systems
5. Upgrade from tool to workflow
6. Move from generation to execution

## Diagnosis Flow

```text
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
```

The key question is not:

```text
Can AI do this?
```

The key question is:

```text
Why would someone come back to use it again?
```

## Repository Map

```text
framework/
  failure_modes.md
  diagnosis_process.md
  scoring_system_v0_1.md

autopsies/
  README.md
  github_public_batch_01.md
  github_public_batch_02.md
  github_public_batch_03.md

findings/
  public_success_cases.md
  survival_paths.md
  trust_cost_of_execution_ai.md

templates/
  case_study_format.md
  submission_template.md
```

## Start Here

- [Failure modes](framework/failure_modes.md)
- [Diagnosis process](framework/diagnosis_process.md)
- [Scoring system](framework/scoring_system_v0_1.md)
- [GitHub autopsy batch 01](autopsies/github_public_batch_01.md)
- [Survival paths](findings/survival_paths.md)
- [Trust cost of execution AI](findings/trust_cost_of_execution_ai.md)

## Research Status

This project is intentionally unfinished.

Current status:

- Framework: v1
- Diagnosis process: v2
- Scoring system: v0.1
- GitHub public autopsies: 15

The next useful contribution is not a new framework version.

It is a better case, a counterexample, or a sharper failure pattern.

## Contributing

If you built an AI project that did not get sustained use, you can submit it anonymously.

Use:

- [Submission template](templates/submission_template.md)
- [Case study format](templates/case_study_format.md)
- [Contributing guide](CONTRIBUTING.md)

Counterexamples are welcome.

If a case contradicts the current framework, that is useful data.

