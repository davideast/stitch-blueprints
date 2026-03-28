---
name: "Professional"
slot: components.buttons
type: influence
tags: [ring, clean, pill, no-icons, professional, tailwind]
---

Buttons use these rules without exception:

**Shape:** Pill-shaped — fully rounded corners. Height 36–38px controlled via padding, never a fixed height value. Font size 14px (text-sm).

**Border treatment:** No solid borders. When a button sits alongside a shadow, use an outer `ring` at gray-950 / 10% opacity placed outside the element. A solid border combined with a shadow creates a muddy transition at the edge — the ring eliminates this.

**Content:** No icons inside buttons. Remove any icon the generator presets. The label alone is sufficient.

**Two-button alignment:** When one button has an outer ring and an adjacent button does not, the ringed button will appear 2px taller. Fix by wrapping the ringed button in a `span` set to `inline-flex p-px`, then using `calc` to compensate the height difference. Both buttons must appear visually identical in height.
