# MENAT Music Pulse

A public music chart dashboard for MENAT and Pakistan. The page reads the validated
`data/radar.json` export and refreshes it every five minutes while open. It contains
no chart scanner, import controls, demonstration tracks, credentials or subscriber data.

The private background collector runs separately and updates the public data file
daily around 12:00 Dubai time. See the dashboard's collection status and source dates
for actual freshness. Scheduled runs and upstream feeds may be delayed.

## Data interpretation

- Each source and market starts with a complete baseline. The baseline produces no new-entry alerts.
- First observations, re-entries and rank movements are distinct. A first observation is not a lifetime debut.
- Missing, partial or stale sources are disclosed. Last good charts may be retained with their original dates.
- Unsubstantiated explanations say **Reason not verified**.
- Apple Music RSS most-played charts, Kworb Spotify daily charts and Kworb YouTube weekly charts are distinct sources; coverage varies by market.

## Hosting

GitHub Pages serves `main` at the repository root. Only public frontend files and the
validated JSON export belong here. The private collector uses a dedicated deploy key
to update that JSON file. Do not copy its source, state, snapshots or secrets here.

For a local preview: `python -m http.server 8765 --bind 127.0.0.1`.
Watchlists and theme choices remain in the visitor's browser. No newsletter subscriptions
or email delivery are connected in this release. See `privacy.html`.
