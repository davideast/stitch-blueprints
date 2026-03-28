---
name: "Nordic Intervention"
slot: color-scheme
type: deterministic
mode: light
tags: [navy, minimal, nordic, cool-toned]
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

The markup generator used `bg-primary` (dark navy) rather than a tertiary token for CTAs. This suggests the generator de-prioritized the muted tertiary family and fell back to the primary family for calls-to-action. For a vivid Nordic CTA, replace the Tertiary with a higher-saturation, mid-lightness value (e.g. a vivid teal or amber at HSL L 45–60%).
