# Motion performance

- Animate only `transform` and `opacity` (`x`, `y`, `scale`, `rotate`, `autoAlpha`). Animating `width`, `height`,
  `top`, `left` or `margin` makes the browser redo layout every frame and causes jank.
- Use `will-change: transform` only on what is animating right now, and remove it after.
- Avoid animating large `filter: blur()` or `box-shadow`; fake them with a pre-blurred image or opacity.
- One scroll loop: Lenis on GSAP's ticker. No extra `requestAnimationFrame` loops for scroll.
- Pause what you can't see: 3D off-screen, videos off-screen, Rive files off-screen.
- Test on a mid-range Android phone with the network throttled, not only on a MacBook.
- Every animation needs a `prefers-reduced-motion` version.
