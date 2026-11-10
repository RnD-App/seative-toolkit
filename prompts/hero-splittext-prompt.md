# Hero with SplitText reveal

````markdown
Add a hero section to this Next.js site:
- Heading: "[heading text]", subheading: "[subheading]", button: "[label]" linking to [#section]
- On load: SplitText line reveal on the heading (mask lines, yPercent 100 to 0), then the subheading and button fade up
- Run the split after document.fonts.ready; revert on unmount (useGSAP)
- Take duration, stagger and ease from motion.ts, and expose them as DialKit controls in a "Hero" panel (dev only)
- prefers-reduced-motion: show everything with no movement
- Style: [colours, font, layout notes]
````
