# funkygene-art
# Funky Gene Live — Firetrails Broadcast Graphics

Browser-based graphics for Dick Collins Firetrails and the Bay Area 100 Series. The graphics are designed for a 1920×1080 OBS Browser Source or vMix Web Browser input and use transparent page backgrounds.

## Animated graphics

- `funky_gene_cut_transition.html` — full-screen branded camera-cut transition with an original contour/trail pattern.
- `funky_gene_lower_third.html` — reusable animated lower third.
- `live_race_results.html` — rotating Top 10 men’s and women’s race results.
- `funky_gene_broadcast_ticker.html` — continuous bottom-of-screen results ticker.
- `funky_gene_runner_crossing.html` — runner timing-point alert.
- `funky_gene_top5_leaders.html` and `funky_gene_top10_leaderboard.html` — leaderboards.

## Quick URLs

After the branch is merged and GitHub Pages updates:

- `https://funkygene.art/funky_gene_cut_transition.html`
- `https://funkygene.art/funky_gene_lower_third.html`
- `https://funkygene.art/live_race_results.html`

Use `?loop=1` while previewing the cut transition. Remove it for live use so the transition plays once whenever the browser source reloads.

Example customized lower third:

```text
https://funkygene.art/funky_gene_lower_third.html?name=EUGENE%20RODRIGUEZ&detail=BROADCAST%20DIRECTOR%20%E2%80%A2%20FUNKY%20GENE%20LIVE&bib=100&badgeLabel=ROLE&badgeValue=PRODUCER&hold=8000
```

Supported lower-third parameters are `name`, `detail`, `eyebrow`, `bib`, `signal`, `badgeLabel`, `badgeValue`, and `hold`. A `hold` value of `0` keeps the graphic visible; a positive value hides it after that many milliseconds.

Example results board with a 12-second rotation:

```text
https://funkygene.art/live_race_results.html?interval=12000
```

## Live-production setup

1. Add the page as a 1920×1080 Browser Source in OBS or Web Browser input in vMix.
2. Keep the page background transparent.
3. For the cut transition, enable refresh/reload when the source becomes active. The default animation is 1.55 seconds and the frame is fully covered around 0.65 seconds after it starts.
4. Switch cameras while the patterned screen fully covers the picture.
5. Use `funky_gene_data_bridge.js` to change the results page from test mode to the approved RaceResult JSON endpoint.

All sample runner names and times are marked as test data. The Firetrails logo remains red/black, and the Bay Area 100 Series logo uses its preserved sage-and-cream artwork.
