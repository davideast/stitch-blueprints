# Library Taxonomy

The authoritative reference for entity types, relationships, naming conventions, and directory structure. All library entries must conform to this specification.

---

## Entity Types

### Concept
**What it is:** A named design philosophy. Abstract and universal — it does not specify any value, color, font, or layout. It describes the principle a design *is trying to embody*, not the sensory territory it occupies (see Aesthetic for that).

**Scope:** Cross-dimensional. A concept makes implicit claims about multiple design dimensions simultaneously.

**Named by:** The philosophy itself, in plain language.
- ✓ `minimalism`, `editorial`, `data-dense`, `esoteric`, `maritime-heritage`
- ✗ `minimalist-hero` (too application-specific), `sovereign-analyst` (metaphor, not philosophy)

**Directory:** `library/concepts/`

**Frontmatter:**
```markdown
---
name: "Minimalism"
entity: concept
tags: [minimal, reduction, whitespace, restraint, essential]
reference: Muji, Apple, Dieter Rams, Swiss International Style
prompt: >-
  Remove everything that isn't load-bearing. One dominant element per section.
  Typography carries the full weight of the design. What remains should feel inevitable.
expressed-by:
  vibes: [tonal-layering, editorial-serif, ring-edge-definition]
  layouts: [hero-full-screen, look-book]
  color-schemes: [crimson-standard]
  roundedness: [sharp]
---
```

**`prompt` field:** Required. A paste-ready generation instruction for Stitch — imperative voice, directly invokable. Stored in frontmatter for clean programmatic extraction by the MCP server.

**Body:** A short, authoritative definition of the philosophy. What it values. What it rejects. The design principle in plain language.

---

### Aesthetic
**What it is:** A named visual territory with a specific sensory character. More concrete than a concept — it describes what a design *feels like*, not just what principle it follows. Named after the experiential domain it evokes.

**Concept vs Aesthetic:**
- A **concept** answers "how is this designed?" → `minimalism` (design principle)
- An **aesthetic** answers "what does this feel like?" → `cinematic-celestial` (experiential territory)

An aesthetic may *express* one or more concepts, but it is not the concept itself.

**Scope:** Cross-dimensional. Like a concept, an aesthetic implies typography, elevation, color, and layout choices simultaneously.

**Named by:** The evocative name of the sensory/experiential territory.
- ✓ `cinematic-celestial`, `editorial-luxury`, `neo-esoteric`, `maritime-heritage`
- ✗ `minimalism` (abstract principle, not territory), `dark-mode-cinematic` (describes type, not territory)

**Directory:** `library/aesthetics/`

**Frontmatter:**
```markdown
---
name: "Cinematic Celestial"
entity: aesthetic
tags: [dark-mode, astronomical, sublime, chiaroscuro, scale, immersive, cinematic, awe, planetary]
reference: High-end planetarium shows, deep-space observatory domes, atmospheric sci-fi films
prompt: >-
  Design this like the establishing shot of a rigorous sci-fi film — not space tourism, not retrofuturism.
  Overwhelming dark backgrounds with single blazing points of concentrated light. Every element must
  earn its brightness against the darkness.
expressed-by:
  vibes: [glass-blur, tonal-layering, technical-mono]
  layouts: [hero-full-screen, look-book]
  color-schemes: [planetary-theater, deep-space]
  roundedness: [soft]
---
```

**`prompt` field:** Required. A paste-ready generation instruction for Stitch — the text an LLM or user drops directly into the generation prompt to invoke this aesthetic. Written in imperative voice. Stored in frontmatter (not body) for clean programmatic extraction by the MCP server.

**Body:** A prose description of the sensory experience. What it looks and feels like. What it rejects. Real-world reference domain in plain language.

---

### Direction
**What it is:** An empirically validated instruction sentence (or short paragraph) that moves a design toward a concept. Dynamic — it describes a move, not a state.

**Why it exists:** Specific phrasings produce measurably better variant results than generic ones. Directions are proven formulations, not just descriptions of concepts. They have value because the wording matters.

