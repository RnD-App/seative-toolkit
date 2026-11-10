# Toolcraft

| | |
|---|---|
| Website | [toolcraft.sh](https://toolcraft.sh) · [examples](https://toolcraft.sh/gallery) |
| Source | [pixel-point/toolcraft](https://github.com/pixel-point/toolcraft) |
| Licence | MIT, by Pixel Point |
| Owner | (add) |
| Last checked | 2026-11-10 |

## What it does
An open-source starter kit and UI library for building your own design apps with AI. The starter app uses TanStack
Router, React, TypeScript, Tailwind CSS and Base UI, with a pan-and-zoom canvas like a design tool. It works with any AI
coding agent.

## Where we use it
- [seaMotion](seamotion.md) started from the Toolcraft app starter and keeps its runtime.
- [Fig-to-SeaMotion](fig-to-seamotion.md) is built on it too.

## Start a new tool
In the terminal:
```bash
npx @pixel-point/toolcraft create
```
Or open an empty folder in Claude Code and ask it to run
`npx --yes @pixel-point/toolcraft create --yes`, build your idea and start a local preview.

## Tips
- Keep Toolcraft's `LICENSE.md` and `NOTICE.md` in every app built on it.
- Look at the [gallery](https://toolcraft.sh/gallery) before starting: someone may have built half of it already.
