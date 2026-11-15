# MCP servers

MCP servers let Claude Code (and other AI tools) work directly inside other apps. Agree as a team before adding one,
and give each one a page here with its setup and rules.

| Server | What it connects | Page |
|---|---|---|
| Figma MCP Bridge | Live Figma and FigJam files: read, edit, motion presets | [figma-mcp-bridge.md](figma-mcp-bridge.md) |
| rive-mcp (third-party, freeware) | Rive `.riv` files without the editor | [stack/rive.md](../stack/rive.md#rive-mcp) |
| GetLayers | Design tools that end in a prompt (SVG to 3D, gradients, shaders) | [learn/motion-presets.md](../learn/motion-presets.md#6-ai-prompt-and-component-libraries) |

## Add one to Claude Code
```bash
claude mcp add <name> -- <command> [args...]
claude mcp list
```

## Rules
- Prefer servers with an open licence and recent releases; write both on the page.
- Read what the server can change. Keep risky tools (running scripts, deleting) off unless needed.
- Never put API keys in this repo; set them in your own MCP config.
