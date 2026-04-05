---
name: "Bottom Tabs"
entity: layout
slot: layout
type: structural
tags: [mobile, tab-bar, navigation, ios, android, app-shell]
expresses: []
prompt: >-
  The viewport is divided into two zones: the full-screen content area fills the top portion and scrolls independently; a fixed bottom bar (49–60px tall) contains 3–5 tab items arranged horizontally. Each tab item has an icon above and a short label below. The active tab icon and label are visually highlighted. The content area renders the active tab's screen. On scroll, the content area scrolls under a potential sticky top header; the bottom bar never scrolls.
---

The primary navigation shell for mobile applications. Choose this when users need to switch between 3–5 top-level destinations — it keeps navigation always accessible without consuming content space. The bottom position is thumb-friendly on large phones. For more than five destinations, consider a sidebar or overflow menu instead. Pairs with any content layout within the tab screens; the shell itself is minimal and should not fight with the content.
