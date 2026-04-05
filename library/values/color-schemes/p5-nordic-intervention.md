---
name: "Nordic Intervention"
entity: color-scheme
slot: color-scheme
type: deterministic
mode: light
tags: [navy, minimal, nordic, cool-toned]
prompt: >-
  Primary #2E59A7 medium navy blue for text and headings. Secondary #50606F cool slate for
  supporting structure. Tertiary #8D4A00 dark burnt orange accent — muted, produced muted
  CTA. Neutral #F4F6F8 cool off-white canvas. Note: generator used bg-primary for CTAs
  rather than tertiary. For vivid CTA, replace Tertiary with a higher-saturation mid-lightness value.
---

## Color Roles

- **Primary** (`#2E59A7`): Medium navy blue — text, headings, icons
- **Secondary** (`#50606F`): Cool slate — supporting structure
- **Tertiary** (`#8D4A00`): Dark burnt orange — accent (muted, resulted in muted CTA)
- **Neutral** (`#F4F6F8`): Cool off-white — canvas

## Observed Token Output

| Token | Hex | Notes |
|---|---|---|
| `primary` | #0a418e | Darker navy derivation |
| `primary-container` | #2e59a7 | Exact match to Panel Primary |
| `tertiary` | #6a3600 | Dark burnt orange |
| `tertiary-container` | #8d4a00 | |
| `secondary` | #50606f | |
| `secondary-container` | #d1e1f4 | Light periwinkle |
| `surface-tint` | #325caa | |
| CTA token used in markup | `bg-primary` | #0a418e dark navy — muted CTA |

## Notes

The generator used `bg-primary` (dark navy) rather than a tertiary token for CTAs. The muted tertiary family was de-prioritized. For a vivid Nordic CTA, replace Tertiary with a higher-saturation, mid-lightness value (e.g. vivid teal or amber at HSL L 45–60%).
