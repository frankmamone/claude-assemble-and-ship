# Build your first plugin

This repo is your workspace for the **Unit 9, Lesson 3** task: package some of your own course work into a working Claude Code plugin, then test it locally.

## What to build

A plugin that bundles **at least two different kinds of component** you've already made — for example, a command from Unit 7 and the subagent you built in Unit 8.

## Target structure

```
.
├── .claude-plugin/
│   └── plugin.json        # name + version (the manifest)
├── commands/              # your slash commands (.md)
├── agents/                # your subagents (.md)
└── README.md              # what your plugin does
```

Only create the folders you actually use. Remember the one rule that trips people up: **only `plugin.json` goes inside `.claude-plugin/`** — the component folders sit at the root.

## Steps

1. Create `.claude-plugin/plugin.json` with a `name` and a `version`.
2. Add the component folders you need (`commands/`, `agents/`, …) and move at least two different kinds of component into them.
3. If a hook or command runs a bundled script, reference it through `${CLAUDE_PLUGIN_ROOT}` — never a hardcoded path.
4. Replace this README with one that describes *your* plugin: what it does, the commands it adds, how to use them.
5. From the repo root, load it locally with `claude --plugin-dir .`, then run each piece by its namespaced name (`/your-plugin:its-name`). Use `/reload-plugins` after edits.
6. Commit and push.

## Done when

- `claude --plugin-dir .` loads the plugin and every piece runs by its namespaced name.
- The repo holds a valid `.claude-plugin/plugin.json`, your component folders, and a README describing the plugin.
