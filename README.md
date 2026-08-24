# Red Rock OPS — Emergency Resources

Live emergency dashboards for the Red Rock OPS team.

**Currently active: [Hawk Fire — Reno Emergency Dashboard](https://redrockopsllc.github.io/emergency/)** (Aug 2026)

## What this repo is

A standing emergency repo. When something hits an area where we have people, the
dashboard at `index.html` gets pointed at that incident. It's a single static
HTML file — no build step, no dependencies — hosted on GitHub Pages.

The page has two layers:

1. **Live panels** — pulled client-side every 5 minutes, no API keys:
   - Active NWS alerts for the Reno point (`api.weather.gov`)
   - US AQI + PM2.5/PM10 (Open-Meteo air quality API)
   - Wind speed/gusts/direction, temp, humidity (Open-Meteo forecast API)
2. **Curated links & facts** — official evacuation map (Perimeter), shelters,
   roads/power, news, checklists. These are verified manually and stamped with a
   date. **Shelter statuses and fire stats age fast — re-verify and re-stamp when
   editing.**

## How to update

1. Edit `index.html` (all CSS/JS is inline).
2. Commit to `main` and push. GitHub Pages redeploys automatically in ~1 minute.
3. Update the "last verified" date in the situation note and shelter section.

## For the next incident

- Copy the current `index.html` into an archive folder (e.g. `hawk-fire-2026/`)
  before repurposing the root page.
- Change `RENO.lat/lon` in the script block to re-aim the live panels.
- Swap the curated links for the new incident's official sources.

## TODO (Angel)

- [ ] Fill in the company contact placeholders in the "Red Rock OPS team
      check-in" card (HR phone/email, emergency policy line).

## Sources verified 2026-08-24

Perimeter (perimetermap.com), EmergencyWashoe.com, Washoe County Regional
Alerts, KOLO 8 resource list, KUNR live blog, NWS Reno. Always follow local
emergency officials over anything in this repo.
