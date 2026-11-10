# Lenis (smooth scroll)

| | |
|---|---|
| Source | [darkroomengineering/lenis](https://github.com/darkroomengineering/lenis) · [React adapter](https://github.com/darkroomengineering/lenis/blob/main/packages/react/README.md) |
| Last checked | 2026-11-10 |

## Install
```bash
npm install lenis
```

## Next.js: one provider, driven by GSAP's clock
Put this in `app/smooth-scroll.tsx` and wrap the app with it in `app/layout.tsx`.

```tsx
'use client'
import gsap from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'
import { ReactLenis, useLenis, type LenisRef } from 'lenis/react'
import { useEffect, useRef } from 'react'
import 'lenis/dist/lenis.css'

gsap.registerPlugin(ScrollTrigger)

export function SmoothScroll({ children }: { children: React.ReactNode }) {
  const lenisRef = useRef<LenisRef>(null)
  useLenis(ScrollTrigger.update)            // keep ScrollTrigger in sync on every scroll

  useEffect(() => {
    function update(time: number) {
      lenisRef.current?.lenis?.raf(time * 1000)
    }
    gsap.ticker.add(update)
    gsap.ticker.lagSmoothing(0)
    return () => gsap.ticker.remove(update)
  }, [])

  return (
    <>
      <ReactLenis root options={{ autoRaf: false }} ref={lenisRef} />
      {children}
    </>
  )
}
```

## Rules
- One Lenis for the whole site. Never run a second smooth-scroll library next to it.
- Use the Lenis CSS, or nested scroll areas and `position: sticky` can misbehave.
- Turn it off (or set a short duration) for `prefers-reduced-motion`.
