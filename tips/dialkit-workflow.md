# DialKit workflow

1. A developer puts every tunable value in `config.ts` and shows it with `useDialKit`, one panel per section.
2. The designer runs the site locally (or on a dev preview) and tunes the dials until it feels right.
3. The designer copies the final values and sends them (or opens a PR).
4. The developer pastes them into `config.ts`. The defaults are now the tuned values.

Rules:
- DialKit is **development only**; it must not be in the production bundle (check in the launch checklist).
- Give every control a sensible `[default, min, max]` so nobody can drag a value into something broken.
- Name panels after page sections (`Hero`, `Work`, `Scene`) so designers can find them.

Setup: [repos/dialkit.md](../repos/dialkit.md).
