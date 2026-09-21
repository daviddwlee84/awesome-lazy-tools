# exp-cli

[Back to the list](../../README.md) · [Research method](../research-method.md)

| Snapshot | Value |
| --- | --- |
| Upstream | [daviddwlee84/exp-cli](https://github.com/daviddwlee84/exp-cli) |
| Reviewed | 2026-09-21 |
| Default branch inspected | `main` |
| Inspected SHA | [`2ce094a23ca1fcc4c1d381de4044705ffa469a25`][snapshot] |

This project is maintained by the maintainer of this collection.

## Why it fits

The `exp` command coordinates Git-based research records, exploratory runs,
experiment queues, evidence, and reviewed decisions. Wizards help create a
workspace and link source repositories; `exp ui` provides a read-only overview.
The shared record model reduces the need to reconstruct an experiment's state
from unrelated commands. [README][readme]

**Tradeoffs:** the inspected TUI cannot execute work or mutate records; actions
remain in explicit CLI workflows. Formal evaluation/promotion has more structure
than a quick experiment, and upstream deliberately separates a lightweight Try
from promotion-bearing evidence. This is an early research-workflow tool, not a
general replacement for MLflow, job schedulers, or experiment scripts.
[README][readme]

## Agentic development

**Homepage status: Documented use.** Public implementation commits explicitly
attribute contributions to Claude Code.

| Evidence kind | What the public record supports |
| --- | --- |
| Implementation attribution | The CLI foundation and later external-workspace feature commits carry Claude Code co-author trailers. |
| Guidance/product interface | The project provides agent-consumable context/guides and records development sessions; these are separate from the attributed commits. |
| Policy | The product documents trust, reviewed execution, and named-human promotion decisions; these are research-operation rules, not evidence of a project-wide AI contribution policy. |
| Review automation | No review bot is needed to substantiate the implementation finding. |

The original brainstorming record alone would only demonstrate discussion.
The code-bearing, attributed commits provide the stronger basis for this status.
[Foundation commit][foundation], [workspace feature][workspaces]

## Public milestones found

| Date (UTC) | Event | Evidence |
| --- | --- | --- |
| 2026-08-29 | Implementation attribution committed | [`66134be0`][foundation]: Git-native research CLI foundation, with a Claude Code co-author trailer. |
| 2026-09-04 | Implementation attribution committed | [`73185515`][workspaces]: external experiment workspaces and guided terminal UX, also attributed to Claude Code. |

## Search boundary and unknowns

Reviewed the complete seven-commit history reachable from the pinned public SHA,
the committed file tree, README, and the available development-session inventory
(five history files). Inspected the original discussion as context, but did not
use that discussion as proof of implementation. Confirmed the snapshot via
GitHub.

Dates above are commit committer dates, not a claim about first public exposure
or first private AI use. This review did not measure the proportion of generated
code, execute experiments, or establish production readiness. The available
[CI run for this snapshot][ci] reports a failed macOS race-test step; this entry
does not claim that all checks passed. Uncommitted work and features beyond the
fixed snapshot were excluded.

## Sources

- [Pinned snapshot][snapshot] and [README][readme].
- [Attributed foundation implementation][foundation].
- [Attributed external-workspace implementation][workspaces].

[foundation]: https://github.com/daviddwlee84/exp-cli/commit/66134be08f7b9dc0061b2a7c97f6fcfca68ca1dd
[workspaces]: https://github.com/daviddwlee84/exp-cli/commit/7318551523d3de7b1b7bad5addf734856a28a048
[ci]: https://github.com/daviddwlee84/exp-cli/actions/runs/34503920282

[snapshot]: https://github.com/daviddwlee84/exp-cli/tree/2ce094a23ca1fcc4c1d381de4044705ffa469a25
[readme]: https://github.com/daviddwlee84/exp-cli/blob/2ce094a23ca1fcc4c1d381de4044705ffa469a25/README.md
