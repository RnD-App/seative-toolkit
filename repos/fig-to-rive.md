# Fig-to-Rive

| | |
|---|---|
| Source | [RnD-Products/Fig-to-Rive](https://github.com/RnD-Products/Fig-to-Rive) |
| Licence | none set yet |
| Owner | (add) |
| Last checked | 2026-11-10 |

## What it does
A Figma plugin plus a small local helper that turns Figma frames into Rive files. Auto layout and live text are kept
(nothing is outlined). Optional Webflow-safe layout and one-command animation.

## Needs on the computer
Node.js 18 or newer · [Rive CLI](../stack/rive.md) and `rive login` · Python 3 (only for animation) · Figma desktop.
Works on Mac, Windows and Linux.

## Set up (once per computer)
```bash
git clone https://github.com/RnD-Products/Fig-to-Rive.git
cd Fig-to-Rive && ./scripts/setup.sh
```
`setup.sh` checks Node.js, the Rive CLI, your Rive login, fonts and kit projects, and tells you what to fix.

Then:
1. Start the helper: `Start Helper.command` (Mac), `Start Helper.bat` (Windows) or `npm start`. Leave it open and copy
   the token it prints.
2. Figma desktop: Plugins > Development > Import plugin from manifest > `plugin/manifest.json`.
   Click the gear in the plugin, paste the token, press Enter.

Full guide: `docs/SETUP-NEW-COMPUTER.md` in the repo.

## Use
Select a frame > **Send to Rive** > **Push to my Rive account**. Nothing is pushed until you click.
Exports go to `../Exports/` (next to the repo folder, not inside it).

## Tips
- Put real `.ttf` files in `Fonts Library/`, named the way the plugin asks. Missing fonts fall back and are flagged.
- The helper listens on this computer only and needs the token.
- Next step after export: add motion with an agent, see [guides/rive-agent-workflow.md](../guides/rive-agent-workflow.md).
