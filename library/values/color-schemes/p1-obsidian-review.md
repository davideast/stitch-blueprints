---
name: "Obsidian Review"
slot: color-scheme
type: deterministic
mode: light
tags: [dark-primary, crimson, dramatic, monochromatic-base]
---

## Color Roles

- **Primary** (`#1A1A2E`): Near-black navy — text, headings, icons
- **Secondary** (`#2D2D44`): Dark muted navy — supporting text, borders
- **Tertiary** (`#C0392B`): Vivid crimson — CTA and accent driver
- **Neutral** (`#F5F5F0`): Warm off-white — canvas

## Observed Token Output

| Token | Hex | Notes |
|---|---|---|
| `primary` | #040000 | Near-black derivation |
| `primary-container` | #420000 | Dark red — unexpected; crimson influenced primary family |
| `tertiary` | #695d3c | Muted olive — vivid crimson did not land here |
| `surface-tint` | #b02d21 | Vivid crimson landed here |
| `background` | ~#F5F5F0 | |
| CTA token used in markup | `bg-surface-tint` | Crimson (#b02d21) — new token, previously untracked |

## Notes

The crimson Tertiary did not land in `tertiary` or `tertiary-container` as expected. Both Primary (#1A1A2E) and Tertiary (#C0392B) are dark-toned in HCT perceptual space, causing the vivid color to route to `surface-tint` instead. This is an anomalous case — the vivid Tertiary should be HSL L 40–65% to land predictably.
