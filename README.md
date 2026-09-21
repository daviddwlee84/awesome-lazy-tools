# Awesome Lazy Tools [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

Terminal tools that make complex workflows visible, navigable, and actionable: **see → select → act → see the result**.

“Lazy” describes an interaction philosophy, not a shared organization, implementation language, or required name prefix. This collection favors useful overviews, fast context changes, discoverable controls, and clear feedback. Editor setups and composable pickers have their own section.

<!-- The age check is an admission rule for the main Awesome directory. This independent list is new and is not submitting there. Re-enable before any future submission. -->
<!--lint disable awesome-git-repo-age-->

## Contents

- [Version Control and Workflows](#version-control-and-workflows)
- [Containers and Task Queues](#containers-and-task-queues)
- [Files, Dotfiles, and System Monitoring](#files-dotfiles-and-system-monitoring)
- [Data and Logs](#data-and-logs)
- [Networking and APIs](#networking-and-apis)
- [Editors and Composable Pickers](#editors-and-composable-pickers)
- [Learn and Build](#learn-and-build)
- [Maintainer Projects](#maintainer-projects)
- [Related Collections](#related-collections)

Research reviewed on **2026-09-21**. Agentic development is a research dimension, **not an inclusion requirement or quality score**. Status links open the evidence notes. Dates identify events found in a bounded review, not claims about a project's first private use of AI. “Guidance found” describes instructions; “documented use” requires implementation evidence; “automation found” covers AI review or documentation workflows. A missing date means unknown. The research method below explains dates, policies, and limitations.

## Version Control and Workflows

| Tool                                                | Purpose / lazy traits                                                                        | Agentic development                               | Public milestones found                                        |
| --------------------------------------------------- | -------------------------------------------------------------------------------------------- | ------------------------------------------------- | -------------------------------------------------------------- |
| [Lazygit](https://github.com/jesseduffield/lazygit) | Git status, diffs, branches, and contextual actions in one workspace.                        | [Documented use](docs/lazygit/README.md)          | Implementation merged: 2026-03-07; guidance merged: 2026-05-04 |
| [lazyjj](https://github.com/Cretezy/lazyjj)         | Jujutsu changes, log, and bookmarks around the existing jj CLI.                              | [No public evidence found](docs/lazyjj/README.md) | —                                                              |
| [gh-dash](https://github.com/dlvhdr/gh-dash)        | GitHub pull requests and issues with configurable sections and actions.                      | [Documented use](docs/gh-dash/README.md)          | Implementation merged: 2026-04-05; policy merged: 2026-06-05   |
| [dev-cli](https://github.com/daviddwlee84/dev-cli)  | Repositories, worktrees, tasks, and runtimes in a shared CLI/dashboard workflow.             | [Documented use](docs/dev-cli/README.md)          | Attributed merge commit: 2026-09-19                            |
| [exp-cli](https://github.com/daviddwlee84/exp-cli)  | Git-based research workflow with a read-only overview and interactive commands; early stage. | [Documented use](docs/exp-cli/README.md)          | Attributed implementation commit: 2026-08-29                   |

## Containers and Task Queues

| Tool                                                      | Purpose / lazy traits                                                              | Agentic development                           | Public milestones found                                |
| --------------------------------------------------------- | ---------------------------------------------------------------------------------- | --------------------------------------------- | ------------------------------------------------------ |
| [Lazydocker](https://github.com/jesseduffield/lazydocker) | Docker and Compose resources beside logs, metrics, and common actions.             | [Documented use](docs/lazydocker/README.md)   | Guidance committed / implementation merged: 2026-04-19 |
| [K9s](https://github.com/derailed/k9s)                    | Browse and operate Kubernetes resources with continuously updated cluster context. | [Documented use](docs/k9s/README.md)          | Implementation merged: 2026-01-03                      |
| [lazypueue](https://github.com/daviddwlee84/lazypueue)    | Pueue queues across hosts, task details, logs, and guided actions; early stage.    | [Documented use](docs/lazypueue/README.md)    | Source / transcript published: 2026-09-21              |

## Files, Dotfiles, and System Monitoring

| Tool                                                       | Purpose / lazy traits                                                                      | Agentic development                            | Public milestones found                                           |
| ---------------------------------------------------------- | ------------------------------------------------------------------------------------------ | ---------------------------------------------- | ----------------------------------------------------------------- |
| [Yazi](https://github.com/sxyazi/yazi)                     | Asynchronous file navigation, previews, and task progress; upstream labels it public beta. | [Documented use](docs/yazi/README.md)          | Implementation merged: 2025-09-04; guidance committed: 2026-07-25 |
| [lazychezmoi](https://github.com/daviddwlee84/lazychezmoi) | Inspect dotfile state and diffs before editing or applying selected changes; early stage.  | [Documented use](docs/lazychezmoi/README.md)   | Source / transcript published: 2026-09-21                         |
| [btop](https://github.com/aristocratos/btop)               | CPU, memory, disks, network, and processes in a persistent monitoring overview.            | [Documented use](docs/btop/README.md)          | Policy committed: 2025-12-04; implementation merged: 2026-05-01   |

## Data and Logs

| Tool                                                     | Purpose / lazy traits                                                                             | Agentic development                            | Public milestones found                                                       |
| -------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ---------------------------------------------- | ----------------------------------------------------------------------------- |
| [lazysql](https://github.com/jorgerojas26/lazysql)       | Database browsing, query editing, and results with keyboard navigation; upstream labels it alpha. | [Documented use](docs/lazysql/README.md)       | Assisted fix merged: 2026-02-27; agent editor merged: 2026-05-25              |
| [lazymlflow](https://github.com/daviddwlee84/lazymlflow) | Browse experiments, compare runs, and inspect artifacts and datasets; early stage.                | [Documented use](docs/lazymlflow/README.md)    | Source / transcript published: 2026-09-21                                     |
| [VisiData](https://github.com/saulpw/visidata)           | Explore tabular data through selections, filters, summaries, and transformations.                 | [Documented use](docs/visidata/README.md)      | Guidance committed: 2026-02-03; implementation merged: 2026-06-22             |
| [lnav](https://github.com/tstack/lnav)                   | Explore merged log timelines with filters and SQL analysis.                                       | [Documented use](docs/lnav/README.md)          | Codex-assisted fix merged: 2026-07-16; Claude-assisted fix merged: 2026-08-24 |
| [lazyjournal](https://github.com/Lifailon/lazyjournal)   | Browse and filter system, file, container, and Kubernetes logs.                                   | [Automation found](docs/lazyjournal/README.md) | AI review workflow committed: 2026-01-23                                      |

## Networking and APIs

| Tool                                                   | Purpose / lazy traits                                                                      | Agentic development                          | Public milestones found                                                       |
| ------------------------------------------------------ | ------------------------------------------------------------------------------------------ | -------------------------------------------- | ----------------------------------------------------------------------------- |
| [lazyssh](https://github.com/Adembc/lazyssh)           | Discover SSH hosts and common connection workflows from a terminal interface.              | [Automation found](docs/lazyssh/README.md)   | PR with automated summary merged: 2025-09-19                                  |
| [lazyclash](https://github.com/daviddwlee84/lazyclash) | Inspect and operate existing Mihomo cores through proxies, traffic, connections, and logs. | [Guidance found](docs/lazyclash/README.md)   | Guidance / agent interface committed: 2026-09-20                              |
| [Trippy](https://github.com/fujiapple852/trippy)       | Network diagnostics combining traceroute and ping in a live view.                          | [Documented use](docs/trippy/README.md)      | Codex-linked fix merged: 2025-06-04; assisted localization merged: 2026-04-05 |
| [Posting](https://github.com/darrenburns/posting)      | Keyboard-oriented HTTP requests, collections, and response inspection.                     | [Documented use](docs/posting/README.md)     | Attributed code commit: 2025-09-12; setup / review: 2026-03-25                |

## Editors and Composable Pickers

These extend the philosophy in different ways: a configured working environment, a plugin manager, or a reusable selection surface.

| Tool                                                       | Purpose / lazy traits                                                              | Agentic development                                  | Public milestones found                                        |
| ---------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------- | -------------------------------------------------------------- |
| [LazyVim](https://github.com/LazyVim/LazyVim)              | Neovim distribution that assembles editor features and discoverable workflows.     | [Documented use](docs/lazyvim/README.md)             | Attributed merge: 2025-10-20; generated commit: 2025-10-24     |
| [lazy.nvim](https://github.com/folke/lazy.nvim)            | Neovim plugin manager with a management UI, lazy loading, lockfile, and profiling. | [No public evidence found](docs/lazy-nvim/README.md) | —                                                              |
| [Television](https://github.com/alexpasmantier/television) | Fuzzy selection and preview across reusable, configurable data-source channels.    | [Documented use](docs/television/README.md)          | Docs disclosure: 2025-06-27; implementation merged: 2026-02-04 |
| [fzf](https://github.com/junegunn/fzf)                     | Composable fuzzy selection with previews and action bindings for shell workflows.  | [No public evidence found](docs/fzf/README.md)       | Policy committed: 2026-03-20                                   |

## Learn and Build

Read the [design guide](docs/design-guide.md) for interaction patterns, tradeoffs, and questions to take back to your own tools.

The [agentic development research method](docs/research-method.md) explains evidence standards and a repeatable workflow. Each status link above opens a tool's notes; Lazygit has the first detailed case study.

[Build a Go CLI or TUI](docs/building-tools.md) with the companion development skill, maintained alongside this collection.

## Maintainer Projects

This list's maintainer also maintains **dev-cli, exp-cli, lazychezmoi, lazyclash, lazymlflow, and lazypueue**. They follow the same inclusion and evidence rules as other entries. New public source repositories are not automatically stable releases. Their notes describe the inspected version and known limitations.

## Related Collections

- [Awesome TUI](https://github.com/alvinunreal/awesometui) - Broad catalog of terminal user interfaces.
- [Awesome TUI Design](https://github.com/cola-runner/awesome-tui-design) - Terminal interface design references for coding agents.
- [Awesome Terminal Aesthetics](https://github.com/kud/awesome-terminal-aesthetics) - Tools and frameworks for terminal presentation.

## Contributing

Read the [contribution guide](CONTRIBUTING.md) and start with the [tool research template](docs/_template.md). Add a useful recommendation and evidence, not just another link.
