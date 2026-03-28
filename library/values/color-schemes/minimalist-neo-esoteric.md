---
name: "Minimalist Neo-Esoteric"
slot: color-scheme
type: deterministic
mode: light
tags: [esoteric, tarot, apothecary, craft, charcoal, gold, crimson, cream]
reference: Modern tarot card decks, high-end apothecary labels
---

## Color Roles

- **Primary** (`#1A1818`): Rich charcoal / soft black — all text, branding, and the central arch container. Monumental without the harshness of pure black.
- **Secondary** (`#C8A963`): Matte brass / muted gold — content text inside dark containers, interactive elements, the geometric circle motif. Warmth and premium weight.
- **Tertiary** (`#9F2B2A`): Deep crimson / brick — used exclusively as micro-accent. Offset drop-shadows, focus states, geometric edge accents. Never fills a button or large area.
- **Neutral** (`#EBEAE5`): Warm alabaster / cream — the canvas. Unbleached paper feel. Prevents the charcoal from reading as clinical or digital.

## HSL Warning

Tertiary `#9F2B2A` sits at approximately HSL(1°, 58%, 39%) — just below the recommended S ≥ 60% and L ≥ 40% thresholds. This may produce a muted tertiary token family in Stitch's derivation. This is acceptable for this palette because the crimson is intentionally not a CTA color — it is a micro-accent only. Expect Stitch's CTA markup to fall back to the primary (charcoal) family, which is correct for this design: the gold circle button should be implemented as a custom element, not a standard CTA token.

## Observed Token Output

> Not yet observed — generate and extract Tailwind config.

## Notes

This palette inverts the standard luminance CTA model. The Secondary (gold) drives the interactive circle button, not the Tertiary. The Tertiary is purely atmospheric — a 1px crimson offset shadow or focus ring. The neutral cream canvas is the most important decision: it makes the charcoal arch read as a physical artifact rather than a UI element.
