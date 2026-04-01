# AoM Retold Icons Aura Generator

A standalone web app for generating Age of Mythology Retold–style aura icons from transparent-background PNGs.  
No installation or build step required — open `IconsAuraGenerator.html` directly in any modern browser.

---

## Features

- **4 style presets** — Hero (gold), Myth (emerald), Legend (sapphire), Villain (ruby)
- **Dynamic UI theming** — the interface accent colours match the active preset
- **Live preview** — output re-renders automatically as you adjust sliders (800 ms debounce)
- **Drag & resize** — position and scale the unit inside the square viewport interactively
- **Zoom & offset sliders** — precise placement with Zoom (10–200 %), X Offset and Y Offset controls
- **Glow controls** — Spread, Intensity, Rim Sharpness
- **Ambient background** — radial coloured background glow with Strength and Radius controls
- **Color controls** — Hue (0–200°) and Saturation (40–100 %) sliders
- **Reset button** — restores all parameters to defaults for the active preset
- **Three download sizes** — 512 px, 256 px, 128 px PNG

---

## How to Use

1. Open `Tools/IconsAuraGenerator.html` in your browser.
2. Drop a PNG with a transparent background onto the **Input & Preview** panel, or click to browse.
3. Choose a **preset** (Hero / Myth / Legend / Villain) from the Parameters panel.
4. Adjust placement and effect sliders as needed; the Output panel updates automatically.
5. Click **↓ 512 px**, **↓ 256 px**, or **↓ 128 px** to download the result.

Output filenames follow the pattern: `<input_name>_<preset>_icon_<size>.png`  
*(e.g. `griffin_myth_icon_256.png`)*

---

## Algorithm

1. Black background fill
2. Radial ambient glow centred slightly above-centre
3. Six additive blur passes over the unit silhouette (colourised to the preset hue)
4. Original unit image composited on top

Calibrated against AoM Retold 4K myth unit icons across 6 civilisations.

---

## Dependencies

- [Interact.js 1.10.27](https://interactjs.io/) — loaded from CDN for drag and resize

---

## File Location

```
Tools/
  EmeraldAuraGenerator.html   ← the app
  README.md                   ← this file
```
