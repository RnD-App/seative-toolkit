# Onboarding: set up a new computer

Do these in order.

## 1. Install the tools
| Tool | Why | Install |
|---|---|---|
| **Node.js (LTS)** | seaMotion, Fig-to-Rive's helper, every Next.js site | [nodejs.org/download](https://nodejs.org/en/download), or [nvm](https://github.com/nvm-sh/nvm) to switch versions |
| Git + GitHub CLI | code, pull requests, go-commands | Mac: `brew install git gh` |
| Claude Code | our AI coding agent | [claude.com/claude-code](https://claude.com/claude-code) |
| Rive CLI | Fig-to-Rive and the Rive agent workflow | `brew install --cask rive-app/cli/rive-cli` |
| ffmpeg | video conversion | Mac: `brew install ffmpeg` (others: [stack/ffmpeg.md](../stack/ffmpeg.md)) |
| Python 3 | only for Fig-to-Rive animation tools | [python.org](https://www.python.org/downloads/) or `brew install python` |
| Figma desktop | our plugins only load in the desktop app | [figma.com/downloads](https://www.figma.com/downloads/) |

**Node.js:** use the **LTS** version, not "Current". Next.js 16 needs 20.9 or newer; Fig-to-Rive needs 18 or newer.
Check with `node -v` and `npm -v`.

## 2. Sign in
```bash
gh auth login
rive login
```
Ask an admin to add you to the **RnD-Products** and **RnD-App** GitHub orgs.

## 3. Install go-commands
```bash
git clone https://github.com/RnD-Products/go-commands.git ~/go-commands
~/go-commands/install.sh --owner RnD-Products
```
Restart Claude Code. Now `go pr`, `go update` and `goapp update` work in every project. See
[repos/go-commands.md](../repos/go-commands.md).

## 4. Chrome extensions
Install [Wappalyzer](../extensions/wappalyzer.md). Install [3D Mview Extractor](../extensions/3d-mview-extractor.md)
only if you need it, in a separate Chrome profile.

## 5. Try our tools
- Run [seaMotion](../repos/seamotion.md) locally.
- Import [Fig-to-SeaMotion](../repos/fig-to-seamotion.md) and [Fig-to-Rive](../repos/fig-to-rive.md) into Figma desktop.

## 6. Read
[stack/](../stack/) for how we build, [tips/](../tips/) for team rules, [learn/motion-presets.md](../learn/motion-presets.md)
to learn motion.
