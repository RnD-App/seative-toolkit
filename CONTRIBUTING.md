# Adding to the toolkit

Changes reach `main` only through a pull request that someone else reviews.

## Add a tool, extension or link

1. Copy [templates/resource-template.md](templates/resource-template.md) into the right folder
   (`repos/`, `extensions/`, `stack/` …). Name it in lowercase with dashes: `my-tool.md`.
2. Fill in every field, including **Owner** (who to ask) and **Last checked** (today's date).
3. Add one line for it in [links.md](links.md) and, if it is a new folder, in the map in [README.md](README.md).
4. Open a pull request. Saying `go pr` in Claude Code does this for you (see [repos/go-commands.md](repos/go-commands.md)).

## Rules

- **Link, don't copy.** Never paste someone else's code, paid prompts or licensed files into this repo.
- **Check the licence** before we fork or reuse anything, and write it on the page.
- **Keep pages short.** One page per tool; put long how-tos in `guides/`.
- **Date your checks.** Links go stale; update **Last checked** when you confirm a page still works.
- No secrets, tokens, client data or personal paths.
