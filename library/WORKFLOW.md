# Stitch Generation Workflow

Practical process for composing, iterating, and refining Stitch screens using the library. Covers three distinct modes: opening prompt construction, directional iteration on existing screens, and staged redesign.

---

## Mode 1 — Opening Prompt

The opening prompt is the most consequential moment in the design process. A strong opening prompt produces a result close enough to the target that subsequent edits are refinements. A weak one produces a generic result that requires corrective edits to rescue.

### Structure

A strong opening prompt does four things simultaneously:

1. **Concept as story** — a short narrative that establishes the creative territory before any specification. What is this? Who is it for? What should it feel like? This is not a design brief — it is a reason the design exists.

2. **Material references** — ground the abstraction in physical, real-world references. Not "warm and inviting" but "lodge amber, firelight, the specific cold of high altitude." Material references give the model a world to design in, not instructions to follow.

3. **Design system** — colors (hex values), typography (role + character), elevation, shape, components. Every dimension specified with hard constraints. See [Hard vs Soft Constraints](#hard-vs-soft-constraints).

4. **Layout brief** — enumerated panels or sections with specific content. Not prose descriptions of structure — numbered items with explicit content per section.

### Example structure

```
[Concept as story — 1–3 sentences. What it is, what it feels like, why it exists.]

[Design system — colors with hex values, typography roles, elevation rule, shape, components.]

[Layout — named pattern + enumerated panels with content.]
```

### What to avoid

- Opening with the design system before establishing the creative territory
- Describing layout in prose ("alternating panels of media and text") instead of enumerating panels
- Leaving any dimension unspecified — Stitch fills gaps with its defaults, which are generic
- Embedding do's and don'ts that restate specs already in the design system

---

## Mode 2 — Directional Edits

A directional edit is a single-variable change applied to an existing screen via Stitch's variant generation workflow. The goal is to isolate cause and effect — change one variable, observe the result, know which change drove the improvement.

### Variant generation settings

Each directional edit specifies four things:

- **Options** — number of variants to generate (2 for Refine edits, 3 for Explore/Reimagine)
- **Creative range** — Refine (small move), Explore (medium move), Reimagine (full reconception)
- **Aspects to vary** — which checkboxes to enable: Layout, Color scheme, Images, Text font, Text content
- **Custom instructions** — the direction text pasted into the prompt box

### Format

Every directional edit has a **general** version and a **specific** version.

**General** — applicable to any design with the same underlying problem. Written in terms of design principles, not content.

**Specific** — targeted at the current design. Names the elements, describes the exact change needed.

```
**Edit title**
[N] options · [Creative range] · [Aspect ☑] [Aspect ☑]

General: "[instruction applicable to any design]"

Specific: "[instruction naming this design's elements specifically]"
```

### Aspect selection rules

- **Single-variable edits**: one aspect only. Checking multiple aspects conflates variables.
- **Concept edits** are the exception — concepts are cross-dimensional by definition. Layout ☑ Color scheme ☑ Text font ☑ together test one variable: the concept.
- **Layout directions**: Layout ☑ only.
- **Typography directions**: Text font ☑ only.
- **Color directions**: Color scheme ☑ only. If the direction strips fills from components, also check Layout ☑.

### Do not combine edits

Run each edit independently on the same source screen. Combining edits produces a better or worse result but no knowledge of which change drove it. The next design starts from zero again.

---

## Mode 3 — Staged Redesign

When an existing design has fundamental problems — wrong aesthetic territory, wrong layout structure, wrong concept — directional edits on individual dimensions won't fix it. Use the staged redesign process.

### Stage 1 — Emotional direction

Establishes the aesthetic territory and the feeling the design should produce. Does not prescribe color or typography — those are execution decisions that follow from the feeling.

**Structure:** Emotion → Principle → Rejection

- Name the emotion/feeling the design should produce
- Name the design principles that express that emotion (specific, visual, structural)
- Explicitly reject the current design patterns that block the target

**Settings:** All aspects ☑, Reimagine, 3 options

**Key insight:** Emotional language alone is not enough. "Warmth and immediacy" without the design principles that express them produces a literal translation — Stitch defaults to the most conventional visual metaphor for the words. The principles are what steer away from defaults.

### Stage 2 — Layout direction

Establishes the structural logic of the page, rooted in the page's goal. Not which grid pattern to use — what the layout must achieve.

**Structure:** Reasoning → Enumerated structure → Rejection

- Why the default layout pattern fails the page's goal
- The structural alternative (enumerated panels, not prose)
- What the current structure does that blocks the goal

**Settings:** Layout ☑ only, Explore, 3 options

**Key insight:** Layout directions must enumerate panels explicitly. Prose descriptions of structure ("alternating full-bleed panels") get interpreted as aesthetic guidance and don't change the architecture. Numbered panels with specific content are hard constraints.

### Stage 3 — Specifics

After Stage 1 and 2 establish the aesthetic territory and structural logic, run individual single-variable edits for color, typography, and components.

---

## Hard vs Soft Constraints

The most important principle for prompt effectiveness: hard constraints execute reliably, soft constraints get overridden by Stitch's defaults.

**Hard constraints** — change the output predictably:
- Hex color values (`#ECC246`)
- Specific font names or roles (`EB Garamond, high-contrast editorial serif`)
- Roundness values (`0px everywhere`)
- Enumerated panels with content (`Panel 1: hero — headline, single gold CTA`)
- Explicit absence rules (`No shadows anywhere`)

**Soft constraints** — frequently ignored:
- Do's and don'ts that restate a spec already present
- Prose descriptions of layout intent ("alternating," "curated," "deliberate")
- Emotional language without design principles
- Behavioral rules that conflict with Stitch's component defaults (`"use gold once per panel"`)

**When soft constraints are worth keeping:** only when blocking a specific Stitch default that no spec directly addresses. "No decorative background typography" and "photography is untreated — no color filters" are worth keeping because they prevent specific default behaviors that specs don't cover.

---

## Semantic Compression

When a prompt is too long, compress it without losing information. The goal is lossless reduction — keep everything that changes the output, cut everything that doesn't.

**What to cut:**
- Prose that restates a spec in different words
- Color poetry (the metaphor after the hex value — keep the hex, cut "the infield at first light")
- Do's and don'ts that restate specs
- Explanations of why a rule exists (the rule is the rule)

**What to keep:**
- Every hex value
- Every font role and character description
- Every explicit absence rule (`0px`, `no shadows`)
- Every enumerated panel with content

**One-sentence layout test:** A look book panel structure can be described in one sentence: "Full-viewport photography panels where text floats over the frame — eyebrow, headline, single CTA — alternating left and right as you scroll." If a layout description is longer than two sentences, compress it.

---

## Look Book Patterns

Two distinct look book layouts. Choose based on what the page is trying to achieve.

### Full-bleed scroll-snap

Photography is the surface of the page. Text floats over the frame. Scrolling feels like turning pages.

**Use when:** the destination or experience should feel immersive — the user should feel present in the place, not reading about it.

**One-sentence version:** "Full-viewport photography panels where text floats over the frame — eyebrow, headline, single CTA — alternating left and right as you scroll."

### Two-column fixed/sliding

Left column fixed, right column scrolls. Left panel updates to reflect whichever right-column item is in view.

**Use when:** multiple items need to be browsed with editorial context — the left column provides reading, the right column provides evidence.

**One-sentence version:** "Two columns — left fixed (eyebrow, headline, body, text CTA), right scrolling (full viewport-height photography per item) — left updates as right scrolls."

---

## Color Extraction from Reference

When deriving a color scheme from a physical reference (packaging, print, a photograph):

1. **Extract four values** mapped to Primary, Secondary, Tertiary, Neutral
2. **Assign roles by function**, not by prominence:
   - **Primary** → the interactive color. Stitch maps this to buttons and CTAs by default. If you want gold buttons, gold must be Primary.
   - **Secondary** → structural elements, headings, supporting UI
   - **Tertiary** → single accent, used sparingly. Muted when Secondary is already chromatic. Vivid when Primary and Secondary are both low-chroma.
   - **Neutral** → the canvas. Drives on-surface text color through tonal derivation.

3. **Check tonal separation** — Primary and Neutral must be sufficiently different in saturation or hue for Stitch's tonal derivation to produce meaningful contrast. Values that are near-identical (e.g., `#0A0E1A` and `#080C14`) collapse into each other in the generated system.

4. **Verify with tokens** — read the generated HTML to extract actual CSS custom property values. The thumbnail preview is unreliable due to photography filters and compression. The token values are the ground truth.

---

## The `prompt:` Field

Concepts and aesthetics in the library contain a `prompt:` field in their frontmatter. This is the paste-ready generation instruction — the text that invokes the concept or aesthetic in a Stitch prompt.

**Use it as:** a foundation block in an opening prompt. Drop the `prompt:` value into the generation prompt directly, then add layout brief and content on top.

**Why frontmatter, not body prose:** the library is intended to be surfaced through an MCP server. Frontmatter is parsed as structured data, making the `prompt:` field directly extractable without markdown parsing.
