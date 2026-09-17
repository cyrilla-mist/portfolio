# GitHub Settings Checklist

Some important GitHub presentation settings live outside repository files. The current connector can inspect them but cannot edit them directly, so this file records the intended values for manual cleanup.

## Profile Pins

Recommended six pinned repositories, in order:

1. `sideglance`
2. `statewake`
3. `nexus-ai`
4. `english-radar`
5. `verity`
6. `portfolio`

Do not use primary pin space for competition snapshots, demo fixtures, or earlier experiments unless there is a temporary reason to showcase one.

## Repository About Settings

### `sideglance`

Current description is already good:

> Context intelligence for the internet — understand what people mean, not just what the words say.

Recommended website:

```text
https://cyrilla-mist.github.io/sideglance/
```

Recommended topics:

```text
context-intelligence
internet-language
pragmatics
ai
llm
cloudflare-workers
typescript
vite
```

Default branch is currently `master`. Rename / migrate to `main` only through GitHub repository settings with deployment references checked at the same time.

### `statewake`

Current About metadata is already in good shape: description, Cloud Run homepage, MIT license, and relevant Google / agent topics are present.

No urgent settings cleanup required.

### `nexus-ai`

Current GitHub description and homepage are blank even though this is a flagship repository.

Recommended description:

> Personal intelligence infrastructure for restoring project context, tracing decisions, and continuing long-running work.

Recommended website:

```text
https://cyrilla-mist.github.io/nexus-ai/atlas.html
```

Recommended topics:

```text
context-engineering
project-continuity
ai-agents
knowledge-management
human-in-the-loop
datahub
javascript
cloudflare-workers
```

Apache-2.0 is already detected from the repository license.

### `english-radar`

Current GitHub description, homepage, and topics are blank.

Recommended description:

> Local-first learning for real internet English through context, tone, usage boundaries, review, and personal mastery.

Recommended website:

```text
https://cyrilla-mist.github.io/english-radar/
```

Recommended topics:

```text
language-learning
english-learning
local-first
spaced-repetition
internet-language
javascript
github-pages
```

The repository currently has no detected license. Choose a license only if public reuse is intentionally allowed; do not add one merely for visual completeness.

### `verity`

Current GitHub description, homepage, and topics are blank.

Recommended description:

> AI-assisted pre-submission review for project materials, evidence coverage, reviewer questions, and revision priorities.

Recommended website:

```text
https://cyrilla-mist.github.io/verity/
```

Recommended topics:

```text
ai-review
project-evaluation
document-analysis
cloudflare-workers
javascript
github-pages
```

The repository currently has no detected license. Treat licensing as a deliberate legal / reuse decision rather than a cosmetic setting.

### `portfolio`

Current GitHub description, homepage, and topics are blank.

Recommended description:

> Cyrilla's selected products, earlier experiments, and lightweight Web Lab.

Recommended website:

```text
https://cyrilla-mist.github.io/portfolio/
```

Recommended topics:

```text
portfolio
web-lab
ai-projects
vanilla-javascript
github-pages
```

### `inkraft`

This is an earlier experiment and should stay visually secondary to the current product repositories.

Recommended description:

> Earlier AI writing experiment for Chinese academic-writing workflows. Maintained minimally.

Recommended website:

```text
https://cyrilla-mist.github.io/inkraft/
```

Recommended topics:

```text
ai-writing
academic-writing
javascript
github-pages
legacy-project
```

Do not pin it. Keep public while it remains useful as development history; archiving is optional rather than urgent because the live demo remains usable.

### `prism-ai`

This is also an earlier experiment and should stay visually secondary.

Recommended description:

> Earlier multi-role AI review experiment for comparing reviewer perspectives and prioritizing revisions.

Recommended website:

```text
https://cyrilla-mist.github.io/prism-ai/
```

Recommended topics:

```text
ai-review
multi-agent
javascript
github-pages
legacy-project
```

