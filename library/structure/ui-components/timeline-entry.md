---
name: "Timeline Entry"
entity: ui-component
slot: ui-component
type: structural
tags: [event, step, history, node, chronological]
expresses: []
prompt: >-
  Display a single timeline node — a dot or icon on a vertical spine connected to a content
  block with timestamp, title, and optional body with supporting detail, attachments, or
  metadata. Entries may be expandable. Connector line is solid for completed steps, dashed
  for pending.
---

A single node in a vertical timeline with connector line, timestamp, and expandable content. Choose this as the building block for timeline layouts — changelogs, process steps, history views. The connector line style (solid/dashed) communicates completion state. Pairs naturally with the timeline layout.
