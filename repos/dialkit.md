# DialKit

| | |
|---|---|
| Source | [joshpuckett/dialkit](https://github.com/joshpuckett/dialkit) · [reference](https://github.com/joshpuckett/dialkit/blob/main/docs/reference.md) |
| Apple | [dialkit-ios](https://github.com/mikelikesdesign/dialkit-ios) · [dialkit-macos](https://github.com/mikelikesdesign/dialkit-macos) (SwiftUI) |
| Owner | (add) |
| Last checked | 2026-11-10 |

## What it does
Live controls for tuning an interface while it runs: adjust values, compare versions and edit animation timing in your
running app. Works with React, Solid, Svelte, Vue and plain JavaScript.

## Set up in Next.js
```bash
npm install dialkit motion
```
Use it in a client component (`'use client'`):

```tsx
'use client'
import { DialRoot, useDialKit } from "dialkit";
import "dialkit/styles.css";

export function Hero() {
  const values = useDialKit("Hero", {
    duration: [0.8, 0.1, 2],   // [default, min, max]
    stagger: [0.06, 0, 0.3],
  });
  // use values.duration and values.stagger in the GSAP timeline
  return (
    <>
      {/* hero markup */}
      <DialRoot />  {/* render once in the app, not in every section */}
    </>
  );
}
```

## Our workflow
1. Keep every tunable value in one typed `config.ts` (durations, eases, distances, camera, lights).
2. DialKit reads those defaults and shows them as controls, grouped by section.
3. The designer tunes them live, then copies the final values.
4. A developer pastes them back into `config.ts` and opens a PR.

## Rules
- Development only. Load it behind `process.env.NODE_ENV !== 'production'` so it never ships.
- When a control changes, rebuild the GSAP timeline (kill and recreate) or set the value directly; no page reload.
