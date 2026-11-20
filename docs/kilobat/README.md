# Kilobat CLI

[Back to the list](../../README.md) · [Research method](../research-method.md)

Maker-contributed research, prepared with Codex assistance. The local observations below were automated checks, not an independent user study.

| Field | Record |
| --- | --- |
| Upstream | [seifip/kilobat-cli](https://github.com/seifip/kilobat-cli) |
| Reviewed | 2026-11-02 (UTC). |
| Inspected revision | [`3145806fc8f921833e6fc483e11422fa848e6163`][snapshot], the default branch at review time. |
| Interface | A keyboard menu that dispatches Mac network checks, plus CLI reports and local stdio MCP. |
| Distribution | Public release [0.20.0][release]; Homebrew builds from source. |

## Why it fits

The menu presents common checks with short descriptions and persistent keyboard hints. Arrow keys or `j`/`k` select a row; Enter dispatches its command, number keys open a choice directly, and `q` exits. One-shot output waits for a key before returning; watch commands return to the menu when they finish. These dispatch and return paths were inspected in [the implementation][menu].

**Hands-on, 2026-11-02:** the installed 0.20.0 menu moved between Live monitor and Speed test and exited cleanly in a native PTY. The [original recording][capture] shows navigation only; it does not demonstrate the selected tools running. Separate CLI checks against `example.com` and `service.invalid` returned a successful report with exit 0 and a DNS-failure finding with exit 1 respectively; IPv6 was skipped in the successful check. The [worked adapter and dated results][probe] preserve those distinctions.

## Design lessons and tradeoffs

**Design interpretation:** pairing action names with the check's purpose makes the entry menu useful before the user knows the command syntax. A small menu can make a larger CLI easier to explore without hiding the underlying commands.

The platform and companion boundaries remain significant. The public CLI is GPL-3.0-only and requires macOS 14+; the Homebrew source build needs Xcode 16+/Swift 6. Some Wi-Fi and traffic features depend on macOS permissions or the separately proprietary desktop app. The open-source CLI does not establish an open-source desktop application. Settings-changing commands are included, so MCP setup is not a read-only capability claim. [Upstream README][readme], [package manifest][package], [MCP implementation][mcp].

## Agentic development

**Homepage status: Documented use.** Public source-update commits carry self-reported Claude co-author trailers. The inspected [0.2.0 update][early-commit] changes Swift implementation and tests as well as documentation. Its trailer is an attribution disclosure, not an independent measurement of agent-written code or proof of which lines an agent produced. The [0.20.0 update][release-commit] also carries a Claude co-author trailer.

| Date (UTC) | Event type | Finding and primary source |
| --- | --- | --- |
| 2026-10-28 | Source-update commit, committer timestamp | [Commit `ff78ec32`][early-commit] contains a Claude co-author trailer; this is the earliest such trailer found in the bounded review below. |
| 2026-11-02 | Documentation PR merged | [PR #1][docs-pr] merged MCP discovery/setup documentation; its [CodeRabbit bot comment][review-comment] is separate review automation evidence. |

The agent-facing MCP interface is a product capability, not evidence of who implemented it. No project-local `AGENTS.md`, `CLAUDE.md`, contribution guide, or `.github` guidance path was found in the inspected tree. The owner-level `.github` repository returned 404. These observations do not establish historical absence, private agent use, or an unrestricted contribution policy.

## Research scope and limits

Reviewed the default README, license, package manifest, menu/terminal code, MCP code, release metadata and the 175-path public tree. The implementation, terminal, MCP, manifest and license blob IDs match the tested 0.20.0 release snapshot; the default README has a later documentation correction.

The default-branch commits API was queried with `per_page=100`; it returned 26 records and no next-page link. Commit messages were searched for Claude co-author trailers, and the earliest matching commit's changed files were inspected. PR #1's merged state, merge timestamp and bot comment were checked separately. Commit timestamps are not release-publication or first-use dates. Deleted branches, private development records and the proprietary companion's history were outside this review.

Only menu navigation/exit and the two host reports above were observed locally. An earlier custom PTY harness timed out waiting for exit; a native PTY exited cleanly, and the cause of the harness difference was not established. Full menu actions, Wi-Fi permissions, filtering, every MCP tool, named-agent integration and production use were not tested. No private configuration or network identifiers are included.

## Sources

- [Pinned upstream tree][snapshot], [README][readme] and [license][license].
- [Menu implementation][menu], [terminal implementation][terminal] and [MCP implementation][mcp].
- [Public release][release], [source-install tap](https://github.com/seifip/homebrew-kilobat), [original menu recording][capture] and [worked diagnostic adapter][probe].

[snapshot]: https://github.com/seifip/kilobat-cli/tree/3145806fc8f921833e6fc483e11422fa848e6163
[readme]: https://github.com/seifip/kilobat-cli/blob/3145806fc8f921833e6fc483e11422fa848e6163/README.md
[license]: https://github.com/seifip/kilobat-cli/blob/3145806fc8f921833e6fc483e11422fa848e6163/LICENSE
[package]: https://github.com/seifip/kilobat-cli/blob/3145806fc8f921833e6fc483e11422fa848e6163/Package.swift
[menu]: https://github.com/seifip/kilobat-cli/blob/3145806fc8f921833e6fc483e11422fa848e6163/Sources/KilobatCLI/KilobatCLI.swift#L417-L448
[terminal]: https://github.com/seifip/kilobat-cli/blob/3145806fc8f921833e6fc483e11422fa848e6163/Sources/KilobatCLI/Terminal.swift
[mcp]: https://github.com/seifip/kilobat-cli/blob/3145806fc8f921833e6fc483e11422fa848e6163/Sources/KilobatCore/Services/MCPServer.swift
[early-commit]: https://github.com/seifip/kilobat-cli/commit/ff78ec323a024997d965644588df85eda744a993
[release-commit]: https://github.com/seifip/kilobat-cli/commit/9bf0b7aaeddcff288db0195b47da6cc579b30376
[release]: https://github.com/seifip/kilobat-cli/releases/tag/v0.20.0
[docs-pr]: https://github.com/seifip/kilobat-cli/pull/1
[review-comment]: https://github.com/seifip/kilobat-cli/pull/1#issuecomment-6566367751
[capture]: https://raw.githubusercontent.com/seifip/My-Awesome-TUIs/ed9345eced49c53f63bba348f74acf7bedb78b4b/imgs/Kilobat-CLI.gif
[probe]: https://gist.github.com/seifip/fa05e77888fc8ec0e99463084f056ae6#file-readme-md
