# lazyssh

[Back to the list](../../README.md) · [Research method](../research-method.md)

| Snapshot | Value |
| --- | --- |
| Upstream | [Adembc/lazyssh](https://github.com/Adembc/lazyssh) |
| Reviewed | 2026-09-21 |
| Default branch inspected | `main` |
| Inspected SHA | [`07cb2abb1abf65d4036a7574c2b33a1808d5614f`][snapshot] |

## Why it fits

lazyssh organizes hosts from SSH configuration into a searchable, sortable list,
with pins/tags, one-key connection, and tabbed configuration editing. Upstream
explicitly cites lazydocker and K9s as inspiration and delegates connections to
the system SSH binary. [README][readme]

**Tradeoffs:** editing a familiar configuration file makes the UI useful alongside
ordinary SSH, but connection options still require SSH knowledge. The README
lists file transfer and key deployment under upcoming work at this snapshot;
they are not counted as shipped capabilities here. Its documented backup and
atomic-write behavior is an upstream claim, not independently tested in this
catalog. [README][readme]

## Agentic development

**Homepage status: Automation found.** A merged PR contains a CodeRabbit-generated
summary. No public coding-agent implementation disclosure or repository guidance
was found within this review.

| Evidence kind | What the public record supports |
| --- | --- |
| Implementation | No explicit coding-agent implementation disclosure was found in the bounded commit/PR review. |
| Guidance | No `AGENTS.md`, `CLAUDE.md`, or Copilot instruction file was found in the inspected tree. |
| Policy | The README's contributing/semantic-PR guidance was inspected; no explicit AI contribution policy was found. |
| Review/summary automation | PR #55 contains an explicitly marked CodeRabbit-generated summary. This does not identify who authored its code, nor prove a completed code review. |

A generated PR summary must not be promoted into a claim that lazyssh was built
with an agent. Equally, the absence of implementation disclosure in these sources
does not establish that its developers never used AI. [PR #55][automation]

## Public milestones found

| Date (UTC) | Event | Evidence |
| --- | --- | --- |
| 2025-09-19 | Merged PR with automated summary | [#55][automation]: CodeRabbit summary attached to CI/test/documentation changes. This is an automation event, not an implementation-adoption date. |

PR chronology (UTC), recorded separately from the milestone labels:

| PR | Opened | Merged |
| --- | --- | --- |
| #55 | 2025-09-19T10:14:41Z | 2025-09-19T11:31:50Z |

## Search boundary and unknowns

Reviewed the README/contribution section and complete file-name tree at the
pinned SHA. The default-branch commit endpoint returned 29 entries with a
100-entry cap; all 29 messages were inspected for explicit attribution.
GitHub queries, 20-result cap each: commit `repo:Adembc/lazyssh
"Co-Authored-By"`, merged PRs with `"AI"`, and merged PRs with `"Codex"`.
They returned 0, 1, and 0 matches. Read #55's body, issue comments, and review
records (100-entry caps).

No default-branch instruction file or public implementation disclosure was
found in those sources. Older/deleted branches, private work, differently worded
disclosures, and other AI products may fall outside this search.

## Sources

- [Pinned snapshot][snapshot] and [README][readme].
- [PR #55 with labeled CodeRabbit summary][automation].
- [How this collection separates evidence types](../research-method.md).

[automation]: https://github.com/Adembc/lazyssh/pull/55

[snapshot]: https://github.com/Adembc/lazyssh/tree/07cb2abb1abf65d4036a7574c2b33a1808d5614f
[readme]: https://github.com/Adembc/lazyssh/blob/07cb2abb1abf65d4036a7574c2b33a1808d5614f/README.md
