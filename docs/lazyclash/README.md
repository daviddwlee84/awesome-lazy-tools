# lazyclash

[Back to the list](../../README.md) · [Research method](../research-method.md)

| Snapshot | Value |
| --- | --- |
| Upstream | [daviddwlee84/lazyclash](https://github.com/daviddwlee84/lazyclash) |
| Reviewed | 2026-09-21 |
| Default branch inspected | `main` |
| Inspected SHA | [`907b6b4a366c5088f17124425474c0d6ba333104`][snapshot] |

This project is maintained by the maintainer of this collection.

## Why it fits

A keyboard-oriented console for Mihomo controllers: targets, proxies, traffic,
connections, logs, comparisons, and routing diagnosis share a persistent
workspace. CLI commands and interactive setup expose the same operations;
local, HTTPS, SSH, and Unix-socket targets are documented. [README][readme]

**Tradeoffs:** runtime controller state, source configuration, and a client
manager's activation state are different layers. Some changes therefore require
a reviewed source edit and native profile reactivation, rather than one toggle.
The inspected project supports macOS/Linux and uses source-based installation;
the interface does not remove Mihomo or SSH configuration complexity.
[README][readme], [operating guide][guide]

## Agentic development

**Homepage status: Guidance found.** The public snapshot contains development
guidance and an agent-facing operational interface, but this bounded review did
not find sufficient public evidence attributing implementation to a coding agent.

| Evidence kind | What the public record supports |
| --- | --- |
| Implementation | The inspected commit messages have no explicit Codex/Claude co-author disclosure, and the snapshot has no committed `.specstory/history/` transcript. |
| Development guidance | An installed `go-cli-tui` skill supplies contributor workflow and terminal UX guidance. |
| Agent-facing product capability | The executable exposes an embedded operational guide through `--skill`. This helps agents use the tool; it does not establish who implemented it. |
| Policy | No separate project-wide AI contribution policy was identified in the reviewed contributor/operating materials. |
| Review automation | No review-bot evidence was used or inferred from CI. |

The project's use of agent-oriented files is intentionally classified as
guidance, not transformed into a claim about autonomous development.
[Development skill][skill], [operating guide][guide]

## Public milestones found

| Date (UTC) | Event | Evidence |
| --- | --- | --- |
| 2026-09-20 | Development guidance committed | [Commit `2fc64fc6`][guidance-commit] adds agent skills; this is guidance availability. |
| 2026-09-20 | Agent-facing interface committed | [Commit `e8594415`][interface-commit] adds the operational guide and source-release support; this is product functionality. |

## Search boundary and unknowns

Reviewed the pinned public commit, all 16 reachable commit messages at that
snapshot, the committed tree, README, operating/reference docs, development skill,
and lock. Confirmed that the exact snapshot is accessible from GitHub.
Uncommitted transcripts and feature work were excluded. Dates above are commit
committer dates, not independently established publication or first-use dates.

No external PR search was needed for a claim of implementation use because no
such claim is made. This local-history-centered review does not exhaust PR
discussion, deleted branches, or private workflows. The absence of a committed
transcript here is not evidence that no agent was used.

## Sources

- [Pinned public snapshot][snapshot], [README][readme], [operating guide][guide].
- [Development skill][skill], [guidance addition][guidance-commit], [agent interface addition][interface-commit].

[guide]: https://github.com/daviddwlee84/lazyclash/blob/907b6b4a366c5088f17124425474c0d6ba333104/docs/README.md
[skill]: https://github.com/daviddwlee84/lazyclash/blob/907b6b4a366c5088f17124425474c0d6ba333104/.agents/skills/go-cli-tui/SKILL.md
[guidance-commit]: https://github.com/daviddwlee84/lazyclash/commit/2fc64fc6a165026c4f78254a07220df68189144f
[interface-commit]: https://github.com/daviddwlee84/lazyclash/commit/e8594415310eebbd3013640f946e861d704c8992

[snapshot]: https://github.com/daviddwlee84/lazyclash/tree/907b6b4a366c5088f17124425474c0d6ba333104
[readme]: https://github.com/daviddwlee84/lazyclash/blob/907b6b4a366c5088f17124425474c0d6ba333104/README.md
