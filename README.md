# Australia's Regional Tourism Renaissance — FIT3179 DV2

This repository contains a small, single‑page web visualisation that explores domestic daytrip tourism in Australia (2019–2025). The site uses official Tourism Research Australia data and GeoJSON boundaries to show geographic distribution, temporal trends, composition, and indexed recovery across all states and territories.

---

## Quick start

- Clone or download the repository and open the project folder.
- Serve locally (recommended):

```powershell
cd bushfire-viz
python -m http.server 8000
# then open http://localhost:8000
```

- Or use VS Code Live Server: right‑click `index.html` → Open with Live Server.

---

## Project structure (important files)

```
bushfire-viz/
├─ index.html                 # Main page (embeds Vega-Lite specs)
├─ README.md                  # This file
├─ MOODLE_SUBMISSION.md       # 500-word assignment description
├─ js/
│  ├─ tourism_map.vg.json     # Choropleth map (aggregates CSV)
│  ├─ tourism_trends_line.vg.json
│  ├─ tourism_stacked_bar.vg.json
│  └─ tourism_recovery.vg.json
└─ data/
   ├─ tourism_daytrips.csv    # Primary numeric data (8 states × 7 years)
   ├─ tourism_growth_index.csv # Indexed recovery values (2019=100)
   └─ states.geojson          # State/territory boundaries
```

---

## Data sources

- Tourism Research Australia — Domestic tourism statistics (daytrip trips, 2019–2025). Data were converted into `tourism_daytrips.csv` for the site.
- GeoJSON boundaries: rowanhogan/australian-states (public GitHub).

All data files used in the visualisations are included in `data/`. Values quoted on the site (for example NT growth +77.4% from 551.309k in 2019 to 978.1865k in 2025) are computed directly from `tourism_daytrips.csv`.

---

## Visualisations (what you'll see)

- Choropleth map — total daytrip visits summed across 2019–2025 per state (geographic overview).
- Multi‑line trends — annual time series per state (temporal trajectories and pandemic recovery).
- Stacked bar — yearly part‑to‑whole composition (how state shares change over time).
- Indexed recovery — all states normalised to 2019 = 100 for fair proportional comparison.

Interactive features: tooltips for exact values and legend filtering for focus.

---

## Deploying to GitHub Pages

1. Create a GitHub repository and push this folder.
2. In GitHub settings → Pages, set source to `main` branch (root).
3. Your site will be available at `https://<username>.github.io/<repo>/` shortly.

Tip: ensure all data and JSON files are committed and use relative paths like `data/...` and `js/...` so the site works on Pages.

---

## License & contact

This project is educational work for FIT3179. Feel free to reuse components with attribution. For questions or corrections, contact: Tharushi Tharunya Tennakoon (student ID 34715274).

---

Enjoy — and good luck with submission! If you want I can create a short `deploy` script or `package.json` with `gh-pages` configured.

## 🌐 Data Attribution

**Data Source:** Bureau of Meteorology (BOM)  
**Copyright:** © Commonwealth of Australia  
**License:** Creative Commons (public data)  
**URL:** http://www.bom.gov.au/climate/data/

All data is publicly available and used in accordance with BOM's data policy.

**Created:** October 2025  
**Course:** FIT3179 Data Visualisation 2, Monash University  
**Topic:** Australian Climate Patterns (Temperature & Rainfall 2019-2024)  
**Data:** Real Bureau of Meteorology official records
