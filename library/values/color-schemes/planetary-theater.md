---
name: "Planetary Theater"
entity: color-scheme
slot: color-scheme
type: deterministic
mode: dark
tags: [dark-mode, cyan, navy, amber, void, astronomical, cinematic, chiaroscuro, planetary]
---

## Color Roles

- **Neutral** (`#050505`): Void black — HSL(0°, 0%, 2%). Near-absolute black, essentially achromatic. The infinite, crushing vacuum. Takes up massive visual real estate so lighter colors glow with theatrical intensity.
- **Primary** (`#6CD3DF`): Luminous cyan — HSL(186°, 64%, 65%). The primary energetic light source. Communicates the ethereal, freezing nature of deep-space phenomena — icy ring composition, atmospheric light scatter. High saturation (S=64%), mid-high lightness (L=65%).
- **Secondary** (`#0A2342`): Deep navy — HSL(213°, 74%, 15%). The atmospheric medium. Communicates volume, mass, and pressurized atmosphere between the bright cyan and the void. Gives planetary bodies three-dimensional weight.
- **Tertiary** (`#C78B50`): Glowing amber — HSL(30°, 52%, 55%). The critical tension. A thin streak of warmth in an otherwise freezing palette — distant stellar reflection, illuminated cosmic dust. Prevents the palette from reading as sterile or artificial.

## Role Mapping Warning

**Primary** (`#6CD3DF`) is an unconventional mapping. Stitch's token model expects Primary to be near-black (light mode) or near-white (dark mode) for core text. Luminous cyan at HSL(186°, 64%, 65%) is neither — it is a vivid chromatic light color. Expect cyan-derived text, headings, and content tokens against the void canvas. The generated design will have glowing cyan typography rather than neutral white text.

## Tertiary Warning

**Tertiary** (`#C78B50`) sits at HSL(30°, 52%, 55%) — S=52% is below the S≥60% threshold. The amber accent will likely produce a muted token family. The amber character is preserved but the CTA may appear less vivid than intended. To ensure reliable landing, nudge to HSL(30°, 62%, 52%): approximately `#CA8A3F`.

## Observed Token Output

> Not yet observed — generate and extract Tailwind config.

## Notes

This palette intentionally inverts the standard Stitch color hierarchy. The "Primary" role carries chromatic energy rather than neutral legibility — the entire aesthetic depends on glowing cyan against void black. This is not a standard light-on-dark or dark-on-light scheme; it is a luminance-from-source scheme where the canvas is absolute and the content glows.