**Scope:** Cross-dimensional by definition. A direction simultaneously invokes multiple vibes, layouts, and values.

**Named by:** The move being made — short, verb-forward.
- ✓ `strip-to-essence`, `amplify-type`, `add-depth`, `editorial-weight`
- ✗ `toward-minimalism` (too passive), `minimalism-direction` (redundant)

**Directory:** `library/directions/`

**Frontmatter:**
```markdown
---
name: "Strip to Essence"
entity: direction
tags: [minimalism, simplify, whitespace, reduce, layout, typography]
targets: minimalism
invokes:
  vibes: [tonal-layering, editorial-serif]
  layouts: [hero-full-screen, look-book]
---
```

**Body:**
```markdown
"Explore minimalist layouts. Use large editorial typography. Less is more."

## When to use
Design feels cluttered or over-specified. Too many elements competing for attention.

## What it moves
Reduces component count, opens whitespace, enlarges type, flattens elevation.

## Variations
- "Strip everything back. One element per panel. Typography is the design."
- "Whitespace is the design. Let the content breathe."
```

---

### Spec
**What it is:** A prose descriptor for a specific design dimension. Maps to exactly one DESIGN.md section. Describes how a design property looks, feels, or behaves — not which concept it expresses.

**Scope:** Single-dimension. This is a hard rule.
- If an entry touches two DESIGN.md sections → decompose into two vibes.
- If an entry spans all dimensions → it is a Concept, not a Vibe.
- If an entry is a coherent multi-rule system → see Rule Sets below.

**Named by:** What the technique does — descriptive, not metaphorical, not attributed to a person.
- ✓ `tonal-layering`, `editorial-serif`, `monospace-eyebrow`, `ring-edge-definition`
- ✗ `ring-edge-definition` (named by source), `darkroom` (metaphor, belongs in concepts)

**Source attribution:** Goes in frontmatter `source:` field only. Never in the name.

**Directory:** `library/vibes/{dimension}/`
- `typography/headline/`, `typography/body/`, `typography/label/`
- `elevation/`
- `components/buttons/`, `components/inputs/`, `components/navigation/`
- `dos-donts/`

**Frontmatter:**
```markdown
---
name: "Tonal Layering"
entity: spec
slot: elevation
type: influence
tags: [flat, no-shadows, depth-through-color, modern]
reference: Material Design 3, Linear, Notion
expresses: [minimalism, data-dense]
---
```

---

### Identity
**What it is:** A named, tested composition of library blueprints that form a coherent, validated design system. References existing blueprints by name rather than inlining values. Contains identity-specific rules — application-specific guidance that doesn't generalize to a universal blueprint.

**Why it exists:** The combination of blueprints is itself information. Decomposing a tested design system into its constituent blueprints loses the knowledge that these specific choices work together. An identity preserves the composition record.

**Scope:** Cross-dimensional. References blueprints across all slots.

**Named by:** The named aesthetic or product the identity represents.
- ✓ `cartographers-atlas`, `the-observatory`
- ✗ `dark-editorial-identity` (describes type, not identity)

**Directory:** `library/identities/`

**Frontmatter:**
```markdown
---
name: "The Cartographer's Atlas"
entity: identity
concept: cinematic-dark
tags: [dark-mode, editorial, cartography]
references:
  color-scheme: obsidian-atlas
  roundedness: sharp
  typography.headline: editorial-serif
  elevation: tonal-layering
  layout: look-book
---
```

**Body:** The aesthetic concept description + identity-specific rules that don't generalize to universal blueprints + generation notes.

---

### Rule Set
**What it is:** A named collection of related rules that span multiple design dimensions but form a coherent, indivisible system. The rules only work correctly when applied together — decomposing them into separate vibes loses the system's coherence.

**When to use instead of decomposing:** When the rules have explicit cross-dimensional dependencies. The concentric radius rule only makes sense in the context of the ring border rule. Separating them produces incomplete guidance.

