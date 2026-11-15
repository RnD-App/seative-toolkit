# Figma handoff

- **Name layers** and use **auto layout**. Both plugins keep names and layout; messy files come out messy.
- **Real fonts.** Fig-to-Rive needs the `.ttf` files in `Fonts Library/`; seaMotion reads fonts from
  `~/Documents/seaMotion/Fonts`.
- **For seaMotion:** use [Fig-to-SeaMotion](../repos/fig-to-seamotion.md) with the cleaners on. For Lottie, run the
  **Lottie** tab's **Analyze selection** first and fix what it lists.
- **For Rive:** use [Fig-to-Rive](../repos/fig-to-rive.md); tick **Safe layout** if it is going into Webflow.
- **Let Claude read the file** with [Figma MCP Bridge](../mcp/figma-mcp-bridge.md) instead of describing the design by hand.
- **Mark motion intent** in Figma (a note or a prototype link): what moves, when, and how fast. It saves a round of guessing.
- **Export pictures at the size they will show**, not 4× by default.
