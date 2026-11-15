# Figma MCP Bridge

| | |
|---|---|
| Source | [gethopp/figma-mcp-bridge](https://github.com/gethopp/figma-mcp-bridge) · [releases](https://github.com/gethopp/figma-mcp-bridge/releases) |
| npm | `@gethopp/figma-mcp-bridge` |
| Licence | MIT, by Hopp |
| Owner | (add) |
| Last checked | 2026-11-15 (v0.0.27) |

## What it does
A Figma plugin plus an MCP server that streams the open Figma file to Claude (or any MCP client) live, through the
plugin instead of Figma's REST API. That means no API rate limits, which matters on free Figma plans.

Claude can then **read** the file (document tree, selection, styles, variables/tokens, prototype flows, screenshots)
and, with a set of opt-in **write** tools, edit it: text, fills, auto layout, frames, shapes, images, SVG, and more.
It also has **motion tools (beta)**: read and apply Figma animation presets and keyframe tracks, and set timeline
duration. It works in Figma design files, Dev Mode (read-only) and FigJam, and with several files open at once.

## Set up
Needs the **Figma desktop app** (Mac or Windows) and Node.js. The browser version of Figma can't load development plugins.

1. **Add the MCP server to Claude Code** (once per computer):
   ```bash
   claude mcp add figma-bridge -- npx -y @gethopp/figma-mcp-bridge
   ```
   Other tools (Cursor, Claude Desktop): add `"command": "npx", "args": ["-y", "@gethopp/figma-mcp-bridge"]` to their MCP config.
2. **Add the plugin to Figma**: download the latest release, then Plugins > Development > Import plugin from manifest >
   `plugin/manifest.json`.
3. Open a Figma file, run the plugin, and prompt Claude. The server connects to the plugin by itself.

## How we use it
- **Design to code:** select a frame, ask Claude to build it in our Next.js stack using the file's variables as tokens.
- **Read motion intent:** prototype flows and motion presets tell Claude what moves and when, before writing GSAP or Rive.
- **Quick edits and cleanup:** rename layers, fix auto layout, swap text, before handing off to
  [Fig-to-SeaMotion](../repos/fig-to-seamotion.md) or [Fig-to-Rive](../repos/fig-to-rive.md).

## Rules
- Edit tools change the real file. Work on a copy or a branch of the file when trying something big.
- Keep `run_script` **off** (it is off by default). It runs any JavaScript in the open file; only turn it on for a
  specific job, then turn it off again.
- `delete_nodes` asks for confirmation; read what Claude is about to delete before saying yes.
- Client files: check the client is fine with AI tools reading their designs.
- Figma also has its own official MCP server. Use the bridge when you hit API limits or want the edit and motion tools.
