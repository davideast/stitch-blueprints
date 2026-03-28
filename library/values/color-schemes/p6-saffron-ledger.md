---
name: "Saffron Ledger"
slot: color-scheme
type: deterministic
mode: light
tags: [orange, warm, editorial, financial]
---

## Color Roles

- **Primary** (`#E67E22`): Vivid saffron orange — dominant brand color
- **Secondary** (`#C7C6C6`): Light gray — supporting structure
- **Tertiary** (`#00A3E4`): Vivid sky blue — accent
- **Neutral** (`#FAFAFA`): Near-white — canvas

## Observed Token Output

| Token | Hex | Notes |
|---|---|---|
| `primary` | #ffb783 | Light peach — tonal derivation (lighter than panel input) |
| `primary-container` | #e67e22 | Exact match to Panel Primary |
| `tertiary` | #86cfff | Light sky blue |
| `tertiary-container` | #00a3e4 | Vivid blue |
| `secondary` | #c7c6c6 | |
| `secondary-container` | #464747 | Dark gray |
| CTA token used in markup | `saffron-gradient` (custom) | Gradient from #ffb783 → #e67e22 (primary → primary-container) |

## Notes

The markup generator invented a custom CSS class (`saffron-gradient`) rather than using a named Tailwind token. This is the only observed instance of a custom gradient class across all experiments. The gradient blends `primary` and `primary-container`, producing a vivid warm CTA. This behavior may be triggered when the primary color is highly saturated and warm — the generator prefers the gradient for visual richness.
