# Spotify_clone

[Live Demo](https://williumtiwari.github.io/Spotify_clone)

A minimal, static Spotify-like web music player built with plain HTML, CSS and JavaScript.

This project is a simple client-side demo that mimics basic music player functionality:

- Play / Pause
- Next / Previous track
- Progress bar / seek
- Playlist with cover images and titles
- Animated playing indicator

---

## Demo / Preview

Open `index.html` in your browser to run the app locally.

## How to run (Windows / PowerShell)

Option 1 — open directly:

- Double-click `index.html` or in PowerShell run:

  Start-Process -FilePath .\index.html

Option 2 — serve with Python's simple HTTP server (recommended for consistent audio behavior):

    python -m http.server 8000

Then open http://localhost:8000 in your browser.

Option 3 — serve with npm `http-server` (if you prefer Node.js):

    npx http-server -p 8000

---

## Project structure

- `index.html` — main UI
- `style.css` — styles
- `script.js` — main player logic and playlist data
- `README.md` — this file
- `favicon.ico`, `logo.png`, `bg.jpg`, `playing.gif` — assets used by the UI
- `covers/` — album art images used in the playlist
- `songs/` — mp3 files used by the demo

Contents of `covers/` and `songs/` are simple placeholders used by the demo. Filenames are referenced from `script.js`.

---

## Adding or editing songs

Open `script.js` and edit the `songs` array. Each item is an object with:

- `songName` — displayed title
- `filePath` — relative path to the audio file (e.g. `songs/1.mp3`)
- `coverPath` — relative path to the cover image (e.g. `covers/1.jpg`)

Make sure the audio and image files exist in the referenced locations and that indices match the playlist UI (the current UI expects up to 10 items by default).

Example entry:

    { songName: "Artist - Track", filePath: "songs/11.mp3", coverPath: "covers/11.jpg" }

If you add more tracks, also update the markup or ensure the `.songItem` elements correspond to the playlist length.

---

## Notes and suggestions

- This is a static demo. Audio files included in the `songs/` folder may be copyrighted; replace them with your own licensed audio for public use.
- The app uses the Font Awesome kit (loaded in `index.html`). If you want to work offline, provide a local copy or adjust icons.
- The UI is basic and not fully responsive — feel free to extend `style.css` and `index.html` for improved layouts and accessibility.

---

## Contributing

Simple contributions are welcome: fix bugs, improve styles, or add features. Fork the repo, make changes, and open a pull request.

---

## License

MIT License — see LICENSE or add one if you need a different license.

---

Created by the repository owner.
