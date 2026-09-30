# Sonic Memoir — Spotify Editorial Showcase

A dark, editorial-style personal music journal built with React 19, TypeScript, Tailwind CSS v4 and Vite. It renders your top tracks, curated playlists, recently played and an artist spotlight as a "visual autobiography written in melodies".

## Quick start

```bash
npm install
npm run dev
```

## Live Spotify data (optional)

Without credentials the app shows local mock data and a small banner saying so. To load your own account:

1. Create an app in the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard) and set its Redirect URI to `http://127.0.0.1:8888/callback`.
2. Copy `.env.example` to `.env` and fill in `VITE_SPOTIFY_CLIENT_ID` and `VITE_SPOTIFY_CLIENT_SECRET`.
3. Run `npm run spotify:token`, open the printed URL, approve, then paste the resulting refresh token into `.env` as `VITE_SPOTIFY_REFRESH_TOKEN`.
4. Restart `npm run dev`.

## Scripts

- `npm run dev` — start the Vite dev server
- `npm run build` — type-check and build for production
- `npm run preview` — preview the production build
- `npm run lint` — run ESLint
- `npm run spotify:token` — helper that walks the Spotify OAuth flow and prints a refresh token

## Structure

- `src/components/` — Navbar, Hero, Marquee, TopTracks, Playlists, RecentlyPlayed, ArtistSpotlight, PlaylistDetail, PreviewPlayer, Footer
- `src/services/spotify.ts` — Spotify Web API client (falls back to mock data)
- `src/data/mockData.ts` — local mock content used when no credentials are set
