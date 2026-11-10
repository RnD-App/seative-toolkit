# Next.js (every website)

| | |
|---|---|
| Source | [vercel/next.js](https://github.com/vercel/next.js) · [docs](https://nextjs.org/docs) |
| Needs | Node.js 20.9 or newer (Next.js 16) |
| Last checked | 2026-11-10 |

## Our default setup
- App Router, TypeScript, Tailwind CSS.
- [GSAP](gsap.md) + [SplitText](splittext.md) for page motion, [Lenis](lenis.md) for smooth scroll.
- [Three.js](threejs.md) or [Rive](rive.md) for 3D and interactive pieces.
- [DialKit](../repos/dialkit.md) for live tuning in development only.
- Deploy on [Vercel](../guides/deploy-vercel.md) (default) or [Netlify](../guides/deploy-netlify.md).

## Start
```bash
npx create-next-app@latest my-site
```
Choose TypeScript, Tailwind and App Router. Or use [prompts/website-create-prompt.md](../prompts/website-create-prompt.md)
and let Claude set it all up.

## Rules
- Anything that touches `window` (GSAP, Lenis, Three.js, Rive, DialKit) goes in a client component (`'use client'`).
- Heavy pieces (3D scenes) load with `next/dynamic` and `ssr: false`, so they don't slow the first paint.
- One `motion.ts` with durations and eases; every animation reads from it.
- Add a `.nvmrc` so the whole team uses the same Node.js version.
