# Viewing Distance Lab: A Screen Size & Viewing Distance Calculator

An interactive tool for modeling the relationship between screen size, resolution, and viewing distance. Figure out whether your screen is "Retina" quality at your seating position, whether you'd benefit from 4K over 1080p, and how your viewing angle compares to cinema standards.

**[Try it live →](https://geoffsmithbk.github.io/screen-size-viewing-distance/)**

## What It Does

Adjust four inputs — **viewing distance**, **screen diagonal**, **horizontal resolution**, and **vertical resolution** — and instantly see:

| Output | What it tells you |
|--------|-------------------|
| **Pixel Density (PPI)** | How tightly packed pixels are on the screen |
| **Angular Density (pp°)** | How many pixels per degree of your vision — the key measure of perceived sharpness |
| **Pixel Visibility** | Whether you can see individual pixels at your distance (Apple's "Retina" threshold: 58 pp°) |
| **Min. Viewing Distance** | How close you can sit before pixels become visible |
| **4K Enhanced Viewing** | Whether you're close enough to actually benefit from 4K over 1080p |
| **Horizontal Angle of View** | Your viewing angle compared to SMPTE, THX, and IMAX standards |
| **Viewing Geometry Diagram** | A scaled side-view showing screen, viewing cone, and 4K benefit zone |

## Presets

Quick-select buttons for common setups:
- **Resolutions:** 720p, 1080p, 1440p, 4K UHD, 5K, 8K, plus ultrawides
- **Common screens:** 27" monitor, 32" 4K monitor, 55"–85" 4K TVs (with typical viewing distances)

## HAoV Reference Standards

The horizontal angle of view section shows how your setup compares to industry standards:

- **10°** — SMPTE NTSC recommendation
- **28°** — THX theatrical minimum (last row)
- **30°** — SMPTE HDTV recommendation
- **40°** — THX home theater optimal
- **60°** — IMAX theatrical minimum
- **68°** — Cinerama Dome best seats
- **120°** — IMAX theatrical maximum
- **140°** — Average maximum human horizontal field of view

## Usage

No installation needed. It's a single HTML file with no dependencies.

- **Online:** Visit the [live site](https://geoffsmithbk.github.io/screen-size-viewing-distance/)
- **Locally:** Open `index.html` in any browser, or serve it with `python3 -m http.server`

## License

MIT
