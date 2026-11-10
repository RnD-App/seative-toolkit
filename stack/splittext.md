# GSAP SplitText

| | |
|---|---|
| Docs | [gsap.com/docs/v3/Plugins/SplitText](https://gsap.com/docs/v3/Plugins/SplitText) |
| Licence | Free with GSAP |
| Last checked | 2026-11-10 |

## What it does
Splits text into lines, words or characters so each piece can animate on its own: line reveals, word staggers,
character effects.

## Line reveal (inside `useGSAP`)
```ts
document.fonts.ready.then(() => {
  const split = SplitText.create('.hero-title', { type: 'lines', mask: 'lines' })
  gsap.from(split.lines, { yPercent: 100, duration: 0.8, stagger: 0.08, ease: 'power3.out' })
})
```

## Rules
- **Split after fonts load** (`document.fonts.ready`). Splitting before the web font arrives breaks lines in the wrong
  places.
- Re-split on resize for line splits, and revert on unmount (`useGSAP` does this for you).
- Keep text readable for screen readers and with `prefers-reduced-motion`: show it without the animation.
- Check the current options (`mask`, `autoSplit`, `aria`) in the docs above before relying on them.
