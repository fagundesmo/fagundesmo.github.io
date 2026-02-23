# fagundesmo.github.io

## Spotify Now Playing Setup

The bottom-right widget uses Spotify OAuth (PKCE) and shows your current track in real time.

1. Create a Spotify app at https://developer.spotify.com/dashboard.
2. Add your GitHub Pages URL as a Redirect URI:
   - `https://fagundesmo.github.io/`
   - `https://fagundesmo.github.io/index.html`
   - Add local dev URL too if needed: `http://127.0.0.1:5500/`
3. Open `/index.html` and replace:
   - `var SPOTIFY_CLIENT_ID = 'YOUR_SPOTIFY_CLIENT_ID';`
   - with your real Spotify app client ID.
4. Commit and deploy to GitHub Pages.
5. Click `Connect` in the site widget and authorize Spotify.

Notes:
- Required scopes are `user-read-currently-playing` and `user-read-playback-state`.
- Tokens are stored in browser `localStorage` for your session.
- Public users cannot click a Disconnect button anymore (connect-only UI).
- `Mute` mutes widget updates/text only; this widget does not stream audio playback.
