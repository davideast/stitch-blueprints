---
name: "The Darkroom"
slot: color-scheme
type: deterministic
mode: dark
tags: [dark-mode, cyan, photography, high-contrast]
---

## Color Roles

- **Primary** (`#EBEBEB`): Near-white — specified as text color for dark mode canvas
- **Secondary** (`#9E9E9E`): Medium gray — supporting structure
- **Tertiary** (`#00BCD4`): Vivid cyan — CTA and accent driver
- **Neutral** (`#121212`): Near-black — dark mode canvas

## Observed Token Output

| Token | Hex | Notes |
|---|---|---|
| `primary` | #e9feff | Near-white light anchor (dark mode inversion) |
| `primary-container` | #00f5ff | Vivid cyan — Tertiary input reinterpreted as primary |
| `tertiary` | (muted) | Cyan did not land in tertiary family |
| `background` | ~#121212 | Dark canvas confirmed |
| CTA token used in markup | `bg-primary-container` | #00f5ff vivid cyan |

## Notes

The LLM reinterpreted the vivid cyan Tertiary as the primary brand color and assigned it to `primary-container` rather than the tertiary family. When Primary is specified as near-white (a text/content color) and Tertiary is the most chromatic, Stitch's semantic engine may override the explicit role label and assign by chromatic dominance. This is an example of role swapping — the label was not honored.
