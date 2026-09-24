# lazypkg

[Back to the list](../../README.md) · [Research method](../research-method.md)

| Snapshot | Value |
| --- | --- |
| Canonical upstream | [daviddwlee84/lazypkg](https://github.com/daviddwlee84/lazypkg) |
| Reviewed | 2026-09-24 (UTC) |
| Inspected revision | [`c125fb8`][snapshot] (full SHA pinned in references) |
| Source version | [`v0.1.2`][tag] |
| Interface | Software inventory CLI and package-management TUI |
| Stage | Early source release; no prebuilt lazypkg binary distribution is claimed |
| Build | Go 1.26 or newer; build `./cmd/lazypkg` from a checkout |
| License | No project-wide license declared; the bundled skill has its own [MIT license][skill-license] |

This project is maintained by the maintainer of this collection. Its documented
targets are macOS, Windows and Linux; native support depends on the selected
package manager. The release describes a source installation, not a verified
package channel or binary bundle. The documented install command is
`go install github.com/daviddwlee84/lazypkg/cmd/lazypkg@v0.1.2`. [README][readme],
[module requirements][module]

A publication-time macOS check installed both `@v0.1.2` and `@latest` outside
the checkout, using a fresh temporary module cache and executable directory.
Both reported `lazypkg version v0.1.2`; help and zsh completion also worked.
This checked source installation without changing managed packages.

## Why it fits

Five views connect installed software, package discovery, available updates,
PATH diagnostics and manager health. Keyboard and mouse controls expose ordered
manager groups, saved sets and package selection. Search and existing inventory
are joined without treating same-name PATH presence as proof of installation
ownership. [README][readme], [shared inventory model][inventory]

A mutation opens a review before handing the terminal to the native manager.
Package batches freeze the selected or filtered records, include selections
hidden by a filter, and execute sequentially after one approval. Changed state,
failure or incomplete verification pauses the batch; rechecking prepares another
review. Installed mise versions and explicit global activation are separate
operations. [Batch service][batch], [TUI selection and review][tui-batch]

Focused command-conflict assessment lets the user choose what to retain and
review one supported removal. It distinguishes independent installations from
symlink or shim aliases and considers dependencies and executable ownership.
Manager maintenance has a separate per-item review queue. Neither feature
silently rewrites PATH or upgrades every detected manager. [Workflow service][workflows],
[README][readme]

## Design observations and tradeoffs

**Interpretation:** separating a user's selection intent from execution-time
verification keeps a retained observation useful without claiming it is live.
Provider results arrive incrementally, and the TUI keeps observations for the
session, warms Updates once and uses manual refresh rather than periodic polling.
Known restrictions have a compact marker and an explanation; old or incomplete
metadata can still be selected for verification. [Session state][session],
[streamed queries][stream], [eligibility contracts][eligibility]

Meta Package Manager 8.0.1 supplies most provider operations. The embedded
catalog describes 149 adapters, but detection does not make every operation or
scope available. Environment-specific and unknown scopes remain passive;
capabilities and native version requirements differ. PATH scans cover the
inherited environment, not parent-shell aliases/functions or installation
history across the whole disk. [README coverage and limits][readme],
[catalog][catalog]

A scoped package request can still invoke native prompts or have partial effects.
The application verifies state afterward rather than promising rollback. Generic
managers choose releases under their native update policy; a displayed candidate
is not a version pin. The verification record distinguishes native macOS reads,
isolated lifecycle checks, fake-provider PTY scenarios and cross-builds from
untested native-platform acceptance. [Verification record][verification]

## Agentic development

**Homepage status: Documented use.** The committed Codex CLI development record
contains implementation patches and recorded test/terminal work, not only agent
instructions. It supports a recorded assisted-development workflow, not an
independent attribution audit or an AI-generated percentage. The installed
`go-cli-tui` skill and project `AGENTS.md` separately establish available guidance.
[Committed development record][record], [project guidance][agents], [skill][skill]

No separate project-wide AI contribution policy or AI review automation was
identified in the inspected root tree, README, guidance and CI workflow. The CI
file configures ordinary tests, vet, builds and POSIX PTY checks. The inspected
revision passed its macOS, Linux and Windows CI jobs and catalog validation;
this verifies the automated suite, not native package-installer acceptance.
[CI workflow][ci], [completed CI run][ci-run]

## Public milestones found

| Date (UTC) | Event | Evidence |
| --- | --- | --- |
| 2026-09-24 | Source, development transcript and source tag published | The public source snapshot includes the recorded implementation workflow. The annotated v0.1.2 tag resolves to the inspected revision; no GitHub Release or binary assets accompanied it. [Snapshot][snapshot], [source tag][tag], [release listing][releases] |

The development record was committed in `c289daa6b07784a37e82a16d57ee9acaf093108b`
at 18:36:16 UTC on September 24; its author and committer timestamps agree. That
records commit creation, rather than proof of when the repository became public. The bounded review
does not establish a first-ever use of coding agents. [Record commit][record-commit]

## Research scope and limits

- Inspected the publication revision, its root tree, README, changelog, module file, architecture, verification notes, project guidance, installed skill and CI workflow. Reviewed the shared inventory/eligibility, streaming, batch and TUI session implementations for the described behavior.
- Reviewed the repository's commit history through publication and the addition history of `AGENTS.md`, the skill and committed development record. Searched that committed record for `Codex`, `apply_patch`, `go test -race`, `pty_smoke` and agent-message markers. Uncommitted session updates were excluded; no conversation text or personal environment values are reproduced here.
- Verified the public repository metadata, pinned source snapshot, annotated tag target, successful hosted CI jobs and empty GitHub Releases listing through the GitHub API. No broader external PR attribution search or exhaustive adoption-history audit was performed.
- This catalog addition does not run real package upgrades or removals. The upstream verification record is the source for native-test claims; target-platform declarations and cross-builds are not independent Windows/Linux acceptance tests.

[snapshot]: https://github.com/daviddwlee84/lazypkg/tree/c125fb8906ea04e4c92fc2c438a3570793e17a9b
[tag]: https://github.com/daviddwlee84/lazypkg/tree/v0.1.2
[readme]: https://github.com/daviddwlee84/lazypkg/blob/c125fb8906ea04e4c92fc2c438a3570793e17a9b/README.md
[module]: https://github.com/daviddwlee84/lazypkg/blob/c125fb8906ea04e4c92fc2c438a3570793e17a9b/go.mod
[inventory]: https://github.com/daviddwlee84/lazypkg/blob/c125fb8906ea04e4c92fc2c438a3570793e17a9b/internal/domain/inventory.go
[batch]: https://github.com/daviddwlee84/lazypkg/blob/c125fb8906ea04e4c92fc2c438a3570793e17a9b/internal/app/batch.go
[tui-batch]: https://github.com/daviddwlee84/lazypkg/blob/c125fb8906ea04e4c92fc2c438a3570793e17a9b/internal/tui/batch.go
[workflows]: https://github.com/daviddwlee84/lazypkg/blob/c125fb8906ea04e4c92fc2c438a3570793e17a9b/internal/app/workflows.go
[session]: https://github.com/daviddwlee84/lazypkg/blob/c125fb8906ea04e4c92fc2c438a3570793e17a9b/internal/tui/session.go
[stream]: https://github.com/daviddwlee84/lazypkg/blob/c125fb8906ea04e4c92fc2c438a3570793e17a9b/internal/app/stream.go
[eligibility]: https://github.com/daviddwlee84/lazypkg/blob/c125fb8906ea04e4c92fc2c438a3570793e17a9b/internal/domain/batch.go
[catalog]: https://github.com/daviddwlee84/lazypkg/blob/c125fb8906ea04e4c92fc2c438a3570793e17a9b/internal/catalog/catalog.json
[verification]: https://github.com/daviddwlee84/lazypkg/blob/c125fb8906ea04e4c92fc2c438a3570793e17a9b/docs/verification.md
[record]: https://github.com/daviddwlee84/lazypkg/blob/c125fb8906ea04e4c92fc2c438a3570793e17a9b/.specstory/history/2026-09-24_12-25-21Z-chatgpt-specstory-references-chatgpt.md
[record-commit]: https://github.com/daviddwlee84/lazypkg/commit/c289daa6b07784a37e82a16d57ee9acaf093108b
[agents]: https://github.com/daviddwlee84/lazypkg/blob/c125fb8906ea04e4c92fc2c438a3570793e17a9b/AGENTS.md
[skill]: https://github.com/daviddwlee84/lazypkg/blob/c125fb8906ea04e4c92fc2c438a3570793e17a9b/.agents/skills/go-cli-tui/SKILL.md
[ci]: https://github.com/daviddwlee84/lazypkg/blob/c125fb8906ea04e4c92fc2c438a3570793e17a9b/.github/workflows/ci.yml
[skill-license]: https://github.com/daviddwlee84/lazypkg/blob/c125fb8906ea04e4c92fc2c438a3570793e17a9b/.agents/skills/go-cli-tui/LICENSE.txt
[ci-run]: https://github.com/daviddwlee84/lazypkg/actions/runs/36062885837
[releases]: https://github.com/daviddwlee84/lazypkg/releases
