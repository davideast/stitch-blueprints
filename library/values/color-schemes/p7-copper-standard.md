---
name: "Copper Standard"
slot: color-scheme
type: deterministic
mode: light
tags: [copper, warm-gray, understated, material]
---

## Color Roles

- **Primary** (`#464646`): Dark charcoal — text, headings, icons
- **Secondary** (`#795548`): Copper brown — supporting accent (label intended this as Tertiary/CTA, but system assigned to secondary)
- **Tertiary** (`#795548`): Copper brown — specified as CTA; reassigned to secondary by system
- **Neutral** (`#F5F0EC`): Warm off-white — canvas

## Observed Token Output

| Token | Hex | Notes |
|---|---|---|
| `primary` | #464646 | Charcoal — matches panel primary |
| `primary-container` | #5e5d5d | Slightly lighter charcoal |
| `secondary` | #7a5649 | Copper landed here, not in tertiary |
| `secondary-container` | (warm) | |
| CTA token used in markup | `bg-primary` + `bg-secondary` | Split — no dedicated CTA token |

## Notes

This is an example of role swapping. The copper (#795548) was labeled as Tertiary (CTA driver) in DESIGN.md but the system interpreted it as a secondary support color based on its chromatic properties relative to the charcoal Primary. The LLM's semantic ordering (which color "should" be secondary vs tertiary) overrode the explicit label. Copper is a warm earth tone at moderate saturation — the system may treat earth tones as secondary/support rather than CTA-primary.
