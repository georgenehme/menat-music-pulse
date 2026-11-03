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
- Apple Music RSS most-played charts, Kworb Spotify daily charts, Kworb YouTube weekly charts and Anghami country Top 50 charts are distinct sources; coverage varies by market.
- An Anghami connection is prepared for Palestine and Syria's official country Top 50 playlists, but its public pages currently block the cloud collector with browser verification. Production coverage remains 16 markets until approved access or another verified feed is available. Source status exposes this limitation; local test snapshots are not production data.
- When accessible, Anghami source dates are playlist update timestamps, distinct from collection times, and each country starts its own baseline. All collection remains in the cloud.

## Labels and release credits

Track details display **record label** and **distributor** separately when the
private cloud collector finds a reliable match in ChartEX's free public chart
previews. Matching requires the same platform, market, chart date, rank, title
and artist; Apple release dates must also agree. Every result is attributed to
ChartEX with a checked date. It is a reported credit, not an independent rights
or ownership verification. Public preview coverage is partial.

Apple Music album **℗/© release credits** are displayed separately, after checking
the album ID, market and membership of the exact song ID. They are never used
to infer a label, publisher or distributor. Missing labels say **Not available**.
Cached credits expire after 30 days; album credits are collected in daily batches
and rechecked weekly. All lookups run privately in the cloud, without paid API
access or manual imports. The CSV export includes available label attribution.

## Hosting

GitHub Pages serves `main` at the repository root. Only public frontend files and the
validated JSON export belong here. The private collector uses a dedicated deploy key
to update that JSON file. Do not copy its source, state, snapshots or secrets here.

For a local preview: `python -m http.server 8765 --bind 127.0.0.1`.
Watchlists and theme choices remain in the visitor's browser. No newsletter subscriptions
or email delivery are connected in this release. See `privacy.html`.
