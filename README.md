# Best of 13 — Multiplayer

An installable Progressive Web App for keeping scores across 13 games for 1–5 players.

## Features

- Select 1–5 players.
- Enter player names by card-draw rank, up to 10 characters each.
- Dynamically generated scorecard and totals.
- Lowest total score ranks first.
- Dealer rotation runs downward through the card-draw ranks: final rank, previous rank, and so on to Rank 1, then repeats.
- Joker advances from Ace through King.
- Use `-` to record a zero score.
- Sticky totals/rankings/current dealer/current joker and sticky table header.
- Saves the active match locally on the device.
- Offline support through a service worker.

## Files

- `index.html` — complete app.
- `manifest.webmanifest` — installation metadata.
- `sw.js` — offline cache and update handling.
- `icon-192.png`, `icon-512.png`, `icon-1024.png` — app icons.

## GitHub Pages deployment

1. Create a new GitHub repository.
2. Upload all files from this folder to the repository root.
3. Open **Settings → Pages**.
4. Choose **Deploy from a branch**.
5. Select `main` and `/ (root)`.
6. Save and wait for the deployment to turn green.

After changing the app, increment the cache version near the top of `sw.js`, for example:

```js
const CACHE = "best-of-13-multiplayer-v1.0.1";
```

## Install on iPad

Open the deployed site in Safari, tap **Share**, then **Add to Home Screen**.
