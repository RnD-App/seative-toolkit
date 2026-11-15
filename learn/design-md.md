# DESIGN.md: design systems for AI agents

| | |
|---|---|
| Browse | [getdesign.md](https://getdesign.md) |
| Collection | [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md) (MIT, 84 files) |
| Starting points | [VoltAgent/awesome-claude-design](https://github.com/VoltAgent/awesome-claude-design) (68 design systems for Claude Design) |
| Format spec | [Google Stitch DESIGN.md](https://stitch.withgoogle.com/docs/design-md/overview) · [google-labs-code/design.md](https://github.com/google-labs-code/design.md) |
| Owner | (add) |
| Last checked | 2026-11-15 |

## What it is
A plain Markdown file in the project root that tells an AI agent how the UI should look: colours, type, spacing,
components and rules. Google Stitch created the format.

| File | Tells the agent |
|---|---|
| `CLAUDE.md` / `AGENTS.md` | How to build the project |
| `DESIGN.md` | How it should look and feel |

## Find one by industry
All on [getdesign.md](https://getdesign.md):

| Industry | Examples |
|---|---|
| AI & LLM platforms | Claude, Cohere, ElevenLabs, Mistral AI, Ollama, Replicate, Runway, xAI |
| Developer tools | Cursor, Expo, Lovable, Raycast, Superhuman, Vercel, Warp |
| Backend, database, DevOps | ClickHouse, HashiCorp, MongoDB, PostHog, Sanity, Sentry, Supabase |
| Productivity & SaaS | Cal.com, Intercom, Linear, Mintlify, Notion, Resend, Zapier |
| Design & creative tools | Airtable, Clay, Figma, Framer, Miro, Webflow |
| Fintech & crypto | Coinbase, Kraken, Mastercard, Mercury, Revolut, Stripe, Wise |
| E-commerce & retail | Airbnb, Nike, Shopify, Starbucks |
| Media & consumer tech | Apple, DJI, IBM, NVIDIA, Oura, Pinterest, Spotify, The Verge, Uber, WIRED |
| Automotive | BMW, Bugatti, Ferrari, Lamborghini, Renault, Tesla |
| Retro web | Dell (1996), Nintendo.com (2001) |

[awesome-claude-design](https://github.com/VoltAgent/awesome-claude-design) uses the same groups.

## How we use it
1. Pick 2–3 DESIGN.md files from the client's industry as a quality reference.
2. Write the client's own `DESIGN.md` in the project root: their colours, fonts, spacing and components. Add our
   motion presets from [motion-presets.md](motion-presets.md) so motion is part of the design system.
3. Tell Claude: "Build this page following DESIGN.md." The [website prompt](../prompts/website-create-prompt.md)
   already asks for it.
4. Keep `DESIGN.md` up to date when the design changes, like `CLAUDE.md`.

## Rules
- The files on getdesign.md are worked out from each brand's public website. Use them for structure and quality,
  **never** to copy a brand's look for a client.
- The client's `DESIGN.md` comes from the client's real brand (Figma file, brand guide), not from someone else's.
- Third-party tools to install DESIGN.md files exist (for example `npx @webdesignhot/design-md`); check them before use.
