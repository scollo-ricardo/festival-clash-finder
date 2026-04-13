# Graspop Metal Meeting 2026 — Festival Planner

A lightweight, client-side festival schedule planner for [Graspop Metal Meeting 2026](https://www.graspop.be). Browse the full lineup across 5 stages and 4 days, star your must-see bands, and spot time clashes before they happen.

## Features

- **Timeline view** — visual schedule per day with all 5 stages side by side
- **Browse view** — searchable card grid with global search across all days
- **Picks view** — your starred bands grouped by day, with automatic clash detection
- **Clash alerts** — overlapping sets are flagged with ⚡ everywhere they appear
- **Multi-user** — multiple names can save independent picks on the same device
- **Toast feedback** — visual confirmation when adding or removing bands
- **Accessible** — keyboard navigable, ARIA roles, focus trapping, screen-reader labels
- **Mobile friendly** — responsive layout from 480px up

## Usage

Open `index.html` in a browser, or visit the [live site](https://scollo-ricardo.github.io/gmm-clash-finder/).

No build step, no dependencies, no server — just static HTML/CSS/JS served via GitHub Pages.

## Project structure

```
├── index.html        # Markup and page shell
├── css/
│   └── style.css     # All styles
├── js/
│   └── app.js        # Data, state, rendering, event handling
├── LICENSE
└── README.md
```

## Data

The lineup data is hardcoded in `js/app.js`. If the schedule changes, edit the `RAW` object — each entry is `[start, end, "Band Name"]` per stage per day. Times past midnight use 24h+ notation (e.g. `"25:30"` = 1:30 AM).

## Storage

Picks are saved in `localStorage` under the key `gmm2026_picks`. Tabs in the same browser sync via `BroadcastChannel`. There is no backend — data lives entirely in your browser.

## License

See [LICENSE](LICENSE).