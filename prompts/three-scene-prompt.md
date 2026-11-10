# Three.js scene section

````markdown
Add a 3D [hero / product / background] scene to this Next.js site:
- Model: [path to .glb, or "a simple placeholder shape"]; compress it with glTF-Transform if it is over 2 MB
- Use React Three Fiber + drei, loaded with next/dynamic and ssr: false; transparent canvas over the page
- Interaction: [e.g. slow auto-rotate, follows the mouse, rotates with scroll via ScrollTrigger]
- Pause rendering when the canvas is off-screen; dispose resources on unmount
- Expose camera position and fov, light intensity and colour, and rotation speed as DialKit controls in a "Scene" panel (dev only)
- prefers-reduced-motion: no auto-rotate, show a still frame
- Fallback for no WebGL: a poster image [path]
````
