# Screen Size & Viewing Distance Calculator

## Project Overview
Single-page interactive web app that models screen size, resolution, and viewing distance relationships. Based on a Google Sheets calculator, rebuilt as a zero-dependency HTML/JS app for GitHub Pages.

- **Live site:** https://geoffsmithbk.github.io/screen-size-viewing-distance/
- **Source spreadsheet:** https://docs.google.com/spreadsheets/d/1cSGM3vnrOeIMzNHTpL94-_5BJfUBF8_K-GG0ejWuUWM/

## Architecture
- Single `index.html` file — all HTML, CSS, and JS inline
- No build step, no dependencies, no frameworks
- Designed for GitHub Pages static hosting

## Key Formulas
All calculations derive from four inputs: viewing distance, screen diagonal, horizontal resolution, vertical resolution.

- **Screen dimensions:** width = diagonal × cos(arctan(vres/hres)), height = diagonal × sin(arctan(vres/hres))
- **PPI:** horizontal_resolution / screen_width
- **Angular density (pp°):** PPI × viewing_distance × (π/180)
- **Pixel visibility:** angular density < 58 pp° means pixels are visible (Apple "Retina" threshold)
- **Min viewing distance:** 3438 / PPI (based on 1 arcminute = 60 pp° at 20/20 vision)
- **HAoV:** 2 × arctan(screen_width / (2 × viewing_distance))
- **4K benefit window:** between pixel visibility threshold for current resolution and for half resolution (e.g., 1080p)

## Reference Standards (HAoV)
- 10° SMPTE NTSC, 28° THX theatrical min, 30° SMPTE HDTV, 40° THX home optimal
- 60° IMAX theatrical min, 68° Cinerama Dome best seats, 120° IMAX max, 140° human max

## Development Notes
- Test locally: `python3 -m http.server 8769` then open `http://localhost:8769/index.html`
- The spreadsheet showed 60° HAoV for the default values; mathematically correct result is 55.4° for a 47.5" screen at 39.4" — the spreadsheet may have had different values at time of export
