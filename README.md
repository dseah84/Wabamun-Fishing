# Wabamun Fishing Weather

A single-page, Windy-style forecast map for Wabamun Lake, built on Environment
and Climate Change Canada's **HRDPS** model (High Resolution Deterministic
Prediction System: 2.5 km grid, 48-hour horizon, four runs a day).

Open `index.html` in any browser. No build step and no API key.

## What it shows

- Animated wind flow over the lake, plus colour layers for wind, gusts,
  temperature, rain and cloud.
- A time slider and play button across the HRDPS run.
- A fishing outlook score (0-100) for each hour at *your spot* (tap the map to
  move it; it is remembered). Every point added or taken off is listed under
  "Why this score", so you can judge it yourself.
- The shore the wind is blowing onto, the best upcoming windows, sunrise and
  sunset, moon phase and solunar periods.
- A small-boat warning when gusts reach 45 km/h.

## Data

The HRDPS values come from Open-Meteo's GEM endpoint
(`models=gem_hrdps_continental`), sampled on a 9 x 7 grid (about 4 km apart)
covering the lake. One request per load; the page refreshes every 30 minutes
and keeps the last good forecast in the browser for use with no signal.

The score is a rule of thumb (wind chop, pressure trend, low light, cloud,
solunar, rain), not a prediction of catches.
