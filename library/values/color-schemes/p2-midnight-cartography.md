---
name: "Midnight Cartography"
slot: color-scheme
type: deterministic
mode: light
tags: [dark-navy, amber, editorial, cartographic]
---

## Color Roles

- **Primary** (`#2C3E6B`): Deep navy — text, headings, icons
- **Secondary** (`#505F7C`): Muted slate blue — supporting structure
- **Tertiary** (`#735C00`): Dark amber/gold — accent (muted, not vivid — resulted in muted CTA)
- **Neutral** (`#F8F6F0`): Warm parchment — canvas

## Observed Token Output

| Token | Hex | Notes |
|---|---|---|
| `primary` | #142854 | Darker navy derivation |
| `primary-container` | #2c3e6b | Exact match to Panel Primary |
| `tertiary` | #735c00 | Dark amber — the panel input itself |
| `tertiary-container` | #cfa702 | More vivid gold |
| `secondary` | #505f7c | |
| `secondary-container` | #cbdafd | Light periwinkle |
| CTA token used in markup | `bg-tertiary` | #735c00 — dark amber, not highly vivid |

## Notes

Tertiary was specified as a muted dark amber rather than a vivid mid-lightness hex. The CTA (`bg-tertiary`) is dark and low-contrast against light backgrounds. To get a vivid gold CTA, the Tertiary input should be closer to #B8860B (HSL ~43°, S 62%, L 38%) or lighter.
