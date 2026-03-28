---
name: "Ring Edge Definition"
entity: rule-set
slots: [elevation, components, shape]
type: influence
tags: [ring, inset-ring, concentric-radius, no-border, no-shadow, clean, professional]
expresses: [minimalism, editorial]
---

A complete edge language built on rings rather than borders or drop shadows. Four rules that work together as a system — applying them individually produces incomplete results.

**1. Outer ring replaces border + shadow**
Any element that has both a visible edge and a shadow: remove the border entirely. Apply an outer `ring` at gray-950 / 10% opacity outside the element. The ring sits cleanly adjacent to the shadow without muddying the transition.

**2. Inset ring for light-background containers**
When a container has a light background and no shadow, use an inset ring at 5% opacity to define its boundary. More subtle than a border — it whispers the edge rather than drawing it.

**3. Concave container treatment**
Media and screenshot containers: gray-950 at 2.5–5% opacity background, zero bottom padding, no bottom border-radius — content "sits in" the container rather than floating above it. Add an inset ring at 5% opacity to define the container edge. The result reads as a recessed slot, not a floating card.

**4. Concentric radius on nested rounded elements**
When a rounded outer container holds a rounded inner element, set the inner radius to: outer radius − padding. Equal radius values on both look disconnected at small gap sizes. Concentric radii create visual harmony.
