# go-commands

| | |
|---|---|
| Source | [RnD-Products/go-commands](https://github.com/RnD-Products/go-commands) |
| Licence | none set yet |
| Owner | (add) |
| Last checked | 2026-11-10 |

## What it does
Shortcut commands for Claude Code. Install once per computer; they work in every project. The project is the folder
Claude Code is open in, and the repo is that folder's `origin`.

| Say | What happens |
|---|---|
| `go pr` | Saves the project to GitHub as a pull request. Not on GitHub yet? Creates a private repo (under the team owner) and pushes to `main` first. |
| `go update` | Pulls the latest version from GitHub. Replaced files go to the Trash (Mac) or `~/go-update-backups/`; local-only files are kept. |
| `goapp update` | Checks first, and updates only if the project is behind GitHub. |

## Install (team setup, once per computer)
```bash
gh auth login
git clone https://github.com/RnD-Products/go-commands.git ~/go-commands
~/go-commands/install.sh --owner RnD-Products
```
Restart Claude Code. `--owner RnD-Products` makes `go pr` create new repos in the team org instead of your own account.

Update later:
```bash
cd ~/go-commands && git pull && ./install.sh --owner RnD-Products
```

Works on macOS and Linux. On Windows, use it inside WSL.

## Daily routine
| When | Say |
|---|---|
| Start of the day | `goapp update` |
| After a change | `go pr` |
| Local copy broken, or after a big merge | `go update` |

## Why it is safe
- `go pr` works on a separate copy, never touches your current branch, never merges or force-pushes.
- It stops if it finds secrets, or if many files would be deleted, and runs the project's tests before pushing.
- `go update` never hard-deletes and keeps files GitHub doesn't have.

## Contributing
Edit `skills/<command>/SKILL.md` or `install.sh` in the go-commands repo and open a PR; someone else reviews it.
