# Claude motion skill

| | |
|---|---|
| Status | to build (team skill) |
| Examples | [anthropics/skills](https://github.com/anthropics/skills) · [rive-app/skills](https://github.com/rive-app/skills) |
| Owner | (add) |
| Last checked | 2026-11-10 |

## What it is for
A prompt is for one website. A **skill** is our house style, written once, that Claude follows every time: the same
presets, timings, cleanup rules and DialKit setup on every project.

## Prompt or skill?
| Use a prompt ([prompts/](../prompts/)) | Use the skill |
|---|---|
| A one-off site or section | Every project, so motion looks and behaves the same |
| You want to try something new | You want our rules applied without repeating them |

## What our skill should contain
- Our stack: Next.js, GSAP + SplitText, Lenis on GSAP's ticker, Three.js / Rive, DialKit in development only.
- Our preset names and values from `motion.ts`: `fade-up`, `reveal-lines`, `scale-in`, `stagger-cards`.
- Our rules from [tips/](../tips/): transform and opacity only, `useGSAP` cleanup, fonts before SplitText,
  reduced motion, off-screen pause for 3D.

## How to share it
Put it in a repo the way [go-commands](../repos/go-commands.md) does (`skills/<name>/SKILL.md` plus an install script),
so every teammate installs the same version.
