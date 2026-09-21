# lazysql

[Back to the list](../../README.md) · [Research method](../research-method.md)

| Snapshot | Value |
| --- | --- |
| Upstream | [jorgerojas26/lazysql](https://github.com/jorgerojas26/lazysql) |
| Reviewed | 2026-09-21 |
| Default branch inspected | `main` |
| Inspected SHA | [`f30ed5afef2a31d566a2ece9c57211058de16a41`][snapshot] |

## Why it fits

A database workbench with a schema browser, SQL editor, results, multiple
connections, tabs, and Vim-style navigation. Its author explicitly cites Lazygit
as the inspiration: keep database context beside the action instead of repeatedly
constructing commands. [Upstream README][readme]

**Tradeoffs:** the inspected README still labels the project alpha. The custom
editor offers completion and modal editing, but its modes and database-specific
behavior add learning and maintenance costs. That is a design tradeoff inferred
from the documented interface, not a reliability benchmark. [README][readme],
[editor rewrite][editor]

## Agentic development

**Homepage status: Documented use.** Multiple merged implementation PRs explicitly
disclose AI assistance; one describes a substantially autonomous editor rewrite.

| Evidence kind | What the public record supports |
| --- | --- |
| Implementation | PR #283 discloses an AI-assisted JSON-viewer fix and manual testing; PR #307 explicitly attributes its editor implementation to OpenCode CLI with DeepSeek V4 Flash. |
| Guidance | No `AGENTS.md`, `CLAUDE.md`, or Copilot instruction file was found in the inspected tree. |
| Policy | The README's contribution section was inspected; no explicit project-wide AI contribution policy was found there. |
| Review automation | No review-bot evidence is needed for the implementation classification; ordinary CI does not establish AI authorship. |

PR #307's author states that the code was neither authored nor reviewed by a
human. This is the author's disclosure attached to a merged contribution, not an
independent audit or a conclusion about the rest of the project. PR #339 later
describes a different workflow: AI assistance followed by human review and
testing. [#307][editor], [#339][sorting]

## Public milestones found

| Date (UTC) | Event | Evidence |
| --- | --- | --- |
| 2026-02-27 | Merged implementation disclosure | [#283][json-fix]: AI-assisted fix for extra JSON nesting. |
| 2026-05-25 | Merged agent-authored implementation disclosure | [#307][editor]: custom SQL editor with highlighting, Vim modes, and completion. |

PR chronology (UTC), recorded separately from the milestone labels:

| PR | Opened | Merged |
| --- | --- | --- |
| #283 | 2026-02-26T22:44:05Z | 2026-02-27T03:01:07Z |
| #307 | 2026-05-18T13:13:42Z | 2026-05-25T03:31:20Z |
| #339 | 2026-08-19T09:54:54Z | 2026-08-20T17:03:24Z |

## Search boundary and unknowns

Reviewed the README/contributing section and the complete file-name tree at the
pinned SHA; read the latest 100 commits reachable from that SHA. GitHub searches
were limited to the first 20 results per query: `repo:jorgerojas26/lazysql
"Co-Authored-By"` in commits, and `repo:jorgerojas26/lazysql is:pr is:merged
"AI"` / `"Codex"` in PRs. These returned 22, 3, and 0 total matches respectively;
the commit search was capped, not exhausted. Read PRs #283, #307, #339 and their
available issue comments. Confirmed #307's merge commit is an ancestor of the
inspected snapshot.

The dates are merge dates for those specific contributions, not first-ever AI
use. Attribution does not measure generated-code percentage or establish quality.
No runtime testing was performed for this catalog entry.

## Sources

- [Pinned repository snapshot][snapshot] and [README][readme].
- [JSON-viewer disclosure][json-fix], [editor disclosure][editor], [sorting disclosure][sorting].

[json-fix]: https://github.com/jorgerojas26/lazysql/pull/283
[editor]: https://github.com/jorgerojas26/lazysql/pull/307
[sorting]: https://github.com/jorgerojas26/lazysql/pull/339

[snapshot]: https://github.com/jorgerojas26/lazysql/tree/f30ed5afef2a31d566a2ece9c57211058de16a41
[readme]: https://github.com/jorgerojas26/lazysql/blob/f30ed5afef2a31d566a2ece9c57211058de16a41/README.md
