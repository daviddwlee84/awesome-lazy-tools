# Yazi

[Back to the list](../../README.md) · [Research method](../research-method.md)

- **Upstream:** [sxyazi/yazi](https://github.com/sxyazi/yazi)
- **Category:** File management TUI
- **Reviewed:** 2026-09-21
- **Inspected revision:** [`112aeceac8e70c73d7a752976d9af7fc83f148bd`](https://github.com/sxyazi/yazi/tree/112aeceac8e70c73d7a752976d9af7fc83f148bd) (`main`)
- **Repository state:** not archived at review time.

## What it does

Yazi is an asynchronous terminal file manager with previews, background task management, plugins, tabs, and integrations such as fzf and zoxide. The inspected README still labels it **public beta**, while saying it can be used as a daily driver. [Upstream README](https://github.com/sxyazi/yazi/blob/112aeceac8e70c73d7a752976d9af7fc83f148bd/README.md).

## Why it fits this list

It combines navigation, preview, selection, and file actions while keeping the surrounding directory context visible. Its task progress and cancellation are useful references for work that must continue without freezing navigation.

**UX tradeoff:** Extensibility brings a configuration and plugin surface beyond the base file browser. The README describes several image protocols and optional integrations; the review does not assume every terminal or plugin setup has identical preview behavior. [Features](https://github.com/sxyazi/yazi/blob/112aeceac8e70c73d7a752976d9af7fc83f148bd/README.md).

These are source-backed design observations, not claims of hands-on testing.

## Agentic development

**Evidence status: Documented use.** Status describes the inspected public record, not project quality or the proportion of AI-written code.

### Implementation evidence

[#3038](https://github.com/sxyazi/yazi/pull/3038) explicitly states that a Kitty graphics/tmux fix was developed with Claude Code assistance; it was merged. [#3984](https://github.com/sxyazi/yazi/pull/3984) later discloses Codex use to inspect a preview-cache code path and draft a regression test. These disclosures describe different assistance scopes and should not both be rewritten as “the entire patch was AI-generated.”

### Guidance and contribution policy

The current [`AGENTS.md`](https://github.com/sxyazi/yazi/blob/112aeceac8e70c73d7a752976d9af7fc83f148bd/AGENTS.md) records Rust/Lua style, architecture, validation, and boundaries on public actions. It tells agents not to create issues, PRs, or comments and not to add/change tests unless requested. Its initial addition is visible in [`2c3f174`](https://github.com/sxyazi/yazi/commit/2c3f174eb5ed9536aa090f2056c6af1ef30323c5).

Yazi permits AI-assisted code under disclosure and human understanding/review/testing requirements, but requires issue, PR, discussion, and commit descriptions to be human-authored. The contributor must name the model and scope of assistance; the PR template excludes AI bots opening PRs. [Policy](https://github.com/sxyazi/yazi/blob/112aeceac8e70c73d7a752976d9af7fc83f148bd/CONTRIBUTING.md#ai-policy); [PR template](https://github.com/sxyazi/yazi/blob/112aeceac8e70c73d7a752976d9af7fc83f148bd/.github/pull_request_template.md).

### Bots and automation

No AI-specific checked-in workflow was established by the workflow scan. The presence of agent guidance and accepted contributions does not establish automated PR submission; the current template explicitly restricts that behavior.

## Public milestones

| Date | Evidence type | Public record |
| --- | --- | --- |
| 2025-09-04 | Disclosed implementation merged | [#3038](https://github.com/sxyazi/yazi/pull/3038), opened August 6 by `yuvals1`, merged at 13:59:06Z; Claude Code assistance is stated in the body. |
| 2026-07-25 | Guidance added in a commit | [`2c3f174`](https://github.com/sxyazi/yazi/commit/2c3f174eb5ed9536aa090f2056c6af1ef30323c5) adds `AGENTS.md`; author and committer timestamps are 03:39:19Z. |

Dates are UTC. PR creation, PR merge, commit author time, and commit committer time are different events. The entries establish evidence found by this review, not first-ever use.


## Review scope

- Inspected the default-branch tree, README, repository agent guidance, contribution files, PR template, and 10 checked-in GitHub workflow files at the pinned revision.
- Instruction/contribution files read: [`.github/pull_request_template.md`](https://github.com/sxyazi/yazi/blob/112aeceac8e70c73d7a752976d9af7fc83f148bd/.github/pull_request_template.md), [`AGENTS.md`](https://github.com/sxyazi/yazi/blob/112aeceac8e70c73d7a752976d9af7fc83f148bd/AGENTS.md), [`CONTRIBUTING.md`](https://github.com/sxyazi/yazi/blob/112aeceac8e70c73d7a752976d9af7fc83f148bd/CONTRIBUTING.md)
- Searched merged PRs separately for `Claude`, `Codex`, and `"AI-generated"`, scoped to `repo:sxyazi/yazi`; inspected up to 10 results per query, ordered by creation date ascending.
- Searched repository commit messages for `"Claude"`; inspected up to 10 results ordered by author date ascending. These are search-index results, not a complete provenance audit.
- Followed the primary PR, commit, discussion, or path-history links cited below when a candidate needed verification. Search hits mentioning an AI product, quoting another repository, or repeating policy text were not treated as disclosures.
- The record is based on public upstream artifacts. No runtime UX evaluation or upstream test suite was run for this dossier.

## Unknowns and limits

The guidance date is later than the observed assisted contribution and cannot be used as the start of AI use. No implementation percentage or universal model preference was established. Test-generation evidence, contributor prose requirements, and core-code authorship must remain separate.

Private usage, undisclosed assistance, work outside the checked paths, and the share of code produced by a model remain unknown. An instruction file records intended behavior; it does not show that every contributor follows it.

[Back to the list](../../README.md)
