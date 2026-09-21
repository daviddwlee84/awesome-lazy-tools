# gh-dash

[Back to the list](../../README.md) · [Research method](../research-method.md)

- **Upstream:** [dlvhdr/gh-dash](https://github.com/dlvhdr/gh-dash)
- **Category:** GitHub review and issue workflow TUI
- **Reviewed:** 2026-09-21
- **Inspected revision:** [`7e140818c139633c4700d55a35947f6b948d6902`](https://github.com/dlvhdr/gh-dash/tree/7e140818c139633c4700d55a35947f6b948d6902) (`main`)
- **Repository state:** not archived at review time.

## What it does

gh-dash presents configurable PR and issue sections, keyboard actions, diffs, and repository-specific commands. Its configuration can describe the views and actions that match a contributor’s GitHub workflow. [Upstream README](https://github.com/dlvhdr/gh-dash/blob/7e140818c139633c4700d55a35947f6b948d6902/README.md).

## Why it fits this list

It keeps the review queue visible while allowing the selected PR or issue to become the target of the next action. User-defined sections and actions offer concrete examples of making frequent work discoverable.

**UX tradeoff:** The useful scope depends on the configured sections, queries, and actions. It is a GitHub workflow surface rather than a replacement for every local Git operation. [Features](https://github.com/dlvhdr/gh-dash/blob/7e140818c139633c4700d55a35947f6b948d6902/README.md).

These are source-backed design observations, not claims of hands-on testing.

## Agentic development

**Evidence status: Documented use.** Status describes the inspected public record, not project quality or the proportion of AI-written code.

### Implementation evidence

[#825](https://github.com/dlvhdr/gh-dash/pull/825) explicitly discloses Claude Code assistance, plus manual review and testing, and was merged by `dlvhdr`. [#849](https://github.com/dlvhdr/gh-dash/pull/849) separately discloses Hermes Agent/OpenAI Codex assistance with inspection, implementation, tests, and verification. These are historical merged contributions; they do not override the current contribution policy.

### Guidance and contribution policy

No matching agent instruction file was found in the inspected tree. Contribution documentation and a dedicated AI policy are present.

The current policy prohibits LLM-generated or LLM-edited code and prose, translation, shared brainstorming, and other AI-assisted outside contributions. It explicitly exempts maintainers subject to their judgment. Thus “strict no-AI” must be qualified as an **outside-contribution policy**, not a claim of zero maintainer AI use. [Policy at the inspected revision](https://github.com/dlvhdr/gh-dash/blob/7e140818c139633c4700d55a35947f6b948d6902/AI_POLICY.md); [current policy](https://github.com/dlvhdr/gh-dash/blob/main/AI_POLICY.md).

### Bots and automation

No checked-in AI review workflow was established by the workflow scan. Historical implementation disclosures and a current policy are different evidence categories from bot automation.

## Public milestones

| Date | Evidence type | Public record |
| --- | --- | --- |
| 2026-04-05 | Disclosed implementation merged | [#825](https://github.com/dlvhdr/gh-dash/pull/825), opened April 3 by `seflue`, merged April 5 at 16:42:56Z; Claude Code assistance is explicit. |
| 2026-06-05 | Restrictive policy merged | [#905](https://github.com/dlvhdr/gh-dash/pull/905) was opened at 12:42:38Z and merged at 12:43:19Z; adds the current no-AI policy with a maintainer exception. |

Dates are UTC. PR creation, PR merge, commit author time, and commit committer time are different events. The entries establish evidence found by this review, not first-ever use.


## Review scope

- Inspected the default-branch tree, README, repository agent guidance, contribution files, PR template, and 8 checked-in GitHub workflow files at the pinned revision.
- Instruction/contribution files read: [`.github/pull_request_template.md`](https://github.com/dlvhdr/gh-dash/blob/7e140818c139633c4700d55a35947f6b948d6902/.github/pull_request_template.md), [`CONTRIBUTING.md`](https://github.com/dlvhdr/gh-dash/blob/7e140818c139633c4700d55a35947f6b948d6902/CONTRIBUTING.md)
- Searched merged PRs separately for `Claude`, `Codex`, and `"AI-generated"`, scoped to `repo:dlvhdr/gh-dash`; inspected up to 10 results per query, ordered by creation date ascending.
- Searched repository commit messages for `"Claude"`; inspected up to 10 results ordered by author date ascending. These are search-index results, not a complete provenance audit.
- Followed the primary PR, commit, discussion, or path-history links cited below when a candidate needed verification. Search hits mentioning an AI product, quoting another repository, or repeating policy text were not treated as disclosures.
- The record is based on public upstream artifacts. No runtime UX evaluation or upstream test suite was run for this dossier.

## Unknowns and limits

The policy changed over time. #849 merged on June 5 at 12:14:35Z, before #905 merged later that day. A historical accepted AI-assisted PR is not evidence that a similar outside submission would comply today. The bounded review does not establish the first private or public use.

Private usage, undisclosed assistance, work outside the checked paths, and the share of code produced by a model remain unknown. An instruction file records intended behavior; it does not show that every contributor follows it.

[Back to the list](../../README.md)
