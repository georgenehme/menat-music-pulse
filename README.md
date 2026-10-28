# MENAT Music Pulse

MENAT Music Pulse is an interactive regional music-chart discovery dashboard covering the Middle East, North Africa, Turkey, and Pakistan.

## Current public version

This repository hosts the **standalone interactive preview** in `index.html`. It contains clearly labelled demonstration chart data. **Live chart scanning and newsletter subscriptions are not enabled here.** No secrets or subscriber addresses belong in this public repository.

## Publish using GitHub Pages

1. Open [Settings → Pages](https://github.com/georgenehme/menat-music-pulse/settings/pages).
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Choose branch `main` and folder `/(root)`, then click **Save**.
4. Open [the website](https://georgenehme.github.io/menat-music-pulse/) after GitHub reports a successful Pages deployment.

The public URL is not guaranteed to work until GitHub Pages is enabled.

## Next phase

Keep chart-scanner scripts, snapshot history, email-provider secrets and any licensed data in a **separate private repository** or private backend. Publish only non-sensitive dashboard data. The Friday newsletter requires a configured third-party subscription and delivery provider.

**Security:** Visitors can inspect public HTML, CSS and JavaScript. Never put API keys, personal data, private reports or subscriber lists in a publicly hosted website.