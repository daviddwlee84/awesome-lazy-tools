# lnav

[Back to the list](../../README.md) · [Research method](../research-method.md)

| Snapshot | Value |
| --- | --- |
| Upstream | [tstack/lnav](https://github.com/tstack/lnav) |
| Reviewed | 2026-09-21 |
| Default branch inspected | `master` |
| Inspected SHA | [`18779fc5b492efd61fae8898d66df7bf928ee282`][snapshot] |

## Why it fits

lnav combines recognized log files into a time-ordered view, follows updates,
indexes errors and warnings, and offers filtering, histograms, and SQLite
analysis. Moving from an overview to a relevant event preserves surrounding
context. This is the collection's interaction criterion applied to a log viewer,
rather than a claim that lnav brands itself as a lazy tool. [README][readme]

**Tradeoffs:** automatic structure depends on recognized formats; unrecognized
files remain available in the text view. Advanced filtering and analysis still
require regular-expression or SQL knowledge. The benefit is fewer separate
parsing and navigation steps, not the elimination of those concepts.
[README][readme]

## Agentic development

**Homepage status: Documented use.** Two inspected merged fixes explicitly
identify coding-agent assistance.

| Evidence kind | What the public record supports |
| --- | --- |
| Implementation | PR #1725 names OpenAI Codex for a Laravel-log fix; #1744 names Claude Code for diagnosis, a reproducer, and a terminfo patch. |
| Guidance | No `AGENTS.md`, `CLAUDE.md`, Copilot instruction file, or dedicated `CONTRIBUTING` file was found in the inspected tree. |
| Policy | The reviewed materials did not establish a project-wide AI contribution rule. Individual contributors describe their own review/validation practices. |
| Review automation | A maintainer identifies one #1744 discussion comment as Claude output; that comment is distinct from the contributor's implementation disclosure. |

#1725 explicitly makes no human-review claim; #1744 says the work was reviewed
before submission and includes a reproducible diagnosis. These are different
reported workflows. The README's acknowledgment of Anthropic's open-source
program is support evidence, not implementation evidence by itself.
[#1725][laravel], [#1744][terminfo], [README][readme]

## Public milestones found

| Date (UTC) | Event | Evidence |
| --- | --- | --- |
| 2026-07-16 | Merged implementation disclosure | [#1725][laravel]: Codex-assisted handling of hyphenated Laravel channels. |
| 2026-08-24 | Merged implementation disclosure | [#1744][terminfo]: Claude Code-assisted terminfo parsing fix. |

PR chronology (UTC), recorded separately from the milestone labels:

| PR | Opened | Merged |
| --- | --- | --- |
| #1725 | 2026-07-16T14:25:43Z | 2026-07-16T15:39:16Z |
| #1744 | 2026-08-23T19:35:47Z | 2026-08-24T02:24:24Z |

## Search boundary and unknowns

Reviewed both root README files and the complete file-name tree at the pinned
SHA, plus the latest 100 reachable commits. GitHub searches were capped at 20
results each: commit `repo:tstack/lnav "Co-Authored-By"`, and merged-PR searches
for `"AI"` and `"Codex"`; totals were 2, 4, and 1. Read PRs #1725/#1744 and up
to 100 issue comments per PR. The recent history includes the attributed
terminfo commits.

This establishes particular accepted contributions, not a project-wide adoption
date, private usage history, or generated-code percentage. No contribution
policy should be inferred from the absence of a root instruction file.

## Sources

- [Pinned snapshot][snapshot] and [README][readme].
- [Laravel patch and disclosure][laravel].
- [Terminfo patch and disclosure][terminfo] and [maintainer's comment][comment].

[laravel]: https://github.com/tstack/lnav/pull/1725
[terminfo]: https://github.com/tstack/lnav/pull/1744
[comment]: https://github.com/tstack/lnav/pull/1744#issuecomment-5388425013

[snapshot]: https://github.com/tstack/lnav/tree/18779fc5b492efd61fae8898d66df7bf928ee282
[readme]: https://github.com/tstack/lnav/blob/18779fc5b492efd61fae8898d66df7bf928ee282/README.md
