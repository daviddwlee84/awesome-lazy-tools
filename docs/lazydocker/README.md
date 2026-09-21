# Lazydocker

[Back to the list](../../README.md) · [Research method](../research-method.md)

- **Upstream:** [jesseduffield/lazydocker](https://github.com/jesseduffield/lazydocker)
- **Category:** Docker and Compose workflow TUI
- **Reviewed:** 2026-09-21
- **Inspected revision:** [`7e7aadc2071d58031bf2daafca1fbd4093efc23f`](https://github.com/jesseduffield/lazydocker/tree/7e7aadc2071d58031bf2daafca1fbd4093efc23f) (`master`)
- **Repository state:** not archived at review time.

## What it does

Lazydocker combines container/service status, logs, metrics, and common management actions in one terminal interface. Its stated aim is to reduce remembered command sequences and switching between terminal windows. [Upstream README](https://github.com/jesseduffield/lazydocker/blob/7e7aadc2071d58031bf2daafca1fbd4093efc23f/README.md).

## Why it fits this list

This is a direct example of inspecting a selected resource and acting in the same interface. Logs and metrics help explain the resource’s state before restarting, attaching, or performing another operation.

**UX tradeoff:** The UI depends on Docker/Compose and their accessible resources. Defaults still shape the view: the README says container logs normally cover the last hour, so a short log pane does not establish that no earlier logs exist. [Requirements and log FAQ](https://github.com/jesseduffield/lazydocker/blob/7e7aadc2071d58031bf2daafca1fbd4093efc23f/README.md).

These are source-backed design observations, not claims of hands-on testing.

## Agentic development

**Evidence status: Documented use.** Status describes the inspected public record, not project quality or the proportion of AI-written code.

### Implementation evidence

Jesse Duffield’s [#797](https://github.com/jesseduffield/lazydocker/pull/797) merged a fix restoring project-scoped behavior. One of its commits, [`f5ff116`](https://github.com/jesseduffield/lazydocker/commit/f5ff116af920c2ad8a094c77845f6e32b105f156), explicitly credits Claude Opus 4.7 and describes responding to Copilot review comments. The PR body itself is empty; the attribution is in the commit.

### Guidance and contribution policy

[`CLAUDE.md`](https://github.com/jesseduffield/lazydocker/blob/7e7aadc2071d58031bf2daafca1fbd4093efc23f/CLAUDE.md) provides a narrow build/test instruction: use the vendored Go dependencies, including the gocui fork and Docker SDK. This is much smaller in scope than Lazygit’s collaboration contract.

No AI-specific acceptance or disclosure rule was identified in the inspected contribution guide. Its ordinary process asks contributors to discuss changes with owners first. [Contribution guide](https://github.com/jesseduffield/lazydocker/blob/7e7aadc2071d58031bf2daafca1fbd4093efc23f/CONTRIBUTING.md).

### Bots and automation

The attributed commit refers to Copilot review feedback. That supports a separate review-assistance observation; it is not the basis for the implementation attribution, which comes from its Claude trailer. No additional AI workflow was established by the checked-in workflow scan. [Commit](https://github.com/jesseduffield/lazydocker/commit/f5ff116af920c2ad8a094c77845f6e32b105f156).

## Public milestones

| Date | Evidence type | Public record |
| --- | --- | --- |
| 2026-04-19 | Guidance committed | [`697cd44`](https://github.com/jesseduffield/lazydocker/commit/697cd441aafa2fd3248267c5f1ef1dc36a4726f0) adds Claude guidance; author and committer timestamps are 02:16:43Z. |
| 2026-04-19 | Attributed implementation merged | [#797](https://github.com/jesseduffield/lazydocker/pull/797) opened at 02:19:36Z and merged at 02:50:06Z; the attributed follow-up commit was authored/committed at 02:47:30Z. |

Dates are UTC. PR creation, PR merge, commit author time, and commit committer time are different events. The entries establish evidence found by this review, not first-ever use.


## Review scope

- Inspected the default-branch tree, README, repository agent guidance, contribution files, PR template, and 3 checked-in GitHub workflow files at the pinned revision.
- Instruction/contribution files read: [`CLAUDE.md`](https://github.com/jesseduffield/lazydocker/blob/7e7aadc2071d58031bf2daafca1fbd4093efc23f/CLAUDE.md), [`CONTRIBUTING.md`](https://github.com/jesseduffield/lazydocker/blob/7e7aadc2071d58031bf2daafca1fbd4093efc23f/CONTRIBUTING.md)
- Searched merged PRs separately for `Claude`, `Codex`, and `"AI-generated"`, scoped to `repo:jesseduffield/lazydocker`; inspected up to 10 results per query, ordered by creation date ascending.
- Searched repository commit messages for `"Claude"`; inspected up to 10 results ordered by author date ascending. These are search-index results, not a complete provenance audit.
- Followed the primary PR, commit, discussion, or path-history links cited below when a candidate needed verification. Search hits mentioning an AI product, quoting another repository, or repeating policy text were not treated as disclosures.
- The record is based on public upstream artifacts. No runtime UX evaluation or upstream test suite was run for this dossier.

## Unknowns and limits

The model trailer is self-reported attribution. It does not identify the fraction of the PR written by a model, establish an earlier adoption date, or show that every future contribution follows this workflow.

Private usage, undisclosed assistance, work outside the checked paths, and the share of code produced by a model remain unknown. An instruction file records intended behavior; it does not show that every contributor follows it.

[Back to the list](../../README.md)
