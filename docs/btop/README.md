# btop

[Back to the list](../../README.md) · [Research method](../research-method.md)

- **Upstream:** [aristocratos/btop](https://github.com/aristocratos/btop)
- **Category:** System monitoring TUI
- **Reviewed:** 2026-09-21
- **Inspected revision:** [`612e18f5bd598fe987b30d041b39e5d7b3e0794f`](https://github.com/aristocratos/btop/tree/612e18f5bd598fe987b30d041b39e5d7b3e0794f) (`main`)
- **Repository state:** not archived at review time.

## What it does

btop displays processor, memory, disk, network, and process state. The README documents process details, filtering, sorting, tree view, signal sending, and a mouse-accessible menu system. [Upstream README](https://github.com/aristocratos/btop/blob/612e18f5bd598fe987b30d041b39e5d7b3e0794f/README.md).

## Why it fits this list

Its central interaction is monitoring first: notice a change, select the relevant process, inspect details, then act. It fits the list through this shared interaction pattern even though its name does not start with “lazy.”

**UX tradeoff:** A monitor’s graphs summarize state rather than replace detailed diagnosis. btop also exposes process actions, so it is more than a passive chart. Its documented keyboard and mouse controls offer a useful alternative to treating Vim-style keys as mandatory for every workflow. [Features](https://github.com/aristocratos/btop/blob/612e18f5bd598fe987b30d041b39e5d7b3e0794f/README.md#features).

These are source-backed design observations, not claims of hands-on testing.

## Agentic development

**Evidence status: Documented use.** Status describes the inspected public record, not project quality or the proportion of AI-written code.

### Implementation evidence

[#1583](https://github.com/aristocratos/btop/pull/1583) explicitly discloses AI-generated original code with human review and testing, and was merged. [#1690](https://github.com/aristocratos/btop/pull/1690) later describes Claude-assisted crash analysis and a proposed patch, with the contributor explaining the extent of their own review. The first does not name a model; the second does.

### Guidance and contribution policy

No matching coding-agent instruction file was found in the inspected tree. Contribution rules are nevertheless explicit about AI-generated code.

The current rules require `[AI generated]` disclosure when any code is produced through prompting; boilerplate autocomplete is excepted. They reject submissions whose authors do not understand the generated code and explain consequences for nondisclosure. This permits accountable contributions rather than treating model use as sufficient quality evidence. [Contribution policy](https://github.com/aristocratos/btop/blob/612e18f5bd598fe987b30d041b39e5d7b3e0794f/CONTRIBUTING.md#ai-generated-code).

### Bots and automation

No AI-specific workflow was established by the checked-in workflow scan. A disclosure policy is not a review bot, and neither establishes automated development of the whole project.

## Public milestones

| Date | Evidence type | Public record |
| --- | --- | --- |
| 2025-12-04 | AI submission policy committed | [`d5c5b6c`](https://github.com/aristocratos/btop/commit/d5c5b6c6ab9f1ca736d513901316a8e99449440d) introduces guidelines; author and committer timestamps are 19:55:15Z. |
| 2026-05-01 | Disclosed implementation merged | [#1583](https://github.com/aristocratos/btop/pull/1583), opened March 23 by `unlimitedsola`, merged at 10:23:40Z; AI-generated code is explicitly disclosed. |

Dates are UTC. PR creation, PR merge, commit author time, and commit committer time are different events. The entries establish evidence found by this review, not first-ever use.


## Review scope

- Inspected the default-branch tree, README, repository agent guidance, contribution files, PR template, and 4 checked-in GitHub workflow files at the pinned revision.
- Instruction/contribution files read: [`CONTRIBUTING.md`](https://github.com/aristocratos/btop/blob/612e18f5bd598fe987b30d041b39e5d7b3e0794f/CONTRIBUTING.md)
- Searched merged PRs separately for `Claude`, `Codex`, and `"AI-generated"`, scoped to `repo:aristocratos/btop`; inspected up to 10 results per query, ordered by creation date ascending.
- Searched repository commit messages for `"Claude"`; inspected up to 10 results ordered by author date ascending. These are search-index results, not a complete provenance audit.
- Followed the primary PR, commit, discussion, or path-history links cited below when a candidate needed verification. Search hits mentioning an AI product, quoting another repository, or repeating policy text were not treated as disclosures.
- The record is based on public upstream artifacts. No runtime UX evaluation or upstream test suite was run for this dossier.

## Unknowns and limits

The policy was tightened on [March 22, 2026](https://github.com/aristocratos/btop/commit/7fda07c0954a8d44963b2198f53398a16a9fd50a); the older policy date does not describe today’s exact wording. The inspected examples establish accepted, disclosed contributions, not the first model-assisted contribution or maintainer-wide adoption.

Private usage, undisclosed assistance, work outside the checked paths, and the share of code produced by a model remain unknown. An instruction file records intended behavior; it does not show that every contributor follows it.

[Back to the list](../../README.md)
