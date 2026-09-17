# GitHub Settings Checklist

This file records GitHub presentation and repository settings that live outside normal repository files. The connected GitHub tools can inspect these values but cannot currently edit repository About metadata, archive repositories, change the default branch, delete branches, or manage profile pins directly.

Last reviewed: **September 17, 2026**.

## Profile Pins

Recommended six pinned repositories, in order:

1. `sideglance`
2. `statewake`
3. `nexus-ai`
4. `english-radar`
5. `verity`
6. `portfolio`

Do not use primary pin space for competition snapshots, demo fixtures, or earlier experiments.

## Repository Settings Matrix

| Repository | Role | About state | Homepage | Branch / archive note |
| --- | --- | --- | --- | --- |
| `sideglance` | current product | description good; topics empty | missing | only repo still using `master`; migrate to `main` only with Pages/workflow refs checked |
| `statewake` | completed deployed product | complete | Cloud Run present | no urgent settings cleanup |
| `nexus-ai` | canonical long-term product | description/topics missing | missing | use branch cleanup audit before manual deletion |
| `english-radar` | maintenance / Radar foundation | description/topics missing | missing | 25 non-main branches fully audited; preserve migration assets |
| `verity` | maintained independent capability | description/topics missing | missing | keep independent |
| `portfolio` | public hub / Web Lab | description/topics missing | missing | pin as public entry point |
| `inkraft` | earlier experiment | description/topics missing | blank | stale `master` is safe deletion candidate |
| `prism-ai` | earlier experiment | description/topics missing | blank | keep visually secondary |
| `nexus-atlas-datahub-2026` | competition snapshot | **stale description** | missing | archive after confirming historical Pages demo should remain |
| `statewake-demo-project` | controlled evidence fixture | description/topics missing | not needed | do **not** archive while STATEWAKE uses it as evidence |

## Exact About Values

### `sideglance`

Keep the current description:

> Context intelligence for the internet — understand what people mean, not just what the words say.

Website:

```text
https://cyrilla-mist.github.io/sideglance/
```

Topics:

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

### `statewake`

Already in good shape: description, Cloud Run homepage, MIT license, and Google / agent topics are present.

### `nexus-ai`

Description:

> Personal intelligence infrastructure for restoring project context, tracing decisions, and continuing long-running work.

Website:

```text
https://cyrilla-mist.github.io/nexus-ai/atlas.html
```

Topics:

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

Apache-2.0 is already detected.

### `english-radar`

Description:

> Local-first learning for real internet English through context, tone, usage boundaries, review, and personal mastery.

Website:

```text
https://cyrilla-mist.github.io/english-radar/
```

Topics:

```text
language-learning
english-learning
local-first
spaced-repetition
internet-language
javascript
github-pages
```

No detected license. Add one only if public reuse is intentionally allowed.

### `verity`

Description:

> AI-assisted pre-submission review for project materials, evidence coverage, reviewer questions, and revision priorities.

Website:

```text
https://cyrilla-mist.github.io/verity/
```

Topics:

```text
ai-review
project-evaluation
document-analysis
cloudflare-workers
javascript
github-pages
```

No detected license. Licensing should remain a deliberate reuse decision rather than a cosmetic setting.

### `portfolio`

Description:

> Cyrilla's selected products, earlier experiments, and lightweight Web Lab.

Website:

```text
https://cyrilla-mist.github.io/portfolio/
```

Topics:

```text
portfolio
web-lab
ai-projects
vanilla-javascript
github-pages
```

### `inkraft`

Description:

> Earlier AI writing experiment for Chinese academic-writing workflows. Maintained minimally.

Website:

```text
https://cyrilla-mist.github.io/inkraft/
```

Topics:

```text
ai-writing
academic-writing
javascript
github-pages
legacy-project
```

Do not pin. Archiving is optional while the live demo remains intentionally available.

### `prism-ai`

Description:

> Earlier multi-role AI review experiment for comparing reviewer perspectives and prioritizing revisions.

