---
name: "Midnight Cartography"
entity: color-scheme
slot: color-scheme
type: deterministic
mode: light
tags: [dark-navy, amber, editorial, cartographic]
prompt: >-
  Primary #2C3E6B deep navy for text and headings. Secondary #505F7C muted slate blue for
  supporting structure. Tertiary #735C00 dark amber/gold for accent — note this is muted
  and produces a dark CTA. Neutral #F8F6F0 warm parchment canvas. For a vivid gold CTA,
  replace Tertiary with ~#B8860B.
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

Tertiary was specified as a muted dark amber rather than a vivid mid-lightness hex. The CTA is dark and low-contrast against light backgrounds. To get a vivid gold CTA, the Tertiary input should be closer to #B8860B (HSL ~43°, S 62%, L 38%) or lighter.
