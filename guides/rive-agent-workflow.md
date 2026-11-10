# Rive with an agent: interactive motion

From a Figma frame to an interactive Rive piece on a Next.js site, with Claude doing the setup.

## Set up once
1. Install the Rive CLI and sign in (see [stack/rive.md](../stack/rive.md)).
2. Install the official Rive skill in Claude Code: `/plugin marketplace add rive-app/skills`, then
   `/plugin install rive@rive` (in a `claude` terminal).
3. Optional: set up [Fig-to-Rive](../repos/fig-to-rive.md) to bring Figma frames in.
4. Optional: add an MCP server for Rive (see [stack/rive.md](../stack/rive.md#rive-mcp)). Ask in the team first.

## The workflow
1. **Design** the piece in Figma.
2. **Bring it in**: send the frame with Fig-to-Rive, or describe it and let the agent build it from scratch.
3. **Add motion with the agent**: ask Claude to use the Rive CLI. It reads the project's `AGENTS.md` (written by
   `rive create`) and builds the states, state machine, inputs and events.
   Prompt: [prompts/rive-interaction-prompt.md](../prompts/rive-interaction-prompt.md).
4. **Refine**: a designer opens the same file in the Rive editor and polishes it.
5. **Put it on the site** with [rive-react](https://github.com/rive-app/rive-react): load the file, set its state
   machine inputs, listen for its events. Keep the visuals and motion in the `.riv` file, not in app code.
6. **Tune live**: wire the state machine inputs to [DialKit](../repos/dialkit.md) in development.
7. **Review**: open a PR with a preview GIF ([ffmpeg](../stack/ffmpeg.md)) or the preview URL.

## Tips
- Name inputs and events clearly (`isHovered`, `progress`, `onComplete`); the site code depends on them.
- Respect reduced motion in the Rive file (Rive supports it) and on the site.
- Check the `.riv` file size before shipping; embedded pictures add up fast.
