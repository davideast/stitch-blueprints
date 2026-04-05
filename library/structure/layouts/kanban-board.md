---
name: "Kanban Board"
entity: layout
slot: layout
type: structural
tags: [kanban, columns, cards, workflow, project-management, pipeline]
expresses: []
prompt: >-
  A horizontally-scrolling surface containing 3–7 fixed-width columns (240–300px each). Each column has a header with a status label and item count. Below the header, cards stack vertically and are draggable between columns. A "+ Add" button sits at the bottom of each column. The board surface itself scrolls horizontally; individual columns scroll vertically when overflow occurs.
---

The workflow visualization layout for project management, CRM pipelines, and status-based systems. Choose this when the primary user action is moving items between states. The column-per-status mental model is instantly legible to most users. Works best when statuses number between 3 and 7 — more columns than that require horizontal scrolling that degrades usability. Pairs with compact card designs and a clean, low-noise aesthetic.
