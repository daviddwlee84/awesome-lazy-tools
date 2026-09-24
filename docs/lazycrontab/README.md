# lazycrontab

[Back to the list](../../README.md) · [Research method](../research-method.md)

| Snapshot | Value |
| --- | --- |
| Intended upstream | `daviddwlee84/lazycrontab`; no public repository verified |
| Reviewed | 2026-09-24 (UTC) |
| Local tagged revision inspected | `b649039c051a4a2dfab40fb23ba1b56a0d222658` |
| Local tag | Annotated `v0.1.0`, not published |
| Interface | Cron management CLI and terminal dashboard |
| Stage | Local v0.1.0 source tag; public repository, tag, release and CI remain unverified |
| License and build | MIT; Go 1.26.6+, `go build -o lazycrontab .` or `go install .` from a supplied checkout |

This project is maintained by the maintainer of this collection. Its list entry
links here rather than to an unverified upstream URL. The module names the
intended GitHub location above, but the inspected checkout has no configured Git
remote and the GitHub repository lookup did not resolve it. A local commit or
tag does not establish public availability. These notes describe local source,
not a publicly installable release.

The annotated local `v0.1.0` tag resolves to the revision above. Its release
preparation changes only the README, changelog and verification notes relative
to implementation snapshot `bce52b0bea8cc779a12b12a379083f6eea9e282f`.

## Why it fits

The inspected implementation keeps hosts/sources, jobs and selected-job details
together, with readable cron descriptions, next occurrences, search, a weekly
forecast and an exact agenda. Its persistent Playground shares a field-based
cron editor with job forms; a tested expression can populate a new-job draft.
CLI commands and dashboard actions use the same planning and service layer.

The add/edit workflow distinguishes one-line commands, existing script files and
managed multiline shell content. Script presets expose runtimes, working
directories and Python/uv project choices. Review shows proposed changes before
the source is installed; results distinguish saved, failed and uncertain writes.
SSH discovery starts from selected existing aliases rather than registering an
entire fleet automatically. These are local source observations, supported by
the inspected files listed below.

## Design observations and tradeoffs

**Interpretation:** keeping form values, rendered rows and focusable fields
separate makes conditional workflows easier to follow. Mutually exclusive
payloads share one position, unused script details retain blank space, and
inapplicable queue settings remain visible with a reason. Arrow navigation and
mouse targets follow the same row model; retained inactive drafts do not alter
the selected task's execution plan.

The tool manages native user crontabs and explicitly registered Supercronic
files on Linux/macOS; system sources are read-only. Fleet visibility does not
create a central scheduler. Writes target one source, preserve unrelated bytes,
check the reviewed revision, back up original content and verify read-back.
Native crontab installation still cannot provide an atomic compare-and-swap
against an unrelated editor.

Optional Pueue integration needs a 4.x client and daemon on the selected host;
queued work is distinct from completed work. Managed scripts use immutable
versions in the target's XDG data directory, retained for existing queue tasks
and backups. Automatic pruning is absent. Forecasts are expected trigger times,
not proof that a daemon executed a job; file inspection cannot recover an
existing Supercronic container's complete runtime environment.

The initial release uses Go source installation; binary archives and a Homebrew
formula are not included. Public versioned installation requires publication of
the repository and tag. The source updater's latest-release lookup additionally
requires a stable GitHub Release. A successful private source-proxy check does
not establish that either public route works.

## Agentic development

**Homepage status: Not reviewed.** A public agentic-development review could not
be completed because no public source revision was verified. This is not a
negative finding about private agent use.

Local `AGENTS.md` provides implementation and verification guidance, and the
project has been developed with coding-agent assistance. Neither this local
observation nor local instructions establish a public implementation milestone.
No public contribution policy, AI review automation, first-use date or
agent-written percentage is claimed. Private development conversations are not
reproduced in this dossier.

## Research scope and limits

- Pinned the local tagged revision above and inspected its README, changelog, MIT license, `go.mod`, `AGENTS.md`, architecture, compatibility and verification notes.
- Inspected `internal/ui/form_rows.go`, `internal/ui/form_popup.go`, `internal/cli/job_form.go`, `internal/cli/job_values.go`, `internal/service/raw_source.go` and `internal/service/managed_script.go` for the described interaction and write boundaries.
- Read eight recent commit subjects at the implementation snapshot, enumerated tracked guidance/development-record paths, and inspected the subsequent release-document diff and annotated `v0.1.0` tag. This is not a complete history audit; local commit and tag timestamps are not publication dates.
- Checked configured remotes and queried `gh repo view daviddwlee84/lazycrontab`; no remote was configured and the repository lookup did not resolve. No public commits, PRs, releases or Actions runs could be inspected.
- The project's local verification notes report macOS/Linux race tests, vet, builds and isolated PTY coverage. The local tag annotation records exact-source installation through an isolated file-backed Go proxy with Go 1.26.6, module-version checks, embedded help, schedule previews, completion checks and a clean source-archive build. These are local verification records, not a successful public installation or CI run. This catalog addition did not repeat those runtime checks or execute user jobs, SSH fleet operations, cron daemons or Pueue submissions.

Publication remains the next verification boundary: confirm the canonical
repository and released commit, replace the local-only entry link with the
verified upstream, and perform the public evidence review before adding a
milestone date or permanent source links.
