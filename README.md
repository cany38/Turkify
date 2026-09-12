# Turkify

Turkify is my personal music app. It lives in the browser. No installer, no Electron build, just search, playlists, likes, downloads, an equalizer and a small remix panel in one tab.

Two copies sit in this repo: one for Windows, one for macOS. Each folder has its own README with the setup steps, so start there. This file is only the overview.

## What it looks like

### Home

![Home](docs/screenshots/01-home-most-played.png)

Home collects your most played playlists and your liked songs, with the player bar pinned to the bottom on every page.

### Search

![Search](docs/screenshots/02-search-results.png)

One box searches your local files, YouTube and Spotify at the same time. Each row wears a badge showing where it came from, and each row downloads on its own. No queue juggling for a single song.

### Equalizer

![Equalizer](docs/screenshots/03-settings-equalizer.png)

Eight bands, 60 Hz to 12 kHz. Presets cover the usual suspects: Flat, Bass Boost, Vocal, Treble, plus one called Pastel Ghost. Drag a band down to cut, up to boost. It sticks to the device and hits every song.

### Remix

![Remix](docs/screenshots/04-remix-slowed-reverb.png)

Three presets up top: Normal, Slowed + Reverb, Sped Up, with three sliders underneath for speed, reverb and bass boost. Dial something in. Then either reset it, keep it as that song's default, or download the whole thing as WAV.

### Playlist

![Playlist](docs/screenshots/05-playlist-detail.png)

Cover up top, song count and total runtime next to it, a search box when the list gets long. Rows you already downloaded carry their codec and bitrate.

### Language and audio format

![Settings](docs/screenshots/06-settings-language-audio.png)

Turkish, Azerbaijani, English. Pick one and the whole app follows. Same page decides the codec for playback and future downloads, Opus packing more quality into the same file size while AAC behaves better on iPhones.

### Import from Spotify and YouTube

![Import](docs/screenshots/07-import-playlist.png)

Paste a public playlist link. Turkify keeps the name, the cover and the track list, no login on either side. Files don't come down by themselves. You grab them row by row, later, whenever. Private lists are invisible to the importer, so make them public first.

## Setup

Short version. Details live in the folder READMEs:

- Windows (`Turkify windows/`): install Node.js 22+, Python 3.12, FFmpeg and Deno, then `python -m pip install "yt-dlp[default]" spotdl spotapi`. Double-click `Launcher.bat`, the browser opens at `http://localhost:3400`.
- macOS (`turkify mac/`): run `bash Setup.command`, then open `Turkify.app`. The browser opens at `http://127.0.0.1:3401`.

## Warnings

- Personal use only. No DRM bypass in here, so only pull down stuff you actually have the right to use.
- Closing the tab doesn't stop the server. Windows: `Durdur.bat`, or the stop button under Settings, Server. macOS: `Stop.command`.
- Search and downloads phone third-party services, which is how a Spotify match can resolve to YouTube audio.
- The mac app is unsigned and not notarized, so right-click, Open on first launch, and only if you trust where it came from.
- Keys and preferences live in browser storage. No vault there.
- Screenshots show a sample library, not a real collection.

## License

Shared license in the root `LICENSE` file.
