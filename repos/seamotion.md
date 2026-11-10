# seaMotion

| | |
|---|---|
| Live | [editor-seamotion.vercel.app](https://editor-seamotion.vercel.app) (example projects, read-only) |
| Source | [RnD-Products/seaMotion](https://github.com/RnD-Products/seaMotion) |
| Licence | MIT, built on [Toolcraft](toolcraft.md) by Pixel Point (see `seaMotion/LICENSE.md` and `NOTICE.md`) |
| Owner | (add) |
| Last checked | 2026-11-10 |

## What it does
A browser-based motion design editor: build a design from layers, animate it on a timeline, preview it and export it.
Video export runs in the browser (the `mediabunny` library); use [ffmpeg](../stack/ffmpeg.md) afterwards to convert or
compress.

## Run it locally
Needs Node.js (see [onboarding](../guides/onboarding.md)) and a desktop browser at least 1024 px wide.

```bash
git clone https://github.com/RnD-Products/seaMotion.git
cd seaMotion/seaMotion
npm install
npm run dev
```

Open http://localhost:3002. `npm run dev` also starts a helper that auto-saves projects to
`~/Documents/seaMotion/Recovered` and reads fonts and presets from `~/Documents/seaMotion/Fonts` and `Presets`.

Other commands (in `seaMotion/`): `npm run build`, `npm run typecheck`, `npm test`.

## Get designs in
- From Figma: [Fig-to-SeaMotion](fig-to-seamotion.md)
- Project files are single `.json` files (format `mo-app-project`); open them from the Open project page.

## Deploy
Vercel, with Root Directory set to `seaMotion`. On the hosted site edits are not saved; saving needs `npm run dev`.

## Tips
- Commit tuned presets to the repo's `Presets/` folder so the whole team gets them, and name them the same way as
  on websites (see [learn/motion-presets.md](../learn/motion-presets.md)).
- How it was built: [guides/build-seamotion-with-toolcraft.md](../guides/build-seamotion-with-toolcraft.md).
