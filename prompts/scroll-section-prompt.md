# Scroll section (Lenis + ScrollTrigger)

````markdown
Add a [pinned / scrubbed / horizontal-scroll] section to this Next.js site:
- Content: [what the section shows, e.g. 4 feature cards / a timeline / product steps]
- Motion: [describe it, e.g. pin for 200% of the viewport while cards stack; progress bar fills]
- Use the existing Lenis provider (Lenis on GSAP's ticker, useLenis(ScrollTrigger.update)); don't add a second scroller
- Use useGSAP for cleanup and gsap.matchMedia() for a simpler mobile version
- Expose start, end and scrub as DialKit controls in a "[Section name]" panel (dev only)
- prefers-reduced-motion: no pin or scrub, show the content as a normal stacked section
````
