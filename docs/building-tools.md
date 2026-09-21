# Build a Go CLI or TUI

[Back to the list](../README.md)

The companion [go-cli-tui skill](../skills/go-cli-tui/SKILL.md) turns the see → select → act → feedback philosophy into practical guidance for Go commands, pickers, wizards, and dashboards. It is a self-contained instruction package, not a generator, application framework, or required dependency of the listed tools.

## Install

From the canonical source, in the project where you are building a tool:

```sh
npx --yes skills@1.7.0 add daviddwlee84/awesome-lazy-tools/skills/go-cli-tui --skill go-cli-tui --agent codex claude-code --yes
```

The same named skill is distributed by the maintainer's broader collection:

```sh
npx --yes skills@1.7.0 add daviddwlee84/agent-skills/skills/owned/go-cli-tui --skill go-cli-tui --agent codex claude-code --yes
```

Choose one source per consuming project. These commands install in project scope; do not add `--global` unless that is your intent. Review the installed files and lock changes. The package's relative references travel with it and do not require cloning this entire catalog.

## Ownership

| Location | Role |
| --- | --- |
| `awesome-lazy-tools/skills/go-cli-tui/` | Canonical source; make instruction changes here. |
| `agent-skills/skills/owned/go-cli-tui/` | Reviewed distribution copy; synced from a recorded upstream commit. |
| A consumer's `.agents/skills/go-cli-tui/` | Installed snapshot; update through the installer and review its lock. |

The skill keeps its existing `go-cli-tui` identity. The move from the collection's `local` to `owned` category changes its source path, not what the skill does. The initial transfer preserves its existing references and adds an explicit MIT license.

The initial source snapshot is [agent-skills commit ac08a157](https://github.com/daviddwlee84/agent-skills/tree/ac08a1575d5e1cc8f835db465f9b81759e078fb9/skills/local/go-cli-tui). Later changes belong in this repository's canonical package.

## Update loop

1. Edit and validate the canonical package here. Keep it usable without the rest of this repository; link optional research rather than requiring all dossiers to be loaded.
2. Publish that source commit.
3. In the agent-skills collection, run `./scripts/sync-vendor.sh --check go-cli-tui`, then `./scripts/sync-vendor.sh go-cli-tui`.
4. Review the mirrored changes and upstream SHA; run `make validate` and `make docs-build` there, then publish the collection update.
5. Update consumers through their chosen source. Check for local edits before an installer replaces the skill directory; never hand-edit generated hashes.

The collection's existing weekly sync workflow also proposes updates. Its [owned-skills workflow](https://github.com/daviddwlee84/agent-skills/blob/main/docs/workflows/adding-owned-skills.md) is authoritative for the distribution mechanism.

Research belongs in `docs/<tool>/`; reusable implementation guidance belongs in the skill. Keep project-specific agent policies out of the general skill unless a concrete lesson warrants an optional reference.
