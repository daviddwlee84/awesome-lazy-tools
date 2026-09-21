# Designing tools for less remembering and more doing

[Back to the list](../README.md)

The shared idea is **see → select → act → see the result**. The patterns below are editorial synthesis from the linked tools and their documentation, not claims that every tool implements the same keys, layout, or safety policy.

## Keep the decision state visible

[Lazygit](lazygit/README.md) connects resource lists to diffs and actions; [Lazydocker](lazydocker/README.md) connects container state to logs and metrics; [btop](btop/README.md) keeps several system signals visible. The useful commonality is context: users can see what an action would affect without reconstructing it from several commands.

Choose an overview around the actual decision. A monitor benefits from trends and low interruption; a management tool needs precise targets and outcomes. More panes are not inherently better: preserve a useful narrow-screen path and a clear focus indicator.

## Make speed discoverable

[K9s](k9s/README.md), [Yazi](yazi/README.md), and Lazygit offer different navigation vocabularies. Borrow contextual help, filtering, and stable pane roles before borrowing a particular keymap. Keep typing separate from global shortcuts, and show only actions that apply to the current target.

For a new tool, test the full sequence: discover an action, select its target, inspect the relevant detail, execute or cancel, and locate the result. Retaining selection by object identity makes refresh less disorienting than retaining a row number.

## Show work without blocking exploration

Yazi's asynchronous design and [dev-cli](dev-cli/README.md)'s dashboard workflow provide useful starting points for thinking about responsiveness. Show available state first; make pending work and stale data legible. A spinner alone does not make blocking discovery responsive.

In your implementation, distinguish successful empty results from failures, correlate late responses with the request that produced them, and keep navigation usable during I/O. These are design recommendations; validate them in the target tool instead of inferring behavior from a screenshot.

## Compose focused surfaces

[Television](television/README.md) and [fzf](fzf/README.md) demonstrate a compact source → filter → preview → action workflow. [LazyVim](lazyvim/README.md) is a configured editor environment, while [lazy.nvim](lazy-nvim/README.md) manages plugins. Neither has to be recast as a domain dashboard to be useful here.

A picker suits a short selection; a wizard suits a sequence of choices; a dashboard suits repeated inspection and operations. Keep CLI and machine-readable paths available where the domain permits them. Let a focused tool hand off to an editor or another interface while preserving the user's working context.

## Make consequences legible

Before a destructive operation, show the exact target and consequence. After any operation, report the result where the user is still looking. Routine navigation should stay immediate. A failed or cancelled request should not silently discard useful context.

Whether confirmation, undo, preview, or a review step fits best depends on the action. Do not copy another tool's deletion key or confirmation policy without checking your own domain.

## Compare patterns, not scores

| Question | Reference surfaces | Tradeoff to examine |
| --- | --- | --- |
| What must remain visible? | Lazygit, Lazydocker, btop. | Overview density versus detail and small terminals. |
| How does the next action become discoverable? | Lazygit, K9s, Yazi. | Contextual hints versus shortcut density. |
| How much interface does the task need? | Television, fzf, dev-cli. | One-shot selection versus a persistent workspace. |
| What survives a refresh or handoff? | Yazi, dev-cli. | Context continuity versus fresh state. |
| Who owns configuration and integration? | LazyVim, lazy.nvim, lazychezmoi. | Convenient defaults versus explicit ownership and reproducibility. |

## Turn an observation into a reusable lesson

Record the tool, inspected version, complete interaction, useful behavior, and downside in its research page. Add a general principle here only when the evidence supports it. For Go implementation work, the [companion skill](building-tools.md) already covers navigation, asynchronous state, terminal ownership, distribution, and verification.

Agentic-development history is a separate source of lessons: inspect what instructions say, what contributors demonstrably did, and what humans retained responsibility for. The existence of a policy does not establish that it was followed on every change.
