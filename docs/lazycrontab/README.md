# lazycrontab

[Back to the list](../../README.md) · [Research method](../research-method.md)

| Snapshot | Value |
| --- | --- |
| Canonical upstream | [daviddwlee84/lazycrontab](https://github.com/daviddwlee84/lazycrontab) |
| Reviewed | 2026-09-24 (UTC) |
| Tagged revision inspected | [`b649039c051a4a2dfab40fb23ba1b56a0d222658`][snapshot] |
| Public tag | Annotated [`v0.1.0`][tag] |
| Interface | Cron management CLI and terminal dashboard |
| Stage | Initial public source tag; no binary distribution or GitHub Release |
| License and build | MIT; Go 1.26.6+, `go build -o lazycrontab .` or `go install .` from a checkout |

This project is maintained by the maintainer of this collection. Its public
repository and annotated `v0.1.0` tag were verified on 2026-09-24. This is an
initial source-only version, not a claim of mature releases or packaged binaries.

The tag resolves to the revision above. Its release preparation changes only
the README, changelog and verification notes relative to implementation snapshot
`bce52b0bea8cc779a12b12a379083f6eea9e282f`. [Tagged source][snapshot],
[changelog][changelog]

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
entire fleet automatically. These are source observations at the pinned
revision, supported by the inspected files listed below. [README][readme], [architecture][architecture]

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

The initial version uses Go source installation; binary archives and a Homebrew
formula are not included. The README documents the pinned install command
`go install github.com/daviddwlee84/lazycrontab@v0.1.0`. The source updater's
latest-release lookup additionally requires a stable GitHub Release, which was
not published with this tag. This catalog review did not independently test a
public Go install or the updater. [Installation][readme], [updater][updater]

## Agentic development

**Homepage status: Not reviewed.** This publication update verified the source
repository and tag, but did not complete a public agentic-development review.
Published [`AGENTS.md`][agents] contains implementation and verification guidance.
The project has been developed with coding-agent assistance; the catalog does
not infer an implementation milestone from guidance alone.

No first-use date, agent-written percentage or review-automation claim is made.
Public development records and attribution history remain to be reviewed under
this collection's research method; development conversations are not reproduced
in this dossier.

## Research scope and limits

- Pinned the tagged revision above and inspected its [README][readme], [changelog][changelog], [MIT license][license], [go.mod][module], [AGENTS.md][agents], [architecture][architecture], [compatibility][compatibility] and [verification notes][verification].
- Inspected [`internal/ui/form_rows.go`][form-rows], [`internal/ui/form_popup.go`][form-popup], [`internal/cli/job_form.go`][job-form], [`internal/cli/job_values.go`][job-values], [`internal/service/raw_source.go`][raw-source] and [`internal/service/managed_script.go`][managed-script] for the described interaction and write boundaries.
- Read eight recent commit subjects at the implementation snapshot, enumerated tracked guidance/development-record paths, and inspected the subsequent release-document diff and annotated `v0.1.0` tag. This is not a complete history audit; commit and tag timestamps are not publication dates.
- Verified public repository metadata, the default branch and annotated tag target after publication. No public PR attribution review or exhaustive history audit was performed. Hosted Actions results were not assessed in this catalog update.
- The project's local verification notes report macOS/Linux race tests, vet, builds and isolated PTY coverage. The tag annotation records exact-source installation through an isolated file-backed Go proxy with Go 1.26.6, module-version checks, embedded help, schedule previews, completion checks and a clean source-archive build. These are local verification records, not a successful public installation or CI run. This catalog addition did not repeat those runtime checks or execute user jobs, SSH fleet operations, cron daemons or Pueue submissions.

A later research refresh should review public implementation evidence and
attribution before assigning an agentic milestone. Binary packaging, hosted CI
results and the GitHub Release channel require separate verification.

[snapshot]: https://github.com/daviddwlee84/lazycrontab/tree/b649039c051a4a2dfab40fb23ba1b56a0d222658
[tag]: https://github.com/daviddwlee84/lazycrontab/tree/v0.1.0
[readme]: https://github.com/daviddwlee84/lazycrontab/blob/b649039c051a4a2dfab40fb23ba1b56a0d222658/README.md
[changelog]: https://github.com/daviddwlee84/lazycrontab/blob/b649039c051a4a2dfab40fb23ba1b56a0d222658/CHANGELOG.md
[architecture]: https://github.com/daviddwlee84/lazycrontab/blob/b649039c051a4a2dfab40fb23ba1b56a0d222658/docs/architecture.md
[updater]: https://github.com/daviddwlee84/lazycrontab/blob/b649039c051a4a2dfab40fb23ba1b56a0d222658/internal/upgrade/upgrade.go
[agents]: https://github.com/daviddwlee84/lazycrontab/blob/b649039c051a4a2dfab40fb23ba1b56a0d222658/AGENTS.md
[license]: https://github.com/daviddwlee84/lazycrontab/blob/b649039c051a4a2dfab40fb23ba1b56a0d222658/LICENSE
[module]: https://github.com/daviddwlee84/lazycrontab/blob/b649039c051a4a2dfab40fb23ba1b56a0d222658/go.mod
[compatibility]: https://github.com/daviddwlee84/lazycrontab/blob/b649039c051a4a2dfab40fb23ba1b56a0d222658/docs/compatibility.md
[verification]: https://github.com/daviddwlee84/lazycrontab/blob/b649039c051a4a2dfab40fb23ba1b56a0d222658/docs/verification.md
[form-rows]: https://github.com/daviddwlee84/lazycrontab/blob/b649039c051a4a2dfab40fb23ba1b56a0d222658/internal/ui/form_rows.go
[form-popup]: https://github.com/daviddwlee84/lazycrontab/blob/b649039c051a4a2dfab40fb23ba1b56a0d222658/internal/ui/form_popup.go
[job-form]: https://github.com/daviddwlee84/lazycrontab/blob/b649039c051a4a2dfab40fb23ba1b56a0d222658/internal/cli/job_form.go
[job-values]: https://github.com/daviddwlee84/lazycrontab/blob/b649039c051a4a2dfab40fb23ba1b56a0d222658/internal/cli/job_values.go
[raw-source]: https://github.com/daviddwlee84/lazycrontab/blob/b649039c051a4a2dfab40fb23ba1b56a0d222658/internal/service/raw_source.go
[managed-script]: https://github.com/daviddwlee84/lazycrontab/blob/b649039c051a4a2dfab40fb23ba1b56a0d222658/internal/service/managed_script.go
