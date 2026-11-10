# Chrome extensions

## Using other people's extensions
- Check the listing's permissions and reviews before installing. Prefer known publishers.
- In `chrome://extensions` > Details, set **Site access** to **On click** when an extension doesn't need every page.
- Use a separate Chrome profile for small or rarely updated extensions.
- Review your extensions every few months and remove what you don't use.

## Building our own
- Use **Manifest V3**. Start from [Chrome extension samples](https://github.com/GoogleChrome/chrome-extensions-samples).
- Test with **Load unpacked** in `chrome://extensions` (turn on Developer mode).
- Ask only for the permissions you need; every extra one makes review slower and users warier.
- Bump `version` in `manifest.json` for every release.
