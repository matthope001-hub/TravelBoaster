# 🚗 TravelBoaster Ontario

**Create animated 3D travel videos of Ontario road trips — right in your browser.**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-blue?style=for-the-badge)](https://matthope001-hub.github.io/TravelBoaster/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

---

## What Is It?

TravelBoaster lets you pick any two Ontario cities, choose a vehicle, and watch a 3D animation of your road trip — then record it as a shareable video. Inspired by the TravelBoast mobile app.

![TravelBoaster Screenshot](screenshot.png)

---

## Features

- 🗺️ **Real road routing** via OpenStreetMap (OSRM) — follows actual highways like the QEW, 401, and 403
- 🚗 **8 detailed 3D vehicles** with realistic suspension bounce, turn banking, and dust particles
- 🎬 **6 camera modes** — Chase, Cinematic Orbit, Overhead, Side Profile, Dashboard, Hood
- 🏙️ **Ontario map tiles** from CartoDB Voyager, dynamically zoomed to your route
- 📹 **Video recording** with 3-second countdown and WebM export
- ⚡ **Speed control** from 0.1× crawl to 3× fast-forward
- 📍 **Preset routes** for popular Ontario trips

---

## Vehicles

| Vehicle | Color | Type |
|---|---|---|
| Toyota Camry | Silver | Sedan |
| Honda CR-V | Dark Blue | SUV |
| RAM 1500 | Red | Pickup |
| BMW M4 | Red | Sports |
| Chrysler Pacifica | Purple | Minivan |
| Tesla Model 3 | White | EV |
| Jeep Wrangler | Lime Green | Off-road |
| Harley Davidson | Orange | Motorcycle |

---

## Preset Routes

- Toronto → Hamilton (QEW / Gardiner)
- Toronto → Niagara Falls (QEW)
- Toronto → London (401 / 403)
- Toronto → Kingston (401 East)
- Mississauga → Oakville
- Brampton → Guelph

Or enter any Ontario city in the custom route field.

---

## How to Use

1. Open the [live demo](https://matthope001-hub.github.io/TravelBoaster/)
2. Click **☰** to open the panel
3. Select a preset route or type your own cities
4. Click **Calculate Route**
5. Pick a vehicle and camera mode
6. Hit **▶ Start Drive**
7. Optionally click **● Record Video** to export a WebM file

---

## Tech Stack

| Library | Purpose |
|---|---|
| [Three.js r128](https://threejs.org/) | 3D rendering |
| [OSRM API](http://project-osrm.org/) | Real road routing |
| [Nominatim](https://nominatim.org/) | City geocoding |
| [CartoDB Voyager](https://carto.com/basemaps/) | Map tiles |
| MediaRecorder API | Video export |

No build tools, no backend, no API keys required. Single HTML file.

---

## Running Locally

```bash
git clone https://github.com/matthope001-hub/TravelBoaster.git
cd TravelBoaster
# Open index.html in any modern browser
open index.html
```

> **Note:** Some map tiles may not load when opened directly from the filesystem due to browser CORS restrictions. Use a local server for best results:
> ```bash
> npx serve .
> # or
> python -m http.server 8080
> ```

---

## Deploying to GitHub Pages

1. Push `index.html` to the `main` branch
2. Go to **Settings → Pages**
3. Set Source to **Deploy from branch → main → / (root)**
4. Your app will be live at `https://matthope001-hub.github.io/TravelBoaster/`

---

## Roadmap

- [ ] Waypoints (multi-stop routes)
- [ ] Route alternatives (pick fastest vs. scenic)
- [ ] Night mode with glowing headlights
- [ ] Engine & road sound effects
- [ ] Points of interest along route (CN Tower, Niagara, etc.)
- [ ] Speed HUD overlay on recordings
- [ ] Saved routes via localStorage
- [ ] Mobile touch support

---

## Known Limitations

- Map tiles require network access — offline use shows a green fallback ground
- Video export is WebM format (not supported in Safari)
- Routing quality depends on OpenStreetMap data accuracy
- Not yet optimized for mobile/touchscreen

---

## License

MIT — free to use, modify, and share.

---

*Built with Three.js and a love for Ontario road trips.*
