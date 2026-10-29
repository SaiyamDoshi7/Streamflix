# StreamFlix: Netflix-style Full Stack App

**Tech:** HTML, CSS, Bootstrap 5, vanilla JavaScript (ES modules), Node.js, Express, JWT, bcrypt, TMDB API (optional)

## Features
- Register / login with JWT, bcrypt-hashed passwords, protected API
- Auto-rotating hero banner, Top 10 row, genre rows with arrow scrolling and hover cards
- Details modal with real YouTube trailers (with a TMDB key)
- My List saved per user on the server
- Instant search, keyboard friendly (Enter opens, Esc closes), responsive

## Run (Node.js 18+)
```bash
npm install
npm run dev
```
Open http://localhost:3000. Without a key you get a built-in sample catalogue.

## Real movies and trailers (free)
1. Create a free account at themoviedb.org and copy your API key.
2. Copy `.env.example` to `.env` and paste the key after `TMDB_KEY=`.
3. Restart `npm run dev`.

## Structure
`server/` Express API (auth, catalogue, My List) | `public/js/` api.js, components.js, app.js

## Video playback
- Everything plays from this project, with no external video links. Videos live in `public/videos/`.
- **Open Movies:** Big Buck Bunny, © Blender Foundation, licensed CC BY 3.0 (www.bigbuckbunny.org).
- **Demo Reels:** short original animations generated with ffmpeg.
- **My Videos:** drop any `.mp4` / `.webm` into `public/videos/` and restart. Optional `NAME.jpg` (poster) and `NAME-wide.jpg` (banner); without them a coloured placeholder is generated.
- **Trailers** of real movies appear when you add a TMDB key. Full copyrighted movies cannot be streamed legally.
- Player: play/pause, seek, ±10s, volume, speed, fullscreen, auto-hiding controls, resume, Continue Watching.
- Shortcuts: Space/K play, ←/→ skip 10s, ↑/↓ volume, M mute, F fullscreen, Esc close.

## Real movies and series (TMDB)
With a free TMDB key the home page fills with real movies and series: posters, descriptions, ratings, a Bollywood row, genre rows, trailers, and seasons with episode lists for every series.
1. Sign up at https://www.themoviedb.org, then Settings > API > create a key (type: Developer).
2. Open `.env` and paste the **API Key (v3)** after `TMDB_KEY=`.
3. Restart `npm run dev`.

Movies and series play their official trailers (YouTube). Full copyrighted films cannot be streamed legally, so the full-length player is used for open-licensed films (Open Movies row). Download Sintel, Tears of Steel, Elephants Dream or Cosmos Laundromat from blender.org (CC BY), save them in `public/videos/` as `sintel.mp4`, `tears-of-steel.mp4`, `elephants-dream.mp4`, `cosmos-laundromat.mp4` and they get proper titles automatically.
