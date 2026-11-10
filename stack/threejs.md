# Three.js

| | |
|---|---|
| Source | [mrdoob/three.js](https://github.com/mrdoob/three.js) · [docs](https://threejs.org/docs/) |
| In React | [React Three Fiber](https://github.com/pmndrs/react-three-fiber) + [drei](https://github.com/pmndrs/drei) |
| Last checked | 2026-11-10 |

## In Next.js
Use React Three Fiber and drei instead of raw Three.js setup code. Load the scene so it never runs on the server:

```tsx
import dynamic from 'next/dynamic'
const HeroScene = dynamic(() => import('./hero-scene'), { ssr: false })
```

## Models
- Export `.glb` (glTF binary).
- Compress with [glTF-Transform](https://github.com/donmccurdy/glTF-Transform) before committing.
- Turn a model into a component with [gltfjsx](https://github.com/pmndrs/gltfjsx).

## Rules
- Transparent canvas over the page; keep one canvas per page where you can.
- Stop rendering when the canvas is off-screen (`frameloop="demand"` or pause on IntersectionObserver).
- Dispose geometry, materials, textures and the renderer on unmount (R3F does most of this; check custom code).
- Camera, lights and material values go in `config.ts` and [DialKit](../repos/dialkit.md) while tuning.

More: [tips/threejs-and-3d-assets.md](../tips/threejs-and-3d-assets.md).
