---
name: "Humanist Sans"
slot: typography.body
type: influence
tags: [readable, neutral, professional, long-form, accessible]
---

Body text uses a humanist sans-serif — warm, legible, and unpretentious. Optimized for reading at 14–16px. Regular weight for prose, medium for emphasis. Line height is generous (1.6–1.75) to support sustained reading. The type feels like it was designed for humans, not for screens.

At 14px (text-sm), line height can be set to 28px — double the font size. Sounds extreme but gives subheadings and explanatory text significant breathing room.

Constrain text block width with character units: `max-w-[40ch]` is a reliable starting point (tune between 35–45ch). Reading comfort scales with font size; ch units maintain that relationship where pixel values don't.

Use `text-pretty` to prevent orphan words at paragraph ends. Use `text-balance` to distribute line lengths more evenly across multiple lines. They produce different effects — choose per block rather than defaulting to one.
