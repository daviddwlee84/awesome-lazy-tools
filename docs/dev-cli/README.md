# dev-cli

[Back to the list](../../README.md) · [Research method](../research-method.md)

| Snapshot | Value |
| --- | --- |
| Upstream | [daviddwlee84/dev-cli](https://github.com/daviddwlee84/dev-cli) |
| Reviewed | 2026-09-21 |
| Default branch inspected | `main` |
| Inspected SHA | [`689836cdea61d46ee86cdfa4a0df42ac324e6561`][snapshot] |

This project is maintained by the maintainer of this collection.

## Why it fits

The `dev` command groups repositories, worktrees, tasks, runtimes, remote hosts,
and agent configuration into a persistent dashboard. Live filters, contextual
actions/help, and shared CLI wizards make the next action visible while Git and
the runtime remain authoritative for their state. [README][readme]

**Tradeoffs:** this is a broad workflow coordinator, with more configuration and
lifecycle concepts than a single-purpose picker. Opening a checkout, launching
an agent, finishing a task, finalizing artifacts, and retiring a worktree are
separate operations. That explicitness costs interaction steps but helps prevent
one action from silently claiming another has completed. [README][readme]

## Agentic development

**Homepage status: Documented use.** The inspected public history includes
implementation commits and a merged PR attributed to Claude Code.

| Evidence kind | What the public record supports |
| --- | --- |
| Implementation attribution | The merge of PR #32 and its implementation/testing commits carry Claude Code co-author trailers. |
| Development guidance | Repository agent instructions and committed development histories are available. |
| Agent-facing product capability | An embedded `dev-cli` operational skill, machine-readable commands, and explicit agent/runtime workflows are shipped features, distinct from implementation attribution. |
| Policy | Artifact retention/publication and guarded mutation workflows are documented; these operational rules are not treated as a universal AI contribution policy. |
| Review automation | The classification relies on attributed work, not dependency bots or CI. |

A tool for coordinating coding agents is not automatically an agent-written tool.
Here the co-author attribution supplies separate evidence for a specific accepted
change. [Attributed merge][implementation], [contributor guidance][guidance]

## Public milestones found

| Date (UTC) | Event | Evidence |
| --- | --- | --- |
| 2026-09-19 | Attributed merge commit | [Commit `953a3a07`][implementation], merging #32, attributes guarded closeout/navigation work to Claude Code. This date is the commit's committer timestamp. |

## Search boundary and unknowns

Reviewed the pinned public tree, README, repository guidance, and the latest
100 commit messages out of 300 reachable commits. The tree includes 66 committed
development-history files; their presence was inventoried, not treated as 66
independently verified agent implementations. The implementation finding above
uses the explicit merge/commit attribution, rather than transcript counts.

Confirmed the pinned public SHA via GitHub. This bounded history review was not
an exhaustive external-PR or historical-model census. The milestone is the
commit's committer date; it does not identify the project's earliest agent use.
Co-author trailers are attribution, not independently measured code provenance.

## Sources

- [Pinned snapshot][snapshot] and [README][readme].
- [Repository contributor guidance][guidance].
- [Claude Code-attributed merge][implementation] and [associated PR][pr].

[guidance]: https://github.com/daviddwlee84/dev-cli/blob/689836cdea61d46ee86cdfa4a0df42ac324e6561/CLAUDE.md
[implementation]: https://github.com/daviddwlee84/dev-cli/commit/953a3a07bc71b83257c24de28b494993a3955a05
[pr]: https://github.com/daviddwlee84/dev-cli/pull/32

[snapshot]: https://github.com/daviddwlee84/dev-cli/tree/689836cdea61d46ee86cdfa4a0df42ac324e6561
[readme]: https://github.com/daviddwlee84/dev-cli/blob/689836cdea61d46ee86cdfa4a0df42ac324e6561/README.md
