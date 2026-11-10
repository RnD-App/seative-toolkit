# Website create prompt

Fill in the `[brackets]`, then paste into Claude Code in an empty folder.

````markdown
Build a [type of site, e.g. portfolio / agency landing page / product launch] for [brand] using this stack:

- Next.js (App Router, TypeScript, Tailwind CSS)
- GSAP with ScrollTrigger and SplitText, set up with @gsap/react (useGSAP)
- Lenis for smooth scroll, using lenis/react, driven by GSAP's ticker:
  ReactLenis root with autoRaf: false; gsap.ticker.add(t => lenis.raf(t * 1000));
  gsap.ticker.lagSmoothing(0); useLenis(ScrollTrigger.update)
- Three.js with React Three Fiber + drei for one 3D [hero / section], loaded with next/dynamic and ssr: false
- DialKit (npm install dialkit motion) for realtime editing, development only

Sections: [Hero, About, Work, Services, Contact]
Style: [colours, fonts, mood, 2–3 reference sites]
Copy: [paste real copy, or say "write placeholder copy that fits the brand"]

Realtime editing with DialKit:
- Keep every tunable value in one typed config.ts: GSAP durations, eases, staggers, ScrollTrigger start/end,
  SplitText type and stagger, Lenis duration, Three.js camera, lights and materials
- Show them as DialKit controls (useDialKit), one panel per section, with sensible [default, min, max]
- Changing a control updates the animation live (rebuild the timeline or set the value); no reload
- Load DialKit only when NODE_ENV is not production, so it never ships

Motion rules:
- Headings: SplitText line reveal, run after document.fonts.ready, revert on unmount
- Sections: ScrollTrigger entrances; scrub only where it adds meaning
- Animate transform and opacity only
- Three.js: compressed .glb, pause rendering off-screen, dispose on unmount
- Wrap all animation in useGSAP so it cleans up
- prefers-reduced-motion: no scrubs or reveals, content fully visible

Deployment:
- Initialise git; commit in small steps
- Add .env.example (no real values), .nvmrc with the Node.js LTS version, and a README with run, build and deploy steps
- Make sure npm run build passes with no type errors and DialKit is not in the production bundle
- Ready to deploy on Vercel (default) or Netlify

Work in this order: show the file tree first, then build section by section, and start the dev server when done.
````
