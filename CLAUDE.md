# gstack development

## Commands

```bash
bun install          # install dependencies
bun test             # run integration tests (browse + snapshot)
bun run dev <cmd>    # run CLI in dev mode, e.g. bun run dev goto https://example.com
```

## Project structure

```
gstack/
├── .claude-plugin/  # Plugin marketplace + manifest
│   ├── marketplace.json
│   └── plugin.json
├── browse/          # Headless browser CLI (Playwright)
│   ├── src/         # CLI + server + commands
│   └── test/        # Integration tests + fixtures
├── ship/            # Ship workflow skill
├── review/          # PR review skill
├── plan-ceo-review/ # /plan-ceo-review skill
├── plan-eng-review/ # /plan-eng-review skill
├── retro/           # Retrospective skill
├── SKILL.md         # Browse skill (Claude discovers this)
└── package.json
```

## Installing as a plugin

```
/plugin marketplace add garrytan/gstack
/plugin install gstack@gstack
```

## Deploying to the active skill

Push your branch, then run `/plugin marketplace update gstack` to pull the latest.