Website:

```text
https://cyrilla-mist.github.io/prism-ai/
```

Topics:

```text
ai-review
multi-agent
javascript
github-pages
legacy-project
```

Do not pin. Archiving is optional while the live demo remains intentionally available.

### `nexus-atlas-datahub-2026`

Current stale description:

> Nexus Atlas — DataHub Hackathon 2026 submission candidate

Replace with:

> Archived Nexus Atlas submission for Build with DataHub: The Agent Hackathon 2026.

Website:

```text
https://cyrilla-mist.github.io/nexus-atlas-datahub-2026/
```

Topics:

```text
hackathon
nexus-atlas
datahub
context-engineering
archived-project
```

Archive this repository after confirming the historical Pages demo should remain available. The canonical long-term repository is `nexus-ai`.

### `statewake-demo-project`

Description:

> Controlled external project evidence used by the STATEWAKE recovery demo; not the STATEWAKE source repository.

Topics:

```text
statewake
demo-fixture
project-evidence
```

Do not archive while the STATEWAKE demo depends on it. Issue #1 is intentionally open as controlled scenario evidence.

## Branch Cleanup

### `sideglance`

Only one branch exists: `master`.

If standardizing to `main`, change the GitHub default branch and any Pages / workflow references together. Do not create a second long-lived branch without changing the default.

### `english-radar`

Use the complete audit:

[`english-radar/docs/BRANCH_CLEANUP_AUDIT_2026-09-17.md`](https://github.com/cyrilla-mist/english-radar/blob/main/docs/BRANCH_CLEANUP_AUDIT_2026-09-17.md)

Audit result at September 17, 2026:

```text
12 verified safe cleanup candidates (ahead_by = 0)
13 branches requiring preservation / review
```

Every non-`main` branch present at audit time has been classified.

Sideglance Radar branches with unique commits must be preserved until their useful assets have an explicit destination. Product-level migration details remain in [`SIDEGLANCE_RADAR_MIGRATION_ASSETS.md`](https://github.com/cyrilla-mist/english-radar/blob/main/docs/SIDEGLANCE_RADAR_MIGRATION_ASSETS.md).

### `nexus-ai`

Use:

[`nexus-ai/docs/BRANCH_CLEANUP_AUDIT_2026-09-17.md`](https://github.com/cyrilla-mist/nexus-ai/blob/main/docs/BRANCH_CLEANUP_AUDIT_2026-09-17.md)

Verified `ahead_by=0` branches are safe manual deletion candidates. `agent/deepseek-project-atlas` contains confirmed unique work and must not be bulk-deleted.

### `inkraft`

`master` has `ahead_by=0` and is behind `main`; it is a safe manual deletion candidate after a final UI check.

## CI / Actions State

### `nexus-ai`

Historical Phase 4–8 and integration-repair workflows were consolidated into one long-term `Nexus Atlas CI` workflow for `main` and pull requests.

The consolidated workflow validates the full test suite, repository checks, security contracts, Verity continuity / DataHub contracts, ingestion dry-run, and diff hygiene. Post-cleanup runs are green.

### `english-radar`

One `English Radar maintenance checks` workflow remains. It runs on Node 22 and is green after README / workflow-contract cleanup and the branch-audit documentation update.

### `sideglance`

One GitHub Pages deployment workflow remains. No workflow cleanup is currently needed.

## Repository Hygiene Defaults

For ordinary active repositories, consider enabling **Automatically delete head branches** after merged pull requests.

Do not enable a workflow that would accidentally remove intentionally long-lived migration branches without first checking how those branches are used.

Keep these rules:

- do not add licenses merely to make metadata look complete;
- do not archive evidence repositories that an active demo still reads;
- do not delete a branch with `ahead_by > 0` without reviewing its unique work;
- keep competition snapshots clearly separated from canonical long-term repositories;
- review profile pins, About metadata, homepage links, topics, default branches, archived state, and Pages links every few months.
