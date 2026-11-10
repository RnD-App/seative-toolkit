# Claude Code for teams

- **Every repo gets a `CLAUDE.md`**: how to run, build and test it, the stack, and our rules. Claude reads it every time.
- **Same commands for everyone.** Install [go-commands](../repos/go-commands.md) with `--owner RnD-Products`.
- **Shared skills.** House rules that repeat across projects belong in a skill (see
  [Claude motion skill](../stack/claude-motion-skill.md)), shared through a repo like go-commands.
- **Plan first.** For big changes, ask Claude for a plan before it edits anything.
- **Review the diff** before you `go pr`. You own what you push, not Claude.
- **MCP servers** (Rive, GetLayers …): agree as a team before adding one, and write the setup into the tool's page here.
- **No secrets in prompts.** Don't paste API keys or client data into a chat.
