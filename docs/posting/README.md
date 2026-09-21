# Posting

[Back to the list](../../README.md) · [Research method](../research-method.md)

| Snapshot | Value |
| --- | --- |
| Upstream | [darrenburns/posting](https://github.com/darrenburns/posting) |
| Reviewed | 2026-09-21 |
| Default branch inspected | `main` |
| Inspected SHA | [`56703a11513e8e74e681b4f859f31945b71e746f`][snapshot] |

## Why it fits

Posting puts request collections, request editing, and response inspection in a
keyboard-oriented HTTP client. Jump mode, a command palette, Vim keys, completion,
and external editor/pager support make actions discoverable. Requests live in
local YAML, so the interface remains connected to inspectable files.
[README][readme]

**Tradeoffs:** a richer persistent request workspace has more configuration than
a one-off command. Environments and pre/post-request Python hooks add power and
behavior to understand. The inspected README officially supports installation
through uv/pipx and explicitly excludes official Homebrew/NixOS support.
[README][readme]

## Agentic development

**Homepage status: Documented use.** The inspected default-branch history contains
a Copilot-attributed code change. Separately, the project has Codex environment
setup and observable review automation.

| Evidence kind | What the public record supports |
| --- | --- |
| Implementation attribution | Commit `596a5153` removes a duplicated application handler and carries a Copilot co-author trailer. This is narrow, self-reported attribution. |
| Guidance/setup | A committed `.codex/environments/environment.toml` defines a development setup command. No root `AGENTS.md` or `CLAUDE.md` was found. |
| Policy | The inspected contribution guide asks for discussion before non-obvious changes and specifies test workflows; no explicit AI contribution policy was found there. |
| Review automation | PR #337 includes Copilot bot reviews. The maintainer also requested Codex review; a request alone does not prove that Codex completed it. |

The OpenAPI implementation in #337 is **not** attributed to Codex merely because
its discussion mentions Codex. Its observed Copilot reviews are review evidence,
separate from the older code commit's co-author trailer.
[Code change][implementation], [review][review], [request][request]

## Public milestones found

| Date (UTC) | Event | Evidence |
| --- | --- | --- |
| 2025-09-12 | Implementation attribution in default-branch history | [Commit `596a5153`][implementation]: Copilot co-author trailer on an application change. Date is the commit's committer timestamp. |
| 2026-03-25 | Agent setup and review automation | [Codex environment commit][environment]; [Copilot review of #337][review]. |

PR chronology (UTC), recorded separately from the milestone labels:

| PR | Opened | Merged |
| --- | --- | --- |
| #337 | 2026-02-15T03:57:26Z | 2026-03-25T22:38:25Z |

## Search boundary and unknowns

Reviewed the full file-name tree, README, contribution guide, and latest 100
commits at the pinned SHA. Inspected the full two cited commits, PR #337, its
issue comments and review records (100-entry caps).

GitHub queries, first 20 results each: commit `repo:darrenburns/posting
"Co-Authored-By"` and merged-PR `"AI"` / `"Codex"` searches returned 1,
0, and 1 total matches. A trailer does not establish autonomous development;
setup files do not establish their execution. No project-wide agent adoption
date or private usage estimate is claimed.

## Sources

- [Snapshot][snapshot], [README][readme], [contribution guide][contributing].
- [Attributed implementation][implementation], [Codex environment][environment].
- [PR #337][openapi], [Copilot review][review], [Codex review request][request].

[contributing]: https://github.com/darrenburns/posting/blob/56703a11513e8e74e681b4f859f31945b71e746f/CONTRIBUTING.md
[implementation]: https://github.com/darrenburns/posting/commit/596a51532ab66c1186261e502060292d51c90fbe
[environment]: https://github.com/darrenburns/posting/commit/a32ad325d1a0f5d41a2b1cfbe78a91294a71dc0d
[openapi]: https://github.com/darrenburns/posting/pull/337
[review]: https://github.com/darrenburns/posting/pull/337#pullrequestreview-4009714472
[request]: https://github.com/darrenburns/posting/pull/337#issuecomment-4129441920

[snapshot]: https://github.com/darrenburns/posting/tree/56703a11513e8e74e681b4f859f31945b71e746f
[readme]: https://github.com/darrenburns/posting/blob/56703a11513e8e74e681b4f859f31945b71e746f/README.md
