# Television

[Back to the list](../../README.md) · [Research method](../research-method.md)

- **Upstream:** [alexpasmantier/television](https://github.com/alexpasmantier/television)
- **Category:** Fuzzy finder and configurable channel toolkit
- **Reviewed:** 2026-09-21
- **Inspected revision:** [`3982f0a4159024e33202664238ef1d8932ae13dc`](https://github.com/alexpasmantier/television/tree/3982f0a4159024e33202664238ef1d8932ae13dc) (`main`)
- **Repository state:** not archived at review time.

## What it does

Television searches files, text, repositories, and other sources through named channels. Its documented channel format separates the source command, preview, and actions; shell integration provides quick entry points. [Upstream README](https://github.com/alexpasmantier/television/blob/3982f0a4159024e33202664238ef1d8932ae13dc/README.md).

## Why it fits this list

Channels package a repeatable source/filter/preview/action workflow behind a consistent interface. That is useful when a full domain-specific TUI would be more infrastructure than the task needs.

**UX tradeoff:** A channel still depends on its underlying data commands and selected actions. The abstraction simplifies the picker interface, but each channel must define meaningful output and preview behavior. [Custom channels](https://github.com/alexpasmantier/television/blob/3982f0a4159024e33202664238ef1d8932ae13dc/README.md#custom-channels).

These are source-backed design observations, not claims of hands-on testing.

## Agentic development

**Evidence status: Documented use.** Status describes the inspected public record, not project quality or the proportion of AI-written code.

### Implementation evidence

[#889](https://github.com/alexpasmantier/television/pull/889) and [#891](https://github.com/alexpasmantier/television/pull/891) explicitly disclose Claude Code generation and were merged. An earlier [author comment on #564](https://github.com/alexpasmantier/television/pull/564#issuecomment-3011941847) acknowledges AI embellishment of documentation based on a human draft; that is documentation assistance, not evidence that its test implementation was generated.

### Guidance and contribution policy

No matching agent instruction file was found in the scoped tree inspection. The contribution guides document development setup, tests, documentation, and channel changes. [Guide](https://github.com/alexpasmantier/television/blob/3982f0a4159024e33202664238ef1d8932ae13dc/CONTRIBUTING.md).

No AI-specific contribution policy was identified in the current inspected guides. A maintainer’s historical request for shorter, clearer documentation is evidence about that review, not a blanket ban on assisted contributions.

### Bots and automation

The inspected workflows did not establish an AI review/generation bot. The fact that #889 changes Dependabot configuration must not be confused with its explicit Claude authorship disclosure.

## Public milestones

| Date | Evidence type | Public record |
| --- | --- | --- |
| 2025-06-27 | Documentation-assistance disclosure | [Author comment on #564](https://github.com/alexpasmantier/television/pull/564#issuecomment-3011941847), 07:07:06Z; PR merged at 11:32:29Z after revision. |
| 2026-02-04 | Disclosed implementation merged | [#889](https://github.com/alexpasmantier/television/pull/889), opened January 28 by `simono`, merged at 20:41:42Z; Claude Code generation is explicit. |

Dates are UTC. PR creation, PR merge, commit author time, and commit committer time are different events. The entries establish evidence found by this review, not first-ever use.


## Review scope

- Inspected the default-branch tree, README, repository agent guidance, contribution files, PR template, and 10 checked-in GitHub workflow files at the pinned revision.
- Instruction/contribution files read: [`.github/pull_request_template.md`](https://github.com/alexpasmantier/television/blob/3982f0a4159024e33202664238ef1d8932ae13dc/.github/pull_request_template.md), [`CONTRIBUTING.md`](https://github.com/alexpasmantier/television/blob/3982f0a4159024e33202664238ef1d8932ae13dc/CONTRIBUTING.md), [`website/CONTRIBUTING.md`](https://github.com/alexpasmantier/television/blob/3982f0a4159024e33202664238ef1d8932ae13dc/website/CONTRIBUTING.md)
- Searched merged PRs separately for `Claude`, `Codex`, and `"AI-generated"`, scoped to `repo:alexpasmantier/television`; inspected up to 10 results per query, ordered by creation date ascending.
- Searched repository commit messages for `"Claude"`; inspected up to 10 results ordered by author date ascending. These are search-index results, not a complete provenance audit.
- Followed the primary PR, commit, discussion, or path-history links cited below when a candidate needed verification. Search hits mentioning an AI product, quoting another repository, or repeating policy text were not treated as disclosures.
- The record is based on public upstream artifacts. No runtime UX evaluation or upstream test suite was run for this dossier.

## Unknowns and limits

Some current commit-search results have February author timestamps but April committer timestamps after history changes. The implementation milestone above uses the PR’s actual merge timestamp, not a rebased commit date. The bounded review establishes separate documentation and code evidence; it does not determine an overall start date.

Private usage, undisclosed assistance, work outside the checked paths, and the share of code produced by a model remain unknown. An instruction file records intended behavior; it does not show that every contributor follows it.

[Back to the list](../../README.md)
