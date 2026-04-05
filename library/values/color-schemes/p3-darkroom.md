---
name: "The Darkroom"
entity: color-scheme
slot: color-scheme
type: deterministic
mode: dark
tags: [dark-mode, cyan, photography, high-contrast]
prompt: >-
  Primary #EBEBEB near-white for text on dark canvas. Secondary #9E9E9E medium gray for
  supporting structure. Tertiary #00BCD4 vivid cyan for CTA accent. Neutral #121212
  near-black dark mode canvas. Note: vivid cyan may route to primary-container rather
  than tertiary family due to chromatic dominance reinterpretation.
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

The LLM reinterpreted vivid cyan Tertiary as the primary brand color and assigned it to `primary-container` rather than the tertiary family. When Primary is near-white and Tertiary is the most chromatic, Stitch may override the role label and assign by chromatic dominance. Example of role swapping.
