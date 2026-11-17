# hemant-plugins

A Claude Code marketplace with three plugins. Each one points to its upstream project.

| Plugin | Upstream | What you get |
|---|---|---|
| ponytail | DietrichGebert/ponytail | Lazy senior dev mode: skills, commands, hooks |
| graphify | Graphify-Labs/graphify | `/graphify` knowledge-graph skill (needs the `graphifyy` CLI) |
| omniroute | cheaper-inference/OmniRoute | MCP server entry and setup skill (needs OmniRoute installed) |

```
/plugin marketplace add hemantmane2113/claude-plugins
/plugin install ponytail@hemant-plugins
/plugin install graphify@hemant-plugins
/plugin install omniroute@hemant-plugins
```

## Prerequisites

**ponytail**: none.

**graphify**: install the upstream CLI first, persistently (not with `uvx`):

```bash
uv tool install graphifyy
graphify install
```

**omniroute**: install and set up the gateway. The plugin only registers its MCP server.

```bash
npm i -g omniroute
omniroute setup
```

The first MCP start can take about 2 minutes while npm installs `omniroute` (it is large). Later starts are fast. Add your own provider accounts and keys in the OmniRoute dashboard.

Upstream licenses: ponytail MIT, graphify Apache-2.0, OmniRoute see its LICENSE. Nothing is copied here.
