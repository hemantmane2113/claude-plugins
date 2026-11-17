---
name: omniroute-setup
description: Use when the user wants to set up, run or troubleshoot OmniRoute, route Claude Code through it, or use its MCP tools.
---

# OmniRoute setup

OmniRoute (https://github.com/cheaper-inference/OmniRoute) is a separate Node gateway.
This plugin only registers its MCP server (`npx -y omniroute --mcp`, stdio). It does not run the gateway.

## Steps

1. Install and first run: `npm i -g omniroute`, then `omniroute setup`. The gateway serves on
   http://localhost:20128. Diagnose problems with `omniroute doctor`.
2. Add your own provider accounts and keys in its dashboard. Never paste keys into chat.
3. To send Claude Code traffic through the gateway: `omniroute run claude --model <provider/model>`.
4. For the full tool set over HTTP instead of stdio, run `omniroute mcp enable --transport streamable-http`,
   then `claude mcp add --transport http omniroute http://localhost:20128/api/mcp/stream --header "Authorization: Bearer <key>"`.

Free-tier limits and terms are set by each provider, not by OmniRoute.
