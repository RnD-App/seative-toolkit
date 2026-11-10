# Rive interactive piece

Needs the Rive CLI and the Rive skill: see [guides/rive-agent-workflow.md](../guides/rive-agent-workflow.md).

````markdown
Create an interactive Rive [button / toggle / loader / onboarding step / character] for [brand].
Use the Rive CLI; if this is a Rive CLI project, read its AGENTS.md first and follow it.
- Look: [size, colours, shapes, or "start from the Fig-to-Rive export in [folder]"]
- States: [idle, hover, pressed, success]
- State machine inputs: [isHovered: boolean, isPressed: boolean, progress: number]
- Events the site listens for: [onComplete]
- Respect reduced motion
Then add it to the Next.js page with rive-react:
- Load the .riv, set the inputs from the page, react to the events
- Wire the inputs to DialKit in a "[Piece name]" panel (dev only)
- Keep all visuals and motion in the .riv file, not in app code
````
