# claude-plugins

A Claude Code marketplace with three plugins. Each one points to its upstream project.

| Plugin | Upstream | What you get |
|---|---|---|
| ponytail | DietrichGebert/ponytail | Lazy senior dev mode: skills, commands, hooks |
| graphify | Graphify-Labs/graphify | `/graphify` knowledge-graph skill (needs the `graphifyy` CLI) |
| omniroute | cheaper-inference/OmniRoute | MCP server entry and setup skill (needs OmniRoute installed) |

```
/plugin marketplace add hemantmane2113/claude-plugins
/plugin install ponytail@claude-plugins
/plugin install graphify@claude-plugins
/plugin install omniroute@claude-plugins
```

Upstream licenses: ponytail MIT, graphify Apache-2.0, OmniRoute see its LICENSE. Nothing is copied here.
