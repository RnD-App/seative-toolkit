# GSAP, Lenis and SplitText together

- **Register plugins once** (ScrollTrigger, SplitText, useGSAP) in one client file, not in every component.
- **Lenis runs on GSAP's ticker** with `autoRaf: false`, and `useLenis(ScrollTrigger.update)` keeps them in sync.
  Setup: [stack/lenis.md](../stack/lenis.md).
- **Fonts before SplitText.** Split inside `document.fonts.ready`, or lines break in the wrong places.
- **Clean up.** Put animations in `useGSAP()`; it reverts SplitText and kills ScrollTriggers on unmount and route change.
- **Refresh after layout changes.** If images or fonts change the page height after load, call `ScrollTrigger.refresh()`.
- **Mobile.** Use `gsap.matchMedia()` for simpler mobile motion; heavy pins and scrubs often feel bad on touch.
- **Reduced motion.** Inside `matchMedia`, skip reveals and scrubs for `(prefers-reduced-motion: reduce)`.
