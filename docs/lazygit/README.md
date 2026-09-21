# Lazygit

[Back to the list](../../README.md) · [Research method](../research-method.md)

- **Upstream:** [jesseduffield/lazygit](https://github.com/jesseduffield/lazygit)
- **Category:** Git workflow TUI
- **Reviewed:** 2026-09-21
- **Inspected revision:** [`f8499e3b490b843d74e3c3b7b9897cd6d8e57c03`](https://github.com/jesseduffield/lazygit/tree/f8499e3b490b843d74e3c3b7b9897cd6d8e57c03) (`master`)
- **Repository state:** not archived at review time.

## What it does

Lazygit presents Git state and operations through panels for files, branches, commits, and related objects. Its documented workflows include line-level staging, interactive rebase, cherry-picking, and inspecting changes before acting. [Upstream README](https://github.com/jesseduffield/lazygit/blob/f8499e3b490b843d74e3c3b7b9897cd6d8e57c03/README.md).

## Why it fits this list

It makes a selected Git object, its state, and relevant operations visible together. The design reduces the need to remember command sequences while retaining Git's underlying concepts. This is a principal reference for the list's interpretation of “lazy.”

**UX tradeoff:** discovery does not remove Git's scope and history semantics. A file, hunk, directory, and commit can be different operation targets; an interface needs to make those distinctions visible. The upstream's descriptions of staging, patch manipulation, and rebasing provide concrete material for studying that design problem. [Features](https://github.com/jesseduffield/lazygit/blob/f8499e3b490b843d74e3c3b7b9897cd6d8e57c03/README.md#features).

These are source-backed design observations. This dossier did not run a comparative usability test or the upstream test suite.

## Agentic development

**Evidence status: Documented use.** The public record includes an explicit maintainer disclosure, a merged implementation, and detailed repository guidance. It does not identify the first private use, the share of AI-written code, or a single date when the entire project became “agentic.”

### Three distinct public events

| Artifact | Opened / accepted | What the evidence actually establishes |
| --- | --- | --- |
| [PR #4843](https://github.com/jesseduffield/lazygit/pull/4843), by `plinde` | Opened 2025-08-22 13:03:11Z; self-closed at 13:12:25Z; never merged | An external proposal to add `CLAUDE.md` and a panel-toggle feature explicitly says it was generated with Claude Code. The author closed it; no reviewer rejection was established. |
| [PR #5273](https://github.com/jesseduffield/lazygit/pull/5273), by `jesseduffield` | Opened 2026-02-07 07:10:16Z; merged by `stefanhaller` on 2026-03-07 19:06:36Z | The body attributes the entire PR to Opus 4.6, while describing the author's own review and local testing. This is an explicit, accepted implementation disclosure. |
| [PR #5581](https://github.com/jesseduffield/lazygit/pull/5581), by `stefanhaller` | Opened 2026-05-04 12:18:41Z; merged by the same maintainer at 12:21:17Z | Adds `AGENTS.md` to the main branch. Its empty PR body and ordinary commit message do not disclose AI authorship of the guidance itself. |

For #5273, the body includes the short statement “opus 4.6 wrote this entire PR.” That is a contributor disclosure, not an independently measured authorship percentage. Stefan's [February 21 review](https://github.com/jesseduffield/lazygit/pull/5273#pullrequestreview-3835401874) supplies separate evidence of human review before merge.

The API also returned a non-null test `merge_commit_sha` for unmerged #4843. This study uses `merged_at`, not the mere presence of a SHA, to establish acceptance.

### When AGENTS.md first appeared

The first commit touching the current path is [`9a2891818ee8e98d935f841d051a5e6387ba447a`](https://github.com/jesseduffield/lazygit/commit/9a2891818ee8e98d935f841d051a5e6387ba447a). Its diff marks `AGENTS.md` as **added**.

| Date field | UTC timestamp | Meaning |
| --- | --- | --- |
| Commit author | 2026-04-19 09:29:14Z | Authorship timestamp recorded by Git, naming Stefan Haller. |
| Commit committer | 2026-05-04 12:16:54Z | Timestamp on the inspected commit object, also naming Stefan Haller. |
| PR merged | 2026-05-04 12:21:17Z | GitHub records #5581 entering the target branch. |

Thus **May 4 is the verified main-branch merge date**, while the author's timestamp is earlier. Neither timestamp by itself reveals when the work was first made public or when the maintainer first used an agent.

The original file already addresses autonomous commits, reviewable commit structure, separation of refactors and behavior changes, and demonstrating existing bugs before fixing them. It also forbids agent-created PRs. These are development-process instructions, beyond a formatting checklist. [Initial file](https://github.com/jesseduffield/lazygit/blob/9a2891818ee8e98d935f841d051a5e6387ba447a/AGENTS.md).

### Guidance evolution

The complete API history for the current `AGENTS.md` path returned **20 commits, including its initial addition**. The following are selected milestones, not a reconstruction of every agent session.

| Date | Evidence type | Public record and date qualification |
| --- | --- | --- |
| 2026-05-04 | Guidance merged | [#5581](https://github.com/jesseduffield/lazygit/pull/5581); precise dates are separated above. |
| 2026-05-09 | Harness redirect committed | [`1cab15e`](https://github.com/jesseduffield/lazygit/commit/1cab15eba863f9619c5a98c10fe74d9fdfed4e6d) adds `CLAUDE.md` pointing to `AGENTS.md`; committer time 12:02:42Z, author time May 4 18:54:22Z. This row does not claim a separately verified PR merge time. |
| 2026-06-23 | Collaboration guidance committed | [`7a60f2d`](https://github.com/jesseduffield/lazygit/commit/7a60f2de800396634b06bf8e60ef80fb703b5f6d) asks agents to surface mid-implementation decisions; committer time 12:15:18Z, author time June 14 16:24:51Z. |
| 2026-07-20 | Tooling guidance committed | [`b371411`](https://github.com/jesseduffield/lazygit/commit/b37141156719332fa53f268bce91f33ad34d9ac3) recommends gopls MCP for symbol navigation; committer time 12:23:09Z, author time July 17 20:52:47Z. |
| 2026-08-16 | Attribution guidance committed | [`adf5970`](https://github.com/jesseduffield/lazygit/commit/adf59703acd7f7d3d75a4204f38cb0f4b60d32f2) adds model-naming co-author trailers and a mid-branch fixup rule; committer time 14:45:50Z, author time August 15 18:02:21Z. |

### Current workflow and contribution boundaries

At the inspected revision, [`AGENTS.md`](https://github.com/jesseduffield/lazygit/blob/f8499e3b490b843d74e3c3b7b9897cd6d8e57c03/AGENTS.md) describes a human-reviewed workflow:

- Use repository `just` recipes for generation, formatting, builds, tests, and linting.
- Prefer available gopls MCP tools for type-aware Go questions; use ordinary text search where appropriate and silently fall back if those tools are absent.
- Commit completed logical units; preserve small, reviewable changes and model attribution.
- Keep `fixup!` and `amend!` iterations visible for human review; do not collapse them as a finishing step.
- Surface meaningful unplanned design or scope choices to the human.
- Follow project-specific architecture, testing, translation, and documentation conventions.
- Do not create PRs; human review and publication boundaries remain explicit.

[`CLAUDE.md`](https://github.com/jesseduffield/lazygit/blob/f8499e3b490b843d74e3c3b7b9897cd6d8e57c03/CLAUDE.md) redirects to the canonical guidance. These upstream instructions are research evidence, not rules imported into this awesome repository.

The reviewed [contribution guide](https://github.com/jesseduffield/lazygit/blob/f8499e3b490b843d74e3c3b7b9897cd6d8e57c03/CONTRIBUTING.md) and [PR template](https://github.com/jesseduffield/lazygit/blob/f8499e3b490b843d74e3c3b7b9897cd6d8e57c03/.github/pull_request_template.md) coexist with that agent guidance. Observed acceptance of #5273 does not waive ordinary contribution expectations for someone else's future PR.

### Bots and automation

#5273 includes a [Copilot review](https://github.com/jesseduffield/lazygit/pull/5273#pullrequestreview-3766526889). That is review automation, separately evidenced from the author's implementation disclosure and Stefan's review. Dependency-bot changelogs quoting another project's Codex work were excluded from Lazygit implementation evidence.

The five checked-in workflow files did not establish an additional AI development workflow. Externally configured bots can exist without a matching workflow file, as the observed Copilot review illustrates.

## Review scope

- Pinned and inspected the default-branch tree, README, `AGENTS.md`, `CLAUDE.md`, contribution guide, PR template, and checked-in workflows.
- Read #4843, #5273, and #5581 directly, including PR metadata, relevant commits, #4843's close event, and #5273's review records.
- Retrieved all 20 commits from the current `AGENTS.md` path history and the current `CLAUDE.md` path history; checked the initial addition and cited evolution artifacts.
- Searched merged PRs for `Claude`, `Codex`, and `"AI-generated"`, scoped to `repo:jesseduffield/lazygit`, with at most 10 results per query in creation-date order.
- Searched repository commit messages for `"Claude"`, with at most 10 results in author-date order. A hit or search-result count was not treated as a measured contribution share.
- Treated the supplied ChatGPT discussion as a research lead. Historical claims here depend on the linked upstream artifacts, not the export alone.
- Did not run the software or upstream tests for this dossier, and did not enumerate every AI-attributed commit.

## Unknowns and limits

- **Earliest evidence found is not first-ever use.** Private work, undisclosed assistance, other model names, and older artifacts outside the bounded search remain unknown.
- **#4843 does not establish rejection.** It was self-closed, so no causal claim about maintainer attitudes follows from its unmerged state.
- **Guidance is intended process.** It cannot establish uniform adoption, agent autonomy, or compliance across every contribution.
- **Evolution does not reveal motivation by itself.** A new rule may address experience, but a specific failure-to-rule story needs a statement or discussion establishing that connection.
- **No AI percentage is asserted.** Search windows, model trailers, author timestamps, committer timestamps, and merge dates describe different populations and events.
- **Attribution remains self-reported.** A named model or harness does not independently establish exactly which lines it produced.

[Back to the list](../../README.md)
