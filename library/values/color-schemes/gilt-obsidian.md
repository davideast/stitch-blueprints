---
name: "Gilt Obsidian"
slot: color-scheme
type: deterministic
mode: light
tags: [black, gold, crimson, cream, esoteric, tarot, apothecary, luxury, analog]
reference: Classic luxury print, tarot card decks, premium apothecary packaging, gold-foil letterpress
---

## Color Roles

- **Primary** (`#0A0A0A`): Near-absolute black — HSL(0°, 0%, 4%). All text, headings, the central arch container. Achromatic — takes on warmth from the cream canvas around it.
- **Secondary** (`#CC0033`): Vivid crimson — HSL(345°, 100%, 40%). Accent fills, secondary surfaces. See note below on the 5-color problem.
- **Tertiary** (`#D4AF37`): Classic gold / antique brass — HSL(46°, 65%, 52%). CTA fills, interactive elements, the gold circle motif. S=65%, L=52% — clean valid Tertiary.
- **Neutral** (`#F5E6D3`): Warm peach cream — HSL(34°, 63%, 89%). The canvas. More character and warmth than the near-white alternative.

## The 5-Color Problem

This palette has 5 colors but Stitch's model has 4 roles. The fifth color, `#FFF8F0` (HSL 32°, 100%, 97%), is a near-white warm cream — a lighter alternative canvas to `#F5E6D3`. Two options:

**Option A (recommended):** Use `#F5E6D3` as Neutral (canvas) and drop `#FFF8F0`. Richer, more distinctive canvas.

**Option B:** Use `#FFF8F0` as Neutral and `#F5E6D3` as Secondary — two cream tones creating a tonal layering effect between canvas and surface containers. Crimson then falls outside the 4-role model entirely and is used only as a custom CSS accent (offset shadows, focus rings) — which matches the neo-esoteric design intent anyway.

## Secondary Mapping Warning

`#CC0033` (crimson) as Secondary is semantically awkward. Stitch will derive supporting UI — borders, captions, metadata text — from the Secondary family. Vivid crimson at L40% in those roles will produce loud supporting elements. Option B (dropping crimson from the role model and using it as a custom accent) is more faithful to the design intent, where crimson appears only as a 1px offset shadow or focus state — never as a surface or supporting text color.

## Observed Token Output

> Not yet observed — generate and extract Tailwind config.

## Notes

The defining duo is the near-black Primary and the gold Tertiary. The crimson is the surprise — used sparingly, it reads as esoteric and handcrafted. Used broadly (as a token-derived Secondary), it becomes aggressive. Treat it as a decoration color outside the token system.
