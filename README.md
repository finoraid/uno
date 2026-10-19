# UNO Arena — Railway starter

Mobile-first UNO-style web game starter with a custom lobby, real-time rooms, AI opponents, browser-generated sound effects, and custom music controls.

## Run locally

Requires Node.js 20+.

```bash
npm install
npm start
```

Open `http://localhost:3000`.

## Deploy to Railway

1. Upload this project to a GitHub repository.
2. Create a new Railway service from that repository.
3. Railway detects Node.js; the start command is `npm start`.
4. In Railway service settings, generate a public domain.
5. The app uses `process.env.PORT`, so no hard-coded port is needed.

## Music and effects

- Open **Music & sound** to upload an audio file for the current browser session.
- Or provide a direct URL to an audio file you have permission to use (MP3/OGG, depending on browser/server headers).
- YouTube links can be embedded in the platform player. Spotify links open in Spotify; playback may require a Spotify account/app.
- Sound effects are synthesized in-browser with Web Audio (card play, draw, UNO, wild, win/lose), so no third-party audio files are required.
- Browser autoplay restrictions mean music may require a user tap.

For a track that should be available to every player, host it at a stable URL and configure that URL in the UI. Uploading a file from a phone is local to that browser session and is not uploaded to Railway.

## Current starter scope

- Room creation/join by code, quick room discovery, and four-player AI mode with Easy/Normal/Hard choice.
- Real-time game state via Socket.IO.
- Card actions, color selection, +2/+4 same-type stacking, and penalty draw.
- No persistent account/leaderboard database yet. Player name is session-based; add PostgreSQL/Redis before scaling across multiple server instances.
- This is an original UNO-inspired implementation, not affiliated with or endorsed by Mattel. Use your own branding/assets and review applicable rules/trademark requirements before public launch.
