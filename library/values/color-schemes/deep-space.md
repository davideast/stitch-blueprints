---
name: "Deep Space"
entity: color-scheme
slot: color-scheme
type: deterministic
mode: dark
tags: [dark-mode, astronomical, electric-blue, near-white, precision, cool, scientific]
reference: Astronomical instruments, telescope interfaces, space agency dashboards, deep-sky imaging platforms
---

## Color Roles

- **Primary** (`#E8EBF4`): Near-white starlight — HSL(225°, 27%, 93%). All text, labels, instrument readouts. Cool white with a faint blue cast — references starlight, not warm lamp light.
- **Secondary** (`#4A5568`): Atmospheric slate — HSL(220°, 16%, 35%). Mid-depth elements, structural frames, grid lines. The atmospheric layer between foreground and void.
- **Tertiary** (`#2563EB`): Vivid electric blue — HSL(221°, 83%, 53%). The instrument indicator light: CTAs, active states, data highlights. S=83%, L=53% — strongly valid Tertiary.
- **Neutral** (`#050810`): Deep space black — HSL(225°, 50%, 4%). The void. Near-absolute black with a blue-black cast — references the sky the telescope points into.

## Observed Token Output

> Not yet observed — generate and extract Tailwind config.

## Notes

Dark mode scheme with light Primary (near-white text on dark canvas) — the inverse of the standard near-black Primary model. The near-white Primary and near-black Neutral produce maximum luminance contrast. The electric blue Tertiary at L53% is well within the valid range and will land cleanly in the tertiary base token. No warmth anywhere in this palette — entirely cool and astronomical.
