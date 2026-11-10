# Rive (interactive motion)

| | |
|---|---|
| Website | [rive.app](https://rive.app) · [runtimes](https://rive.app/docs/runtimes/getting-started) · [CLI](https://rive.app/docs/cli/getting-started) |
| Web runtime | [rive-react](https://github.com/rive-app/rive-react) · [rive-wasm](https://github.com/rive-app/rive-wasm) |
| Agent skill | [rive-app/skills](https://github.com/rive-app/skills) (official, MIT) |
| Examples | [awesome-rive](https://github.com/rive-app/awesome-rive) |
| Last checked | 2026-11-10 |

## When to use Rive vs GSAP
| Use Rive for | Use GSAP for |
|---|---|
| Pieces with their own states: buttons, toggles, loaders, onboarding, characters, hero graphics | Page motion: scroll, text reveals, layout and section transitions |

One Rive file holds the visuals, motion, interaction (state machines) and layout. The site only loads it, sets its
inputs and listens for its events.

## Rive CLI (built for coding agents)
Makes and checks `.riv` files from text.

```bash
brew install --cask rive-app/cli/rive-cli    # macOS (Apple Silicon) or Linux x64
rive login
```
- `rive create` sets up a project and writes an `AGENTS.md` for the agent to follow.
- `rive docs` opens the docs.
- The Homebrew install is pinned; update with `brew upgrade`. (`rive update` only works with Rive's curl installer.)

## Rive agent skill for Claude Code
In a `claude` terminal:
```
/plugin marketplace add rive-app/skills
/plugin install rive@rive
```
It tells Claude when Rive fits and sends it to the CLI, the runtime docs or the project's `AGENTS.md`.

## Rive MCP
- [rive-mcp](https://github.com/ODU33104/rive-mcp) (third-party): builds, edits, inspects and previews `.riv` files from
  Claude without the Rive editor. It is **freeware, not open source**: link to it, never fork or copy it.
- Rive may also offer its own MCP that works with the editor running; check Rive's docs before setting one up.

Step-by-step: [guides/rive-agent-workflow.md](../guides/rive-agent-workflow.md). From Figma: [Fig-to-Rive](../repos/fig-to-rive.md).
