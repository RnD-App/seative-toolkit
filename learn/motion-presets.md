# Motion presets: learn and reuse

Last checked: 2026-11-10

## 1. Easing: understand it and build it
- [easings.net](https://easings.net): cheat sheet of standard easing curves with previews
- [cubic-bezier.com](https://cubic-bezier.com): draw a curve and compare it with others
- [Easing Wizard](https://easingwizard.com): build springs, bounces and curves, copy the CSS
- [GSAP ease visualizer](https://gsap.com/docs/v3/Eases): every GSAP ease, live

## 2. Ready-made presets to study or reuse
- [Animista](https://animista.net): CSS entrance, exit and attention presets you can customise
- [Animate.css](https://github.com/animate-css/animate.css): a classic preset library; read it for timings
- [Motion examples](https://motion.dev/examples): animation snippets for React, JavaScript and Vue
- [LottieFiles free animations](https://lottiefiles.com/free-animations) · [Rive community](https://rive.app/community):
  files you can open and take apart

## 3. Learn GSAP properly
- [GSAP resources](https://gsap.com/resources/): the official learning hub
- [GreenSock on CodePen](https://codepen.io/GreenSock): official demos, including ScrollTrigger and SplitText

## 4. Motion principles from big design systems
- [Material 3 motion](https://m3.material.io/styles/motion/overview): duration and easing tokens
- [Apple HIG motion](https://developer.apple.com/design/human-interface-guidelines/motion): when motion helps and
  when it gets in the way

## 5. Go deeper
- [Josh Comeau on animation](https://www.joshwcomeau.com/animation/): free in-depth articles
- [animations.dev](https://animations.dev): paid course on web animation craft
- [Codrops](https://tympanus.net/codrops/): creative demos with tutorials
- [Theatre.js docs](https://www.theatrejs.com/docs/latest): timeline-based motion on the web

## 6. AI prompt and component libraries
- [Motion examples](https://motion.dev/examples): free, copy-paste
- [Scrolltide components](https://www.scrolltide.co/components): animated component prompts (paid plans, link only)
- [GetLayers AI tools](https://www.getlayers.ai/tools): free design tools that end in a prompt; works over MCP

## Team tips
- **One preset vocabulary everywhere.** Same names in seaMotion and on websites: `fade-up`, `reveal-lines`,
  `scale-in`, `stagger-cards`.
- **Motion tokens in every site.** One `motion.ts`:
  ```ts
  export const duration = { fast: 0.2, base: 0.4, slow: 0.8 }
  export const ease = { out: 'power3.out', inOut: 'power2.inOut', back: 'back.out(1.6)' }
  ```
  GSAP, DialKit and the prompts all read from it.
- **Save seaMotion presets in the repo** (`Presets/` in seaMotion) so everyone gets them.
- **Practise by rebuilding.** Pick a preset from Animista or easings.net, rebuild it in GSAP, then in seaMotion.
- **Less is more.** Shorter durations and smaller distances usually look more polished. Every preset needs a
  `prefers-reduced-motion` version.
