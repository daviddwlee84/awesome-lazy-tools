# K9s

[Back to the list](../../README.md) · [Research method](../research-method.md)

- **Upstream:** [derailed/k9s](https://github.com/derailed/k9s)
- **Category:** Kubernetes workflow TUI
- **Reviewed:** 2026-09-21
- **Inspected revision:** [`fefa878f05f6227500d0a5528f62ef6c12de4652`](https://github.com/derailed/k9s/tree/fefa878f05f6227500d0a5528f62ef6c12de4652) (`master`)
- **Repository state:** not archived at review time.

## What it does

K9s watches Kubernetes resources and provides navigation, observation, and management commands for applications in a cluster. Its documented views and keyboard actions cover resources, logs, and related operations. [Upstream README](https://github.com/derailed/k9s/blob/fefa878f05f6227500d0a5528f62ef6c12de4652/README.md).

## Why it fits this list

The selected context and resource remain visible while the user drills into state and chooses an action. It extends the same state-and-action approach beyond a local process or repository.

**UX tradeoff:** The interface still operates within Kubernetes contexts and permissions. Its README documents read-only operation and plugins that add custom commands, so discoverability and available actions depend on the chosen configuration. Some features are explicitly experimental; that does not label the entire project alpha. [Usage and plugins](https://github.com/derailed/k9s/blob/fefa878f05f6227500d0a5528f62ef6c12de4652/README.md).

These are source-backed design observations, not claims of hands-on testing.

## Agentic development

**Evidence status: Documented use.** Status describes the inspected public record, not project quality or the proportion of AI-written code.

### Implementation evidence

The merge commit for [#3755](https://github.com/derailed/k9s/pull/3755) explicitly says it was generated with Claude Code and includes a Claude Opus 4.5 co-author trailer. The PR body describes the fix but does not contain that disclosure. A later merge, [#4045](https://github.com/derailed/k9s/pull/4045), has a Claude Opus 4.8 trailer in its [merge commit](https://github.com/derailed/k9s/commit/25f04da310d5d2aae02af670e7e1c8487127ffda).

### Guidance and contribution policy

No matching `AGENTS.md`, `CLAUDE.md`, Copilot instructions, root contribution guide, or PR template was found in the scoped tree inspection. This does not rule out guidance in other channels or earlier revisions.

No AI-specific contribution policy was identified in the reviewed README or inspected paths. Accepted attributed changes are observations, not a universal contribution permission.

### Bots and automation

The checked-in workflows did not establish AI review or generation automation. Model-attributed merge commits are stronger implementation evidence than a generic automation account or CI result.

## Public milestones

| Date | Evidence type | Public record |
| --- | --- | --- |
| 2026-01-03 | Attributed implementation merged | [#3755](https://github.com/derailed/k9s/pull/3755), opened December 30, 2025 by `majiayu000`, merged at 16:47:48Z; attribution is in [`6cf7e12`](https://github.com/derailed/k9s/commit/6cf7e122f559d317ed8f16b0f27130f8b3dfce56). |
| 2026-06-12 | Later attributed implementation merged | [#4045](https://github.com/derailed/k9s/pull/4045), opened June 10 by `brenth-monad`, merged at 06:48:27Z; fixes arm64 container builds. |

Dates are UTC. PR creation, PR merge, commit author time, and commit committer time are different events. The entries establish evidence found by this review, not first-ever use.


## Review scope

- Inspected the default-branch tree, README, repository agent guidance, contribution files, PR template, and 4 checked-in GitHub workflow files at the pinned revision.
- Instruction/contribution files read: No matching instruction or contribution file was present in the inspected tree.
- Searched merged PRs separately for `Claude`, `Codex`, and `"AI-generated"`, scoped to `repo:derailed/k9s`; inspected up to 10 results per query, ordered by creation date ascending.
- Searched repository commit messages for `"Claude"`; inspected up to 10 results ordered by author date ascending. These are search-index results, not a complete provenance audit.
- Followed the primary PR, commit, discussion, or path-history links cited below when a candidate needed verification. Search hits mentioning an AI product, quoting another repository, or repeating policy text were not treated as disclosures.
- The record is based on public upstream artifacts. No runtime UX evaluation or upstream test suite was run for this dossier.

## Unknowns and limits

The three merged-PR text searches returned no qualifying model-name matches, while commit search found explicit trailers. This is a concrete limit of relying on PR bodies alone. The evidence supports disclosed assistance in specific work, not the autonomy or frequency of the overall development process.

Private usage, undisclosed assistance, work outside the checked paths, and the share of code produced by a model remain unknown. An instruction file records intended behavior; it does not show that every contributor follows it.

[Back to the list](../../README.md)
