# pi-ask-user-question

Interactive `ask_user_question` tool for [pi](https://pi.dev) — pause the agent and ask the user one question via TUI.

Modes: free-text (`ctx.ui.editor`), single-select list, multi-select checklist. All modes support `Other` custom input, `Esc` cancel, and serialize through a shared UI lock.

## Install

From this repo checkout:

```bash
pi install ./pi-ask-user-question
```

Project-local only:

```bash
pi install -l ./pi-ask-user-question
```

Try once without installing:

```bash
pi -e ./pi-ask-user-question
```

Manage:

```bash
pi list
pi update
pi remove ./pi-ask-user-question
```

## Layout

```
pi-ask-user-question/
├── package.json                    # pi-package manifest (pi.extensions)
└── extensions/
    └── ask-user-question.ts        # the extension (model-only, read-only tool)
```

Requires pi `^1.1.0`. Host packages (`@earendil-works/pi-coding-agent`, `@earendil-works/pi-tui`, `typebox`) are `peerDependencies` — do not put them in `dependencies`.
