# Public Repository Map

This document defines the role of Cyrilla's public GitHub repositories and the maintenance rules used to keep the account readable over time.

## 1. Current Product Repositories

These repositories represent products that are current, strategically important, or still useful as independent systems.

| Repository | Role | Status |
| --- | --- | --- |
| [`sideglance`](https://github.com/cyrilla-mist/sideglance) | Internet context intelligence; Decode is the current release and Radar / Archive are the long-term product direction | Current product |
| [`statewake`](https://github.com/cyrilla-mist/statewake) | Interrupted-work recovery agent built around Validate before Recover | Completed deployed project; post-hackathon |
| [`nexus-ai`](https://github.com/cyrilla-mist/nexus-ai) | Canonical long-term Nexus Atlas repository | Long-term experimental product |
| [`english-radar`](https://github.com/cyrilla-mist/english-radar) | Local-first real-internet-English learning system; foundation for future Sideglance Radar | Maintenance |
| [`verity`](https://github.com/cyrilla-mist/verity) | AI-assisted project-material quality and review tool | Independent product |

## 2. Portfolio and Small Web Work

[`portfolio`](https://github.com/cyrilla-mist/portfolio) is the public presentation hub.

Small browser utilities should normally live inside the Portfolio repository rather than becoming new repositories.

```text
portfolio/
├── index.html
├── lab/
│   ├── prompt-builder/
│   ├── ai-tools/
│   ├── color-palette/
│   └── gradient-generator/
├── experiments/
└── docs/
```

### Web Lab rule

Use `portfolio/lab/` when a project is primarily:

- one or a few static pages;
- a small HTML / CSS / JavaScript utility;
- a UI experiment;
- a generator, reference tool, or personal utility;
- not expected to need an independent issue tracker, release history, backend, or architecture documentation.

A small experiment should not become a separate repository only to make the repository count larger.

## 3. Earlier Experiments

| Repository | Role | Status |
| --- | --- | --- |
| [`inkraft`](https://github.com/cyrilla-mist/inkraft) | Earlier Chinese academic-writing AI assistant experiment | Preserved; minimal maintenance |
| [`prism-ai`](https://github.com/cyrilla-mist/prism-ai) | Earlier multi-role AI review experiment | Preserved; minimal maintenance |

Their code and Git history remain in the standalone repositories for now. The Portfolio `experiments/` directory acts as the index for these projects until a safe physical repository migration is intentionally performed.

## 4. Competition and Supporting Repositories

These repositories exist for reproducibility, evidence, or competition history. They should not be presented as separate current products.

| Repository | Role | Status |
| --- | --- | --- |
| [`nexus-atlas-datahub-2026`](https://github.com/cyrilla-mist/nexus-atlas-datahub-2026) | Frozen DataHub Hackathon 2026 Nexus Atlas submission | Competition snapshot |
| [`statewake-demo-project`](https://github.com/cyrilla-mist/statewake-demo-project) | External project-evidence fixture used by the STATEWAKE demo | Supporting repository |

### Competition snapshot rule

Create a separate competition repository only when the submission needs to remain reproducible independently from the long-term product repository.

A competition snapshot should:

1. say clearly that it is a competition snapshot;
2. link to the canonical long-term repository when one exists;
3. preserve submission links and evidence;
4. stop presenting itself as active development after submission;
5. avoid competing with the canonical repository for Portfolio prominence.

## 5. When a Project Deserves Its Own Repository

A new independent repository should normally satisfy at least one of these conditions:

- it has a distinct product identity and roadmap;
- it has meaningful backend / infrastructure / model integration;
- it has tests, deployment, or architecture worth maintaining independently;
- it needs its own release history or reproducibility boundary;
- it is a competition submission that must remain frozen as evidence;
- it is a supporting repository required by another product's architecture or demo.

Otherwise, prefer `portfolio/lab/` or `portfolio/experiments/`.

## 6. README Standard

Public repositories should use English as the default README language.

Recommended structure:

```text
Project name
One-sentence product definition
Status / canonical-repository note when needed
Live demo / important links
Problem or overview
Core experience / features
How it works / architecture
Technology
Local development
Current boundaries / limitations
Status / direction
License when applicable
```

Long technical repositories may be detailed. Small experiments should keep their README short.

Chinese documentation can remain in `docs/` when it is useful to the product or original audience.

## 7. Status Labels

Use a small set of consistent status concepts:

- **Current product** — active or strategically current product work
- **Maintenance** — usable product with no current feature-expansion priority
- **Long-term experimental product** — canonical product codebase that remains exploratory
- **Completed deployed project** — completed product snapshot that remains publicly usable
- **Earlier experiment** — preserved project with minimal maintenance
- **Competition snapshot** — frozen submitted build
- **Supporting repository** — repository that exists to support another product or demo

Avoid ambiguous wording such as `pending`, `candidate`, `not frozen`, or `coming soon` after those states are no longer true.

## 8. Maintenance Checklist

When reviewing the GitHub account:

- confirm the README describes the repository's current role;
- remove expired submission language;
- verify live links and canonical-repository links;
- keep small utilities consolidated;
- avoid duplicate copies of the same product without explicit snapshot labeling;
- keep public README language consistent;
- update Portfolio cards when product roles change;
- review GitHub About descriptions, homepage URLs, topics, default branches, and pinned repositories separately because those are repository/profile settings rather than files.

Last reorganized: September 2026.
