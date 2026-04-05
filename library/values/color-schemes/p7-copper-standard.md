---
name: "Copper Standard"
entity: color-scheme
slot: color-scheme
type: deterministic
mode: light
tags: [copper, warm-gray, understated, material]
prompt: >-
  Primary #464646 dark charcoal for text and headings. Secondary #795548 copper brown for
  supporting accent. Tertiary #795548 copper brown specified as CTA but system reassigned
  to secondary. Neutral #F5F0EC warm off-white canvas. Note: copper earth tone was role-swapped
  by system from Tertiary to Secondary based on chromatic properties.
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

Example of role swapping. Copper (#795548) was labeled as Tertiary (CTA driver) but the system interpreted it as secondary support based on chromatic properties. Earth tones at moderate saturation may be treated as secondary/support rather than CTA-primary.