Do not pin it. Archiving is optional while the live demo remains intentionally available.

### `nexus-atlas-datahub-2026`

**Current About description is stale** and still says:

> Nexus Atlas — DataHub Hackathon 2026 submission candidate

The README is already frozen as an archived submitted snapshot, so change the About description to:

> Archived Nexus Atlas submission for Build with DataHub: The Agent Hackathon 2026.

Recommended website:

```text
https://cyrilla-mist.github.io/nexus-atlas-datahub-2026/
```

Recommended topics:

```text
hackathon
nexus-atlas
datahub
context-engineering
archived-project
```

Recommended repository setting: **Archive this repository** after confirming the public demo should remain as a historical snapshot. The canonical long-term repository is `nexus-ai`.

### `statewake-demo-project`

This is a controlled evidence fixture, not a second STATEWAKE product.

Recommended description:

> Controlled external project evidence used by the STATEWAKE recovery demo; not the STATEWAKE source repository.

Recommended topics:

```text
statewake
demo-fixture
project-evidence
```

Do not archive while the live STATEWAKE demo depends on its GitHub evidence. Issue #1 is intentionally open as scenario evidence and is documented in the repository README.

## Branch Cleanup Settings

### `sideglance`

Only one branch exists (`master`). If standardizing to `main`, change the GitHub default branch and any Pages / workflow references together. Do not create a second long-lived branch without changing the default.

### `english-radar`

The repository currently has many historical release and Radar migration branches.

Use [`SIDEGLANCE_RADAR_MIGRATION_ASSETS.md`](https://github.com/cyrilla-mist/english-radar/blob/main/docs/SIDEGLANCE_RADAR_MIGRATION_ASSETS.md) before deleting branches.

Known Sideglance Radar migration branches with unique assets must be preserved. In particular, `feat/sideglance-radar-v0.2-signal-v2-foundation` has confirmed commits not present on `main`. Historical release branches with `ahead_by=0` can be deleted after verification.

### `nexus-ai`

The repository accumulated many development branches. Use [`BRANCH_CLEANUP_AUDIT_2026-09-17.md`](https://github.com/cyrilla-mist/nexus-ai/blob/main/docs/BRANCH_CLEANUP_AUDIT_2026-09-17.md) as the cleanup record.

At least one branch, `agent/deepseek-project-atlas`, contains confirmed unique work and must not be bulk-deleted. Verified `ahead_by=0` branches listed in the audit are safe manual cleanup candidates.

### `inkraft`

`master` is a stale historical branch with `ahead_by=0` and is behind `main`. It is a safe manual deletion candidate after a final UI check.

## Actions / CI State

### `nexus-ai`

Historical Phase 4–8 and integration-repair workflows have been consolidated into one long-term `.github/workflows/ci.yml` workflow for `main` and pull requests.

The consolidated workflow runs the full test suite, repository checks, security contracts, Verity continuity / DataHub checks, ingestion dry-run, and diff hygiene. Its first run after consolidation completed successfully.

### `english-radar`

One maintenance workflow remains. No phase-per-release workflow cleanup is currently needed.

### `sideglance`

One GitHub Pages deployment workflow remains. No workflow cleanup is currently needed.

## Repository Settings Hygiene

For active repositories, consider enabling **Automatically delete head branches** after merged pull requests. This prevents the kind of branch accumulation currently visible in Nexus Atlas and English Radar.

Before enabling it on repositories that use long-lived migration branches, confirm those branches are not being merged-and-reused intentionally.

## License Rule

Do not add licenses merely to make repository metadata look complete.

A missing detected license means reuse rights have not been explicitly granted through a recognized repository license. Choose one only when the intended reuse policy is clear.

## Settings Review Cadence

A lightweight review every few months is enough:

- pinned repositories;
- About description;
- website link;
- topics;
- default branch;
- stale branches;
- archived / maintenance status;
- license detection;
- Pages deployment link.

Last reviewed: September 2026.
