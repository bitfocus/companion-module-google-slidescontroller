# companion-module-google-slidescontroller

Bitfocus Companion module for controlling the [Google Slides Opener](https://github.com/nerif-tafu/gslide-opener) desktop app via its HTTP API.

See [companion/HELP.md](companion/HELP.md) for in-Companion help and setup. See [LICENSE](LICENSE) for license terms.

## What this module does

The module talks to the **Google Slides Opener** Electron app (default API port **9595**). That app runs on your presentation computer and opens Google Slides in full-screen with optional speaker notes on a second display. This Companion module sends commands (open presentation, next/previous slide, notes control, etc.) over HTTP.

- **App repo:** [nerif-tafu/gslide-opener](https://github.com/nerif-tafu/gslide-opener) (and community forks)
- **Module repo:** [bitfocus/companion-module-google-slidescontroller](https://github.com/bitfocus/companion-module-google-slidescontroller)

## Development

- Install dependencies: `yarn install`
- Build package: `yarn run package` (produces a `.tgz` for import into Companion)
- Format: `yarn run format`

## Releasing

1. Update `package.json` version (e.g. `1.0.1`).
2. Create a Git tag with a `v` prefix (e.g. `v1.0.1`).
3. Submit the version in the [Bitfocus Developer Portal](https://developer.bitfocus.io/) (My Connections → this module → Submit Version → choose the tag).

Only versions submitted there are reviewed and then distributed to Companion users. See [Releasing your module](https://github.com/bitfocus/companion-module-base/wiki/Releasing-your-module).
