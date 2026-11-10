# Git and pull requests

- `main` is protected. Work on branches named `feat/…`, `fix/…` or `docs/…`, or just say `go pr`.
- Keep pull requests small: one feature or fix each. Big PRs don't get reviewed properly.
- For any motion change, put the **preview URL** and a short **screen recording or GIF** in the PR
  (make the GIF with [ffmpeg](../stack/ffmpeg.md)).
- Someone else reviews and merges. Don't merge your own PR unless it is an emergency, and say so in the PR.
- Never commit `.env`. Commit `.env.example` with the names only.
- Start the day with `goapp update` so you build on the latest work.
