# How seaMotion was built with Toolcraft

> **Outline.** The sections below say what is known from the seaMotion repo today. Each one still needs a full write-up
> by someone who built that part (marked *To write*). Owner: (add)

## 01. Start from the Toolcraft starter
seaMotion began as the [Toolcraft](../repos/toolcraft.md) app starter (`npx @pixel-point/toolcraft create`) and keeps its
runtime under the MIT licence. Toolcraft gives the React + TypeScript app, Tailwind, Base UI and a pan-and-zoom canvas.
*To write: what was kept, what was replaced, and the first prompts used.*

## 02. Layers and timeline
The editor builds a design from layers and animates them on a timeline, with presets read from `Presets/`.
*To write: the project format (`mo-app-project` JSON), layer types, keyframes and how presets apply.*

## 03. Getting designs in from Figma
[Fig-to-SeaMotion](../repos/fig-to-seamotion.md) copies Figma layers as JSON; seaMotion's **Import** reads it.
*To write: how the JSON maps onto seaMotion layers, and how to add a new property end to end.*

## 04. Export
Video export runs in the browser with the `mediabunny` library. Post-processing uses [ffmpeg](../stack/ffmpeg.md).
*To write: export formats (video, Lottie), settings, and known limits.*

## 05. Saving and deploying
`npm run dev` starts a helper that auto-saves to `~/Documents/seaMotion/Recovered`. The site deploys on Vercel from the
`seaMotion/` folder; the build copies projects from `Recovered/` so the hosted Open project page can list them.
*To write: the release steps and how to add example projects.*

Source: [RnD-Products/seaMotion](https://github.com/RnD-Products/seaMotion).
