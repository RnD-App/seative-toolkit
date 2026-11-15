# Jitter MCP

| | |
|---|---|
| Website | [jitter.video](https://jitter.video) |
| Setup guide | [Connect Jitter to your AI assistant with the MCP server](https://help.jitter.video/en/articles/17600405-connect-jitter-to-your-ai-assistant-with-the-mcp-server) |
| Server URL | `https://mcp.jitter.video` |
| Made by | Jitter (official) · **beta** |
| Owner | (add) |
| Last checked | 2026-11-15 |

## What it does
Connects your Jitter account to Claude (or ChatGPT, Notion and other MCP apps). Claude works directly in your Jitter
projects, and everything stays editable in Jitter. It can:
- create new Jitter projects and find files you can access
- inspect designs, layers, text and animations
- edit layouts, content and motion
- import images or videos, take screenshots to review, and export

Not yet available through MCP: Jitter's credit-based AI features, and moving files between drafts or workspaces.

## Set up
It's a remote server: no install, you sign in to Jitter when you connect.

**Claude Code** (once per computer):
```bash
claude mcp add --transport http jitter https://mcp.jitter.video
```
Then run `/mcp` in a `claude` terminal, pick **jitter** and sign in to Jitter.

**Claude Desktop / claude.ai:** Settings > Connectors > Add custom connector, paste `https://mcp.jitter.video`, then
sign in to Jitter and select **Allow access**.

## How we use it
- **Brief to first draft:** "Turn this launch brief into 3 animated social posts in Jitter."
- **Every format at once:** adapt one animation to square, vertical and widescreen.
- **Bulk updates:** swap headlines, CTAs or approved images across several files.
- **Brand kits:** bring a site's colours, styles and easings into the Jitter workspace. Use the names from
  [learn/motion-presets.md](../learn/motion-presets.md) so Jitter, seaMotion and websites match.
- **Handover:** "Walk me through the layers and animations in this file" when picking up a teammate's work.
- **Review:** ask for a screenshot of each scene before opening Jitter.

## Where it fits
| Tool | Best for |
|---|---|
| Jitter (+ MCP) | Quick animated social posts, ads, product shots and multi-format variants |
| [seaMotion](../repos/seamotion.md) | Our own editor; Lottie and video export, Figma import |
| [Rive](../stack/rive.md) | Interactive pieces with states, for apps and websites |
| [GSAP](../stack/gsap.md) | Motion on the website itself |

## Rules
- It edits real files in your Jitter workspace. Try big changes on a duplicate first.
- It's in beta: check the result in Jitter before sending anything to a client.
- Each teammate signs in with their own Jitter account; never share a login.
- Client files: check the client is fine with AI tools working on their designs.
