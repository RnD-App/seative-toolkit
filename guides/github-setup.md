# GitHub setup and workflow

## Install and sign in
```bash
brew install git gh      # Mac
gh auth login
```

## Where repos live
- **RnD-Products**: our apps and tools (seaMotion, the Figma plugins, go-commands). `go pr` creates new repos here.
- **RnD-App**: this toolkit.

## How we work
- `main` is protected. Nobody pushes to it directly.
- Work on a branch: `feat/…`, `fix/…`, `docs/…`.
- Every change goes in through a pull request that someone else reviews.
- The easy way: say `go pr` in Claude Code ([go-commands](../repos/go-commands.md)).

## Every repo has
- `README.md`: what it is, how to run it, how to deploy it.
- `.gitignore`: at least `node_modules`, `.next`, `dist`, `.env*`, `.DS_Store`.
- `.env.example`: every environment variable the project needs, with no real values.
- `.nvmrc`: the Node.js version.
- `CLAUDE.md`: run commands, stack and rules for Claude Code.

## Never commit
`.env` files, API keys, tokens, client data, large videos (link them or use a release).
