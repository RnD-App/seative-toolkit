# Fig-to-SeaMotion

| | |
|---|---|
| Source | [RnD-Products/Fig-to-SeaMotion](https://github.com/RnD-Products/Fig-to-SeaMotion) |
| Download | [latest release](https://github.com/RnD-Products/Fig-to-SeaMotion/releases/latest) (`Fig-to-SeaMotion.zip`) |
| Licence | MIT, built on Toolcraft |
| Owner | (add) |
| Last checked | 2026-11-10 |

## What it does
A Figma plugin that copies the selected layers as JSON, which you paste into [seaMotion](seamotion.md) with **Import**.
It carries layout, fills, strokes, effects, text and small icons as SVG, and can attach PNG pictures of each layer.
It has no network access; nothing leaves Figma except what you paste.

## Install (any computer, any Figma account)
1. Download and unzip the latest release.
2. Figma **desktop app**: Plugins > Development > Import plugin from manifest > `manifest.json`.
3. Run it from Plugins > Development > Fig to SeaMotion.

Development plugins only load in the Figma desktop app, not in the browser.

## Tips
- Leave the three cleaners on (clean names, round values, remove hidden layers). Your Figma file is not changed.
- Making a Lottie? Use the **Lottie** tab's **Analyze selection** first: it lists what Lottie can't carry and how to fix it.
- Big pictures: turn on **Make pictures smaller** and pick a max width before copying.
- The plugin also lives inside the seaMotion repo (`seaMotion/Fig-to-SeaMotion/`). Treat this repo as the source.
