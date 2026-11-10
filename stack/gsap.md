# GSAP

| | |
|---|---|
| Source | [greensock/GSAP](https://github.com/greensock/GSAP) · [docs](https://gsap.com/docs/v3/) |
| Licence | Free, including commercial use and all bonus plugins (SplitText, MorphSVG …) |
| Last checked | 2026-11-10 |

## Install
```bash
npm install gsap @gsap/react
```

## Set up once (client component)
```ts
'use client'
import gsap from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'
import { SplitText } from 'gsap/SplitText'
import { useGSAP } from '@gsap/react'

gsap.registerPlugin(ScrollTrigger, SplitText, useGSAP)
```

## In a component
```tsx
const scope = useRef(null)
useGSAP(() => {
  gsap.from('.card', {
    y: 40, opacity: 0, stagger: 0.08,
    scrollTrigger: { trigger: scope.current, start: 'top 80%' },
  })
}, { scope })   // everything inside is reverted on unmount
```

## Rules
- Use `useGSAP()` (or `gsap.context()`) so animations clean up on unmount and route change.
- Use `gsap.matchMedia()` for mobile vs desktop and for `prefers-reduced-motion`.
- Animate `transform` and `opacity` (`x`, `y`, `scale`, `rotate`, `autoAlpha`), not `top`, `width` or `margin`.

See also: [splittext.md](splittext.md), [lenis.md](lenis.md), [learn/motion-presets.md](../learn/motion-presets.md).
