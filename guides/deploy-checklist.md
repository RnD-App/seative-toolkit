# Before every launch

Copy this into the launch PR and tick it.

## Build
- [ ] `npm run build` passes locally with no type errors
- [ ] Environment variables are set on the host (Vercel or Netlify)
- [ ] Node.js version on the host matches `.nvmrc`

## Motion
- [ ] DialKit is not in the production bundle
- [ ] `prefers-reduced-motion` turns off scroll scrubs, SplitText reveals and big movement; content is still visible
- [ ] No layout jump when fonts load (SplitText runs after `document.fonts.ready`)
- [ ] Lenis and ScrollTrigger stay in sync (scroll to the bottom and back)

## Assets
- [ ] 3D models compressed (glTF-Transform), under 2–3 MB per scene
- [ ] Videos compressed with ffmpeg, MP4 has `+faststart`, poster image set
- [ ] Images sized for their slot, modern formats where possible

## Checks
- [ ] Mobile: a mid-range phone, not only a MacBook
- [ ] Lighthouse: performance and accessibility looked at, big problems fixed
- [ ] The PR preview URL was reviewed by someone else
- [ ] README says how to run, build and deploy
