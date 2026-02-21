# companion-module-google-slidescontroller

Bitfocus Companion module for controlling the [Google Slides Opener](https://github.com/TomsFaire/Google-Slides-Controller) desktop app via its HTTP API.

See [companion/HELP.md](companion/HELP.md) for in-Companion setup. See [LICENSE](LICENSE) for license terms.

---

**Early release:** This module and the Google Slides Opener app are early-release software. Use with caution in production environments. Test thoroughly in rehearsal or non-critical setups before relying on them for important events.

---

## What this module does

This module connects Companion to the **Google Slides Opener** app running on your presentation computer. It sends commands over HTTP (default API port **9595**) so you can open presentations, move slides, control speaker notes, and read status—all from Companion buttons, feedbacks, and variables.

## Required app: Google Slides Opener

You must install and run the desktop app on the machine that will drive the presentation (or on a machine that Companion can reach on your network).

**[Download / source: TomsFaire/Google-Slides-Controller](https://github.com/TomsFaire/Google-Slides-Controller)**

### What the app provides

- **Full-screen Google Slides** on a chosen presentation monitor, with optional **speaker notes** on a second monitor.
- **Web UI** (default port 80): browser-based remote from phones, tablets, or laptops—previous/next slide, speaker notes, slide previews, optional stagetimer.io.
- **HTTP API** (default port 9595): the interface this Companion module uses. The app also supports other controllers (e.g. Q-SYS, Stream Deck) via the same API.
- **Presets:** Up to three preset presentation URLs you can open from Companion (Open Presentation 1 / 2 / 3).
- **Primary/backup mode:** Run the app on multiple computers; one primary can send commands to backup machines for failover.
- **Optional:** stagetimer.io integration, Slido support, display brightness control for the Web UI, and more. See the app repository for full documentation.

Configure the app’s **API port** (default **9595**) and, if Companion is on another machine, ensure the presentation computer’s firewall allows that port.

## How to use this module

1. Install and run the [Google Slides Opener](https://github.com/TomsFaire/Google-Slides-Controller) app on your presentation computer. Note its API port (default **9595**).
2. In Companion, go to **Modules** → **Import module package** and import this module’s `.tgz` (from [releases](https://github.com/bitfocus/companion-module-google-slidescontroller/releases) or the [Bitfocus Developer Portal](https://developer.bitfocus.io/)).
3. Add a connection for **Google Slides Controller**. Set **Host** (e.g. `127.0.0.1` if the app is on the same machine as Companion) and **Port** to the app’s API port.

The module polls the app about once per second and updates variables and feedbacks automatically.

## Actions

- **Open Presentation** (by URL), **Open Presentation with Notes**
- **Open Presentation 1 / 2 / 3** (presets configured in the app)
- **Close Current Presentation**, **Reload Presentation**
- **Next Slide**, **Previous Slide**, **Go to Slide** (by number)
- **Toggle Video Playback**
- **Open Speaker Notes**, **Close Speaker Notes**
- **Scroll Speaker Notes Up / Down**, **Zoom In / Zoom Out Speaker Notes**

## Variables

- `presentation_open`, `notes_open` (Yes/No)
- `current_slide`, `total_slides`, `slide_info` (e.g. 3 / 10)
- `next_slide`, `previous_slide`, `is_first_slide`, `is_last_slide` (Yes/No)
- `presentation_url`, `presentation_title`
- `timer_elapsed` (e.g. 00:00:06)
- `presentation_display_id`, `notes_display_id`
- `login_state` (Yes/No), `logged_in_user` (email)

## Feedbacks

- Presentation is Open  
- Speaker Notes are Open  
- On Specific Slide (by slide number)  
- Is First Slide / Is Last Slide  
- Logged In to Google  
