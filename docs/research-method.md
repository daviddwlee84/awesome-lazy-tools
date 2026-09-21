# Researching agentic development

[Back to the list](../README.md)

This research asks what a project's **public record** shows about coding-agent use and how that workflow evolved. It does not estimate private usage, implementation quality, or an AI-generated percentage.

## Read the homepage columns

| Status | What it supports |
| --- | --- |
| Documented use | An explicit implementation disclosure, attributable merged contribution, or published development record was inspected. The notes identify which kind. |
| Guidance found | Coding-agent instructions were found; actual use may remain unverified. |
| Automation found | AI review or documentation automation is configured or explicitly documented; agent-written implementation remains unverified. |
| No public evidence found | The recorded, bounded search found no sufficient implementation or guidance evidence. This does not mean no AI use. |
| Not reviewed | Research has not yet been completed. Do not substitute a negative conclusion. |

These are evidence summaries, not maturity levels. Contribution restrictions, attribution requirements, and human-review expectations belong beside the evidence in each tool's notes. A maintainer can use agents privately while restricting external AI-generated pull requests.

Homepage milestones name the event: for example, **merged implementation**, **guidance merged**, or **published transcript**. Different events are not interchangeable adoption dates. All dates use UTC unless explicitly stated otherwise.

## A bounded review for each tool

1. Inspect the canonical repository's default branch and pin its SHA. Read its README, contribution policy, and relevant agent instruction files, including repository-specific locations if present.
2. Look for explicit implementation disclosures in merged pull requests, commit trailers, or maintainer-authored development records. Record the queries and limits, including pagination or search caps. A small search is not an exhaustive history audit.
3. Trace the history of relevant instruction files when found. Distinguish their initial addition from later policy and tooling changes. File absence today does not prove historical absence.
4. Check current policy separately from observed use. Review bots, dependency bots, and CI automation do not establish agent-written implementation.
5. Record the review date, inspected ref, findings, primary sources, and unresolved questions in `docs/<tool>/README.md`. Summarize only what that evidence supports in the homepage.

Use the [research template](_template.md). Additional history work should answer a concrete question; the default review need not enumerate every AI-attributed commit.

## Evidence and dates

Prefer an explicit maintainer/contributor statement attached to the work, a merged PR with attribution, a committed development transcript, or the exact instruction-file revision. Attribution trailers are self-reported evidence, not independent measurements of how much code a model wrote. A skill installed in a repository demonstrates available guidance, not necessarily its execution.

For PRs, record `created_at` and `merged_at` separately. A non-null `merge_commit_sha` can describe a test merge even when a PR was never merged; use `merged` or `merged_at`. For commits, distinguish author and committer timestamps. Neither automatically gives the date the work became public or entered the main branch.

Use **earliest evidence found**, not “first ever.” An unopened or self-closed proposal does not establish maintainer rejection. A new instruction does not by itself prove an earlier failure caused it. Link fixed commit URLs for historical claims; use current upstream policy links when directing contributors to rules that may change.

## Deep case studies

The [Lazygit study](lazygit/README.md) separates an external proposal, an explicitly disclosed maintainer implementation, repository guidance, and subsequent collaboration rules. That distinction is reusable across older projects adopting agents and newer projects with agent-assisted development records from inception.

We do not carry forward unverified AI-commit counts or percentages from search-result windows. Any future quantitative study must define its population, date fields, deduplication, query coverage, and attribution limits first.

## Refreshing research

Revisit the notes when adding or materially revising an entry, when upstream policy changes, or when a reader supplies better evidence. Preserve dated historical events; update the current-state summary and `Reviewed` date together. If a URL breaks, seek the same primary artifact before weakening a claim or citing a secondary retelling.

Research observations can inform the [design guide](design-guide.md) and companion skill, but one project's workflow is not a universal rule.