**Scope:** Multi-dimensional, but bounded — a rule set is not a philosophy (concept), it is a specific technique implementation.

**Named by:** What the system does.
- ✓ `ring-edge-definition`

**Directory:** `library/vibes/systems/`

**Frontmatter:**
```markdown
---
name: "Ring Edge Definition"
entity: rule-set
slots: [elevation, components, shape]
type: influence
tags: [ring, inset-ring, concentric-radius, no-border, clean]
expresses: [minimalism]
---
```

---

### Color Scheme
**What it is:** Four deterministic hex values mapped to the four Stitch panel roles (Primary, Secondary, Tertiary, Neutral). Sets the palette directly — Stitch's tonal derivation generates the full 60+ token hierarchy from these four values.

**Scope:** Single entity, four values. Not a vibe — no interpretation required.

**Named by:** An evocative name for the palette's character — not a hex value, not a description of hue.
- ✓ `atlantic`, `noir-crimson`, `gilt-obsidian`, `crimson-standard`
- ✗ `dark-navy-gold` (describes hue, not character)

**Directory:** `library/values/color-schemes/`

---

### Roundedness
**What it is:** A single integer representing the corner radius scale. Sets the value directly.

**Directory:** `library/values/roundedness/`

---

### Layout
**What it is:** A page-level structural pattern. Goes into the generation prompt body — not into DESIGN.md. Describes how content is organized spatially across the viewport.

**Named by:** The pattern name, descriptive.
- ✓ `look-book`, `bento-box`, `feature-strip`

**Directory:** `library/structure/layouts/`

---

### UI Component
**What it is:** A specific UI pattern to include in a screen. Goes into the generation prompt body.

**Directory:** `library/structure/ui-components/`

---

### Decoration
**What it is:** A page-level finishing treatment — visual technique applied across the whole page, not tied to a specific component.

**Directory:** `library/structure/decorations/`

---

## Relationship Rules

```
Concept  ←───────────────  expressed-by  ───────────────→  Vibe
Concept  ←───────────────  expressed-by  ───────────────→  Rule Set
Concept  ←───────────────  expressed-by  ───────────────→  Layout
Concept  ←───────────────  expressed-by  ───────────────→  Color Scheme
Concept  ←───────────────  expressed-by  ───────────────→  Roundedness

Direction  ──→  targets  ──→  Concept
Direction  ──→  invokes  ──→  Vibe / Rule Set / Layout
```

- Relationships are declared in the **Concept** file's `expressed-by` field and the **Direction** file's `invokes` field.
- Vibes and Layouts declare which concepts they express via `expresses:` in frontmatter — this is the reverse pointer.
- Color Schemes declare `expresses:` concepts as tags — they are not tightly coupled to concepts because a palette can express multiple concepts.

---

## Naming Conventions

| Rule | ✓ | ✗ |
|---|---|---|
| Name by function, not source | `ring-edge-definition` | `tailwind-ring-system` |
| Name by philosophy, not metaphor (concepts) | `minimalism` | `minimalist-hero` |
| Name by move, verb-forward (directions) | `strip-to-essence` | `toward-minimalism` |
| Name by character, not hue (color schemes) | `atlantic` | `dark-navy-gold` |
| No grab-bag files unified by authorship | — | `tailwind-spacing-tokens.md` |

---

## Directory Structure

```
library/
  TAXONOMY.md               ← this document

  concepts/                 ← named design philosophies (abstract principles)
  aesthetics/               ← named visual territories (experiential character)
  identities/               ← tested blueprint compositions
  directions/               ← variant instruction sentences

  vibes/                    ← dimension-specific prose descriptors
    systems/                ← multi-dimensional rule sets
    typography/
      headline/
      body/
      label/
    elevation/
    components/
      buttons/
      inputs/
      navigation/
    dos-donts/

  structure/                ← structural patterns (prompt body)
    layouts/
    ui-components/
    decorations/

  values/                   ← deterministic settings
    color-schemes/
    roundedness/
```
