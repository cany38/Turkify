# Turkify

Turkify is my personal music app. It runs in the browser, there is no installer and no Electron build. Search, playlists, likes, downloads, an equalizer and a small remix panel live in one place.

Two copies sit in this repo: one for Windows, one for macOS. Each folder has its own README with setup steps. Start there, this file is only an overview.

## What it looks like

### Home

![Home](docs/screenshots/01-home-most-played.png)

The home page collects your most played playlists and your liked songs. The player bar at the bottom stays on every page.

### Search

![Search](docs/screenshots/02-search-results.png)

One search box covers your local files, YouTube and Spotify at once. The badge on the right shows where each row came from, and every row has its own download button.

### Equalizer

![Equalizer](docs/screenshots/03-settings-equalizer.png)

Eight bands from 60 Hz to 12 kHz, with presets such as Flat, Bass Boost, Vocal, Pastel Ghost and Treble. Pull a band down to cut it, push it up to boost it. The setting stays on your device and applies to every song.

### Remix

![Remix](docs/screenshots/04-remix-slowed-reverb.png)

The remix panel has three presets: Normal, Slowed + Reverb and Sped Up, plus sliders for speed, reverb and bass boost. You can reset, save the current setting as that song's default, or download the result as a WAV file.

### Playlist

![Playlist](docs/screenshots/05-playlist-detail.png)

A playlist page shows the cover, the song count and the total length, with a search box for the list itself. Downloaded rows show their codec and bitrate.

### Language and audio format

![Settings](docs/screenshots/06-settings-language-audio.png)

The app speaks Turkish, Azerbaijani and English. Playback and future downloads use the codec you pick here: Opus for higher quality at the same size, AAC for Apple devices.

### Import from Spotify and YouTube

![Import](docs/screenshots/07-import-playlist.png)

Paste a public playlist link and Turkify saves the name, the cover and the tracks. No login is needed. Audio files are not downloaded automatically, you download them per row later. Private lists cannot be imported.

## Setup

Short version, details are in the folder READMEs:

- Windows (`Turkify windows/`): install Node.js 22+, Python 3.12, FFmpeg and Deno, then `python -m pip install "yt-dlp[default]" spotdl spotapi`. Double-click `Launcher.bat`, the browser opens at `http://localhost:3400`.
- macOS (`turkify mac/`): run `bash Setup.command`, then open `Turkify.app`. The browser opens at `http://127.0.0.1:3401`.

## Warnings

- Personal use only. There is no DRM bypass here, so only fetch content you have the right to use.
- Closing the browser tab does not stop the server. On Windows use `Durdur.bat` or the stop button under Settings, Server. On macOS run `Stop.command`.
- Search and downloads send requests to third-party services. A Spotify match may resolve to YouTube audio.
- The macOS app is unsigned and not notarized by Apple. If you trust the source, open it with right-click, Open the first time.
- API keys and preferences sit in browser storage. That is not an encrypted vault.
- The screenshots show sample library content, not a real collection.

## License

Shared license in the root `LICENSE` file.
