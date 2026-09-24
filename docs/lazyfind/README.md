# lazyfind

[Back to the list](../../README.md) · [Research method](../research-method.md)

| Snapshot | Value |
| --- | --- |
| Canonical upstream | [daviddwlee84/lazyfind](https://github.com/daviddwlee84/lazyfind) |
| Reviewed | 2026-09-24 (UTC) |
| Inspected revision | [`05b7d6e0af2cbf332800abaa8a66e87c967af591`][snapshot] |
| Tagged implementation | [`v0.1.1`][tag], targeting `0292b873b27b259cba0531cc3ddcb952c3af8acb` |
| Interface | Search orchestration CLI, TUI and single-result picker |
| Stage | Early source-only version; annotated tags, no GitHub Release or binary distribution |
| Build | Go 1.26+, `make build` or `go install .` from a checkout |
| License | No project-wide license declared in this revision; the bundled skill has a separate [MIT license][skill-license] |

This project is maintained by the maintainer of this collection. The reviewed
README documents `go install github.com/daviddwlee84/lazyfind@v0.1.1` and a
checkout-based installation path. The public repository, default branch and
annotated source tags were verified on 2026-09-24. These tags do not provide a
GitHub Release or prebuilt binaries. The bundled skill license does not declare
a license for the application. [Installation][readme], [module requirements][module]

## Why it fits

The source implements a search-first workflow: choose local or single-host SSH
roots, enter a keyword, refine conditions, inspect a deduplicated result list and
choose a downstream action. fd handles traversal and name search; ripgrep handles
text, while ripgrep-all and zoxide provide optional document and frequent-directory
sources. Keyboard and mouse controls expose source selection, metadata filters,
match navigation, preview and sorting. [README][readme], [search service][search]

Two refinements have different costs: editing the main query starts another
backend search, while Ctrl+F narrows already loaded results in memory. Condition
completion and a visual filter form make qualifiers discoverable. Searchable
Actions and Help popups retain the surrounding list; editor, Yazi and other
configured commands use explicit handoffs. These are documentation and source
observations, not a separate hands-on evaluation. [Query completion][completion],
[TUI state and effects][tui], [actions][actions]

## Design observations and tradeoffs

**Interpretation:** separating a query execution, its retained snapshot and the
current result view helps users understand when an operation will repeat work.
Sorting and list filtering preserve selection by item identity. History opens
stored results offline; rerunning creates a new run and resolves relative dates
again. Durable SQLite history belongs under XDG state, while previews use a
separately disposable cache. [Architecture][architecture], [history][history]

Native text previews retain source line numbers and match spans. Extracted
document positions remain extracted-text locations, and custom preview output
is not assigned invented source lines. Path-copy choices distinguish search-root
relative paths, absolute paths and supported native match references.
[Preview service][preview], [copy formats][copy]

Directory disk usage is an explicit recursive operation, with a cost prompt,
selected/visible-directory choices, cancellation and bounded concurrency. Its
session cache and separate Usage column do not turn directory metadata into
logical file size or alter stored search snapshots. [Disk-usage service][usage],
[configuration][configuration]

The remote model operates on one SSH target per search and requires its existing
fd/rg installation and noninteractive authentication. It does not install a remote
helper; remote descendant termination remains best effort. ripgrep-all depends
on its converters, and extracted lines are not guaranteed PDF pages. This version
uses source installation; published binary archives, a package channel and a
self-updater are not part of the inspected distribution. [Remote and install
boundaries][readme], [architecture][architecture]

## Agentic development

**Homepage status: Documented use.** The published Codex CLI transcript contains
implementation patches and recorded terminal/test work, rather than guidance alone.

| Evidence kind | What the inspected record supports |
| --- | --- |
| Implementation record | The committed September 24 Codex CLI session contains implementation patches, tool output, test commands and PTY work for the initial tool and the v0.1.1 interaction changes. |
| Guidance | `AGENTS.md` specifies shared services, async ownership, offline history and verification expectations; the bundled `go-cli-tui` skill supplies development guidance. |
| Contribution policy | No separate project-wide AI contribution policy was identified in the inspected README, root tree or agent guidance. |
| Review automation | The inspected workflow configures ordinary Go tests, vet, builds and PTY checks. No AI review automation was used to establish implementation assistance. |

The transcript is evidence of a recorded agent implementation workflow, not an
independent attribution audit. Available instructions alone would establish only
guidance. No first-use date, code percentage or bot-review claim is made.
[Committed development record][record], [project guidance][agents],
[development skill][skill], [test workflow][workflow]

## Public milestones found

| Date (UTC) | Event | Evidence |
| --- | --- | --- |
| 2026-09-24 | Source and development transcript published | The verified public default branch includes the [recorded Codex workflow][record] and committed application. |

The recorded session date is also 2026-09-24. The transcript was committed that
day at 13:32:06 UTC; its author and committer timestamps agree. Those timestamps
describe the commit, while the table records the separately verified public
publication date. No earlier public implementation milestone was established.
[Record commit][record-commit]

## Research scope and limits

- Inspected the full revision above, its root tree, README, changelog, module requirements, architecture, configuration, verification notes and workflow. Read the search, history, preview, action/copy, query-completion, popup and disk-usage implementations for the described boundaries.
- Reviewed the six-commit history through the inspected revision, both annotated tags and guidance-path history. The code matches the tagged implementation; subsequent commits add session artifacts and source-install documentation. The bundled skill first appears in `5626619e72eebde18d1fcf9a4edd2c0cd57b280f`; project `AGENTS.md` appears in `bd4bb7c84d2ca62f6393d9123573cf286c4360ab`. These are commit-history observations, not public adoption dates.
- Inspected the one committed development transcript at this revision, including searches for `Codex`, `apply_patch`, `go test -race`, `pty_smoke`, implementation requests and commit commands. Uncommitted session updates were excluded. Development conversations and personal environment values are not reproduced here.
- Verified public repository metadata, default-branch SHA and annotated tag targets on 2026-09-24; a GitHub release-list query returned no releases. No public PR attribution review or exhaustive external search was performed. The first hosted test workflow completed successfully on both Ubuntu and macOS at the inspected revision. [Hosted test run][ci]
- A publication check installed `github.com/daviddwlee84/lazyfind@v0.1.1` from outside a checkout with `GOPROXY=direct` and a fresh temporary `GOBIN`; the installed executable reported `lazyfind version v0.1.1`, and `--help` succeeded. This checks the public source-install path, not an interactive session or binary package. [Installation][readme], [source tag][tag]
- The project's verification notes report macOS arm64 race tests, vet, a v0.1.1 build and 18 real PTY scenario groups. The notes explicitly leave real-server authentication, remote descendant cleanup and installed rga converters unverified; Linux jobs are configured in CI. This catalog review did not rerun the TUI/runtime suite or connect to SSH hosts. [Verification record][verification]

[snapshot]: https://github.com/daviddwlee84/lazyfind/tree/05b7d6e0af2cbf332800abaa8a66e87c967af591
[tag]: https://github.com/daviddwlee84/lazyfind/tree/v0.1.1
[readme]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/README.md
[module]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/go.mod
[architecture]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/docs/architecture.md
[configuration]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/docs/configuration.md
[verification]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/docs/verification.md
[search]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/internal/search/search.go
[completion]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/internal/tui/completion.go
[tui]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/internal/tui/model.go
[actions]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/internal/actions/actions.go
[copy]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/internal/actions/copy.go
[history]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/internal/history/history.go
[preview]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/internal/preview/preview.go
[usage]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/internal/usage/usage.go
[agents]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/AGENTS.md
[skill]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/.agents/skills/go-cli-tui/SKILL.md
[workflow]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/.github/workflows/test.yml
[record]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/.specstory/history/2026-09-24_10-02-41Z-lazyfind-tui-users-zhouhanru.md
[record-commit]: https://github.com/daviddwlee84/lazyfind/commit/540b1ae8f4e709b909f21bab6cd235c81f1b27a8
[skill-license]: https://github.com/daviddwlee84/lazyfind/blob/05b7d6e0af2cbf332800abaa8a66e87c967af591/.agents/skills/go-cli-tui/LICENSE.txt
[ci]: https://github.com/daviddwlee84/lazyfind/actions/runs/36008838994
