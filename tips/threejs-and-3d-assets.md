# Three.js and 3D assets

- **Compress every model** with [glTF-Transform](https://github.com/donmccurdy/glTF-Transform): Draco or Meshopt for
  geometry, KTX2 for textures. Aim for under 2–3 MB per scene.
- **Textures** are usually the biggest part. 2048 px is plenty for most web scenes; 1024 px for small objects.
- **Load late.** `next/dynamic` with `ssr: false`, and show a poster image until the scene is ready.
- **Pause off-screen** and **dispose on unmount** (geometry, materials, textures, renderer).
- **One canvas per page** where you can; several WebGL contexts are heavy.
- **Tune live** with DialKit (camera, lights, materials), then save the values in `config.ts`.
- **Don't reuse other people's models** without a licence, including ones found with
  [3D Mview Extractor](../extensions/3d-mview-extractor.md).
