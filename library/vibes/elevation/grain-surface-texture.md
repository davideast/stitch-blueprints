---
name: "Grain Surface Texture"
entity: vibe
slot: elevation
type: influence
tags: [grain, texture, analog, tactile, overlay, dark-mode, material, depth, particle]
reference: Screen printing, risograph, film grain, letterpress, photographic paper
expresses: [cinematic-dark]
---

A low-opacity tiled PNG texture applied as an absolute overlay on dark surfaces — adding analog grain, particle depth, and printed-object tactility. The surface reads as a physical material rather than a flat digital plane.

**Technique:** An absolutely positioned element covering the target surface, with `opacity-10` (or similar low value), `mix-blend-overlay`, and `pointer-events-none`. The texture tiles seamlessly and does not interrupt content interaction.

**Effect:** The surface gains the impression of depth without cast shadow. It suggests the texture of a photographic print, a darkroom print, a screen-printed poster. Warmth without color. Material without weight.

**When to use:** Dark surfaces in cinematic, esoteric, or analog aesthetic contexts where flat color reads as sterile. Works best against near-black backgrounds — the low-opacity overlay on near-white reads as noise rather than texture.

## Observed Markup

```html
<div class="absolute inset-0 opacity-10 pointer-events-none mix-blend-overlay
            bg-[url('https://www.transparenttextures.com/patterns/stardust.png')]">
</div>
```

Stitch gravitates toward `transparenttextures.com` patterns. Common patterns observed: `stardust.png`, `noise.png`, `subtle-grunge.png`. The URL pattern is `https://www.transparenttextures.com/patterns/{name}.png`.

## Invocation

Stitch will generate this spontaneously when the aesthetic context is cinematic, esoteric, or dark-analog. To invoke deliberately:

> "Add a subtle grain texture overlay to dark panel surfaces — low opacity, mix-blend-overlay, analog material quality."

## Notes

- Apply to the container, not the page canvas — canvas-level grain reads as a background pattern, not surface material
- `rounded-full` or matching the parent's border-radius is required when applied to shaped elements
- Pairs with: `tonal-layering`, `glass-blur`, `cinematic-dark` concept, `cinematic-celestial` aesthetic
- Do not use on light backgrounds — the blend mode produces noise artifact rather than texture depth
