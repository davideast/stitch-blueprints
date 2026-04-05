---
name: "Atlantic"
entity: color-scheme
slot: color-scheme
type: deterministic
mode: light
tags: [navy, maritime, gold, nautical, institutional, preppy, heritage, tonal]
reference: Naval heritage, Ivy League institutions, nautical charts, classic American preppy, maritime museums
prompt: >-
  Primary #1A2744 deep navy for all text and headings. Secondary #3D5A80 slate blue for
  borders, captions, metadata. Tertiary #D9AE5E vivid gold for CTAs and interactive elements.
  Neutral #E0E1DD cool silver-gray canvas. Tonal blue progression from dark navy through
  slate to silver with a single warm gold accent.
---

## Color Roles

- **Primary** (`#1A2744`): Deep navy — HSL(221°, 45%, 18%). All text, headings, core content. Near-dark with strong blue hue — reads as near-black with character rather than neutral charcoal.
- **Secondary** (`#3D5A80`): Slate blue — HSL(214°, 35%, 37%). Supporting structure, borders, captions, metadata. Bridges the dark navy and the light canvas through tonal blue progression.
- **Tertiary** (`#D9AE5E`): Vivid gold — HSL(39°, 62%, 61%). CTA fills, interactive elements, the warm accent. Nudged from original `#C9A86C` (S=46%) to S=62% for reliable Tertiary token landing.
- **Neutral** (`#E0E1DD`): Cool silver-gray — HSL(75°, 6%, 87%). The canvas. Nearly achromatic with a faint warm undertone — references institutional paper, naval chart stock.

## The Dropped Color

`#98C1D9` — powder blue at HSL(202°, 46%, 72%) — does not fit cleanly into any of the 4 roles. Too light for Primary or Secondary, too muted and light for Tertiary, too blue for Neutral. It may emerge naturally from Stitch's tonal derivation of the blue Secondary family (as a `secondary-container` or `surface-tint` value). Worth checking in the generated Tailwind config.

## Nudge Note

Original gold `#C9A86C` sat at HSL(39°, 46%, 61%) — S=46% is 14 points below the S≥60% threshold. Nudged to `#D9AE5E` at HSL(39°, 62%, 61%) — same hue and lightness, saturation brought above threshold. The visual difference is subtle; the character of the gold is preserved.

## Notes

A tonal blue progression with a single warm gold accent. The palette reads as heritage institutional — serious, measured, earned. Favors the tonal layering elevation system.
