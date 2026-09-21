# VisiData

[Back to the list](../../README.md) · [Research method](../research-method.md)

| Snapshot | Value |
| --- | --- |
| Upstream | [saulpw/visidata](https://github.com/saulpw/visidata) |
| Reviewed | 2026-09-21 |
| Default branch inspected | `develop` |
| Inspected SHA | [`013d9b3e985f575baa8316e461a704e5085c9bba`][snapshot] |

## Why it fits

VisiData turns tabular sources into a consistent terminal workspace for
navigation, selection, sorting, frequency tables, and further exploration.
The README documents CSV, TSV, SQLite, JSON, Excel, and other loaders; the
contribution guide recommends teaching a small useful subset first.
[README][readme], [contribution guide][contributing]

**Tradeoffs:** hundreds of commands reward repeated use but create a substantial
learning surface. Some formats need additional Python packages. The inspected
default branch is `develop`, which upstream distinguishes from its stable
distribution; this snapshot is not a promise about the installed release.
[README][readme]

## Agentic development

**Homepage status: Documented use.** Explicit implementation attribution exists
alongside contributor guidance and a human-review policy.

| Evidence kind | What the public record supports |
| --- | --- |
| Implementation | Merged PR #3151 identifies Claude Code/Claude Opus 4.8 assistance and a human operator's understanding; the pinned HEAD also carries a Codex co-author trailer. |
| Guidance | Root `CLAUDE.md` describes architecture/workflow; `AGENTS.md` routes agents to it and focused developer references. |
| Policy | Guidance requires human review, approval, and testing before merge or PR. The PR template asks for AI level, model/version where applicable, and the human operator for bot accounts. |
| Review automation | Review-bot activity is not the basis for the documented-use classification. |

The maintainer's discussion on #2981 explicitly distinguishes useful agent
instructions from accepting unreviewed bot contributions. A guidance file alone
would be weaker evidence than the separately attributed implementation.
[Policy][claude], [PR template][template], [discussion][guidance-pr]

## Public milestones found

| Date (UTC) | Event | Evidence |
| --- | --- | --- |
| 2026-02-03 | Guidance introduced | [Commit `ede8f983`][first-guidance] adds `CLAUDE.md`. |
| 2026-06-22 | Merged implementation disclosure | [#3151][implementation]: CSV blank-line handling, with explicit AI level and model disclosure. |

PR chronology (UTC), recorded separately from the milestone labels:

| PR | Opened | Merged |
| --- | --- | --- |
| #2981 | 2026-02-15T20:04:45Z | 2026-03-06T21:52:45Z |
| #3151 | 2026-06-22T17:50:29Z | 2026-06-22T21:55:26Z |

## Search boundary and unknowns

Reviewed the complete file-name tree, README, root contribution/guidance files,
nested DAW guidance, and PR template at the pinned SHA; scanned its latest 100
commits. Read root instruction-file histories (up to 100 commits per file), PRs
#2981/#3151, and their available issue comments.

GitHub queries, first 20 results each: commit `repo:saulpw/visidata
"Co-Authored-By"`; merged-PR searches for `"AI"` and `"Codex"`.
They returned 292, 31, and 1 total matches; the first two were capped.
This is not a count of all AI-written commits or an audit of private workflows.
The latest [Codex-attributed commit][head-commit] is additional specific evidence,
not a basis for extrapolating authorship across the project.

## Sources

- [Snapshot][snapshot], [README][readme], [contribution guide][contributing].
- [CLAUDE.md][claude], [AGENTS.md][agents], [PR template][template].
- [Guidance discussion][guidance-pr], [implementation disclosure][implementation].

[contributing]: https://github.com/saulpw/visidata/blob/013d9b3e985f575baa8316e461a704e5085c9bba/CONTRIBUTING.md
[claude]: https://github.com/saulpw/visidata/blob/013d9b3e985f575baa8316e461a704e5085c9bba/CLAUDE.md
[agents]: https://github.com/saulpw/visidata/blob/013d9b3e985f575baa8316e461a704e5085c9bba/AGENTS.md
[template]: https://github.com/saulpw/visidata/blob/013d9b3e985f575baa8316e461a704e5085c9bba/.github/PULL_REQUEST_TEMPLATE.md
[guidance-pr]: https://github.com/saulpw/visidata/pull/2981
[first-guidance]: https://github.com/saulpw/visidata/commit/ede8f983921692c6dcaa0def9c5b10c376046294
[implementation]: https://github.com/saulpw/visidata/pull/3151
[head-commit]: https://github.com/saulpw/visidata/commit/013d9b3e985f575baa8316e461a704e5085c9bba

[snapshot]: https://github.com/saulpw/visidata/tree/013d9b3e985f575baa8316e461a704e5085c9bba
[readme]: https://github.com/saulpw/visidata/blob/013d9b3e985f575baa8316e461a704e5085c9bba/README.md
