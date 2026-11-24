# StreamSync - Creator Control Room

StreamSync combines Twitch-style streaming with Discord-style community in one place.

## Latest Fix - Stop Stream + Glitch
- Go Live Studio NOW HAS Stop Stream in 3 places: sticky top bar with timer, control bar under preview, mobile bottom bar.
- Clicking Stop shows confirm, ends stream, stops timer, hides LIVE pill, shows Stream Ended summary.
- Glitch fixes: avatar no longer clipped by banner, video grid has bottom padding so last row fully visible, no VIDEO THUMBNAIL placeholder text, sidebar red dot aligned.

## Structure
- index.html = Main app (single-file, works on GitHub Pages)
- css/style.css = Extra styles
- js/main.js = Helpers + TODOs for production
- assets/logos/ = Proper SVG logos for all platforms
- manifest.json = PWA manifest

## How to run locally
1. Unzip, open index.html in Chrome / Safari / Firefox / Edge
2. Login demo: demo@streamsync.gg / demo123 OR Google / Twitch / Discord demo OAuth
3. Works on Mobile, Tablet, PC

## GitHub Pages (Free)
1. Push this repository to GitHub.
2. In the repository, open **Settings > Pages** and set **Build and deployment > Source** to **GitHub Actions**.
3. The included workflow publishes the `streamsync-github` folder whenever you push to `main`. You can also run it from the **Actions** tab with **Run workflow**.
4. After the workflow succeeds, open the Pages URL shown in the workflow run. For a project site, it is usually `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`.

## Test Stop Stream
1. Go Live Studio > Go Live > Verify Stop Stream appears + LIVE pill appears
2. Click Stop Stream > Confirm > Verify stream ends, timer stops, LIVE pill disappears
3. Profile > Verify avatar not clipped, video grid fully visible

## Notes
- OAuth is DEMO. For real login add real Client IDs in js/main.js and use Firebase / Supabase Auth.
- Mic/Camera are preview-mode. Real mic needs getUserMedia on https (works on GitHub Pages https).
- License MIT