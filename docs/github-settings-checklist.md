# GitHub Settings Checklist

Some important GitHub presentation settings live outside the repository files. The current connector can inspect them but cannot edit them directly, so this file records the intended values for manual cleanup.

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

## Branch Cleanup Settings

### `sideglance`

Only one branch exists (`master`). If standardizing to `main`, change the GitHub default branch and any Pages / workflow references together. Do not create a second long-lived branch without changing the default.

### `english-radar`

The repository currently has many historical release and Radar migration branches.

Use [`SIDEGLANCE_RADAR_MIGRATION_ASSETS.md`](https://github.com/cyrilla-mist/english-radar/blob/main/docs/SIDEGLANCE_RADAR_MIGRATION_ASSETS.md) before deleting branches.

Known migration branches with unique assets must be preserved. Historical branches with `ahead_by=0` can be deleted after verification.

### `nexus-ai`

The repository accumulated many development branches. Use [`BRANCH_CLEANUP_AUDIT_2026-09-17.md`](https://github.com/cyrilla-mist/nexus-ai/blob/main/docs/BRANCH_CLEANUP_AUDIT_2026-09-17.md) as the cleanup record.

At least one branch, `agent/deepseek-project-atlas`, contains confirmed unique work and must not be bulk-deleted.

### `inkraft`

`master` is a stale historical branch with `ahead_by=0` and is behind `main`. It is a safe manual deletion candidate after a final UI check.

## Repository Settings Hygiene

For active repositories, consider enabling **Automatically delete head branches** after merged pull requests. This prevents the kind of branch accumulation currently visible in Nexus Atlas and English Radar.

Before enabling it on repositories that use long-lived migration branches, confirm those branches are not being merged-and-reused intentionally.

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
