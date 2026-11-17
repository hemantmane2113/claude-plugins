---
name: graphify
description: Use for questions about a codebase's architecture or file relationships, or when the user types /graphify. Builds and queries a knowledge graph of code, docs, PDFs and images with the upstream graphify CLI.
---

# graphify

This skill is a thin wrapper. The real tool is the upstream graphify CLI
(https://github.com/Graphify-Labs/graphify).

## Steps

1. Check the CLI: `command -v graphify`. If missing, install it persistently:
   `uv tool install graphifyy` (or `pipx install graphifyy`). Do not use `uvx`.
2. Install the upstream skill and hooks for Claude Code once per machine: `graphify install`
   (per project: `graphify claude install --project`). This gives you the full `/graphify`
   workflow, including the pre-search hooks.
3. Build the graph: `graphify extract <path>` or follow the upstream `/graphify` skill.
   Code is parsed locally. Docs, PDFs and images use a model for a semantic pass.
4. Answer architecture questions from `graphify-out/GRAPH_REPORT.md` and by querying the
   graph before grepping files. Edges tagged `INFERRED` are guesses; say so.

Remove with `graphify uninstall` (add `--purge` to delete `graphify-out/`).
