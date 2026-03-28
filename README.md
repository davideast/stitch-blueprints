# Stitch Blueprints

A structured vocabulary for composing Stitch screen generation prompts. The library is organized into distinct entity types — each with a specific role in the composition process.

For the full specification of entity types, naming conventions, and relationships, see [TAXONOMY.md](TAXONOMY.md).

For the generation workflow — opening prompts, directional edits, staged redesign — see [WORKFLOW.md](WORKFLOW.md).

---

## Entity Types

### Concepts
Named design philosophies. Abstract and universal — they describe what a design is trying to be, not how it looks. Each contains a `prompt:` field: a paste-ready generation instruction for direct use in Stitch.

`concepts/` — minimalism, editorial, cinematic-dark, data-dense

### Aesthetics
Named visual territories with a specific sensory character. More concrete than concepts — they describe what a design feels like, not just what principle it follows. Each contains a `prompt:` field for direct use in Stitch.

`aesthetics/` — cinematic-celestial, editorial-luxury

### Identities
Named, tested compositions of blueprints that form a coherent design system. References blueprints by name. Contains identity-specific rules that don't generalize to universal blueprints.

`identities/` — cartographers-atlas, the-observatory

### Directions
Empirically validated instruction sentences that move a design toward a concept. Used in Stitch's variant generation workflow as Custom instructions. Each direction has a general version (any design with the same problem) and a specific version (names this design's elements explicitly).

`directions/` — 48 directions across type, layout, color, elevation, and concept move families

### Vibes
Dimension-specific prose descriptors. Each vibe maps to exactly one DESIGN.md section — typography, elevation, components, or dos-donts.

```
vibes/
  systems/        multi-dimensional rule sets (ring-edge-definition)
  typography/
    headline/     editorial-serif, technical-mono, left-aligned-editorial
    body/         humanist-sans
    label/        uppercase-tracking, monospace-eyebrow
  elevation/      tonal-layering, glass-blur, editorial-shadow, offset-shadow-depth
  components/
    buttons/      professional
  dos-donts/      left-aligned-hero
```

### Structure
Structural patterns that go into the prompt body — not into DESIGN.md. They describe what to build, not how it should look.

```
structure/
  layouts/        look-book, bento-box, masonry-grid, feature-strip,
                  hero-full-screen, split-screen, horizontal-overflow,
                  timeline, infinite-scroll-feed, editorial-mosaic
  ui-components/  skeleton-loader, empty-state, activity-feed, context-menu,
                  notification-center, timeline-entry, code-block,
                  rating-star-input, canvas-grid
  decorations/    canvas-grid, testimonial-photo-card, arch-portal
```

### Values
Deterministic settings. Set values directly — Stitch honors these with high reliability.

```
values/
  color-schemes/  obsidian-atlas, deep-space, atlantic, noir-crimson,
                  crimson-standard, gilt-obsidian, minimalist-neo-esoteric,
                  tracks-of-washington, planetary-theater,
                  + P1–P7 observed schemes
  roundedness/    sharp (0px), soft (8px), rounded (16px)
```

---

## How to Compose

The library is reference vocabulary. Composition is judgment — select coherent blueprints that express the same concept and synthesize them into a prompt. Do not concatenate mechanically.

**Opening prompt (new screen):**
Start with a concept or aesthetic and its `prompt:` field as the foundation. Add a design system (hex values, typography roles, roundedness) and an enumerated layout brief. See WORKFLOW.md Mode 1 for the full structure.

**Directional edit (variant on existing screen):**
Select a direction from `directions/` and paste it as custom instructions in Stitch's variant workflow. Set Options, Creative range, and Aspects to vary before generating. Run each edit independently — one variable at a time. See WORKFLOW.md Mode 2.

**Start from an identity:**
An identity is a complete, tested composition. Use it directly or as a starting point — swap individual blueprints to explore variations.

**Start from scratch:**
Select one blueprint from each relevant slot. More slots = more directed output. Fewer slots = more Stitch judgment.

---

## Composition Examples

**Opening prompt with concept:**
```
[concept prompt: field value]

Colors: Primary #hex, Secondary #hex, Tertiary #hex, Neutral #hex
Typography: [role + character description]
Shape: 0px everywhere
No shadows.

Panel 1: hero — [content]
Panel 2: [content]
Panel 3: [content]
```

**Concept-driven (legacy format):**
```
Concept: Minimalism
Color scheme: Crimson Standard
Typography headline: Editorial Serif
Elevation: Tonal Layering

A home page for a marathon training app.
```

**Identity-based:**
```
Identity: The Cartographer's Atlas
Layout: Bento Box  ← override the default layout for a different screen type

A catalog page for a geographical data platform.
```

**Directional edit:**
```
[existing screen in Stitch]
Options: 3 · Explore · Layout ☑

"Lead with one giant typographic statement — a single headline scaled to near full-viewport width. No hero image. Typography is the hero."
```

---

## Blueprint → Prompt Relationship

| Entity | Goes into |
|---|---|
| Color scheme | DESIGN.md Colors section (via Stitch token derivation) |
| Roundedness | DESIGN.md Shape section |
| Vibe | The DESIGN.md section it maps to |
| Rule set | Multiple DESIGN.md sections simultaneously |
| Layout | Prompt body |
| UI component | Prompt body |
| Decoration | Prompt body |
| Concept | `prompt:` field → foundation of opening prompt |
| Aesthetic | `prompt:` field → foundation of opening prompt |
| Identity | Resolves to its referenced blueprints |
| Direction | Variant generation custom instructions |
