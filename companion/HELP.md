# Bitfocus Companion Module for Google Slides Controller

This module allows you to control the Google Slides Opener Electron app from Bitfocus Companion.

The app runs on your presentation computer and exposes an HTTP API; this module connects to that API to open presentations, navigate slides, control speaker notes, and more.

- **App (required):** [Google Slides Opener](https://github.com/nerif-tafu/gslide-opener) — run it on the same machine as Companion (or use the app’s Host/Port to point to another machine).

## Setup

1. Install and run the **Google Slides Opener** app on the computer that will drive the presentation (or the machine Companion will talk to).
2. In the app, note the **API port** (default **9595**).
3. In Companion, add this module and set **Host** (e.g. `127.0.0.1` if the app is on the same machine) and **Port** to match the app’s API port.

## Actions

- Open Presentation (by URL), Open Presentation with Notes
- Open Preset 1 / 2 / 3
- Close Presentation, Reload Presentation
- Next / Previous Slide, Go to Slide
- Open / Close Speaker Notes, Scroll Notes Up/Down, Zoom In/Out Notes
- Toggle Video Playback

See the main app repository for full documentation.
