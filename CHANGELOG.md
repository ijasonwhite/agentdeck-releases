# Changelog

## 1.13.0 — 2026-08-02

**Engineer Prompt studio.** The per-tab CLAUDE.md editor grew into a full
prompt-engineering environment:

- Real text engine: native find & replace (⌘F), full undo/redo, live markdown
  syntax highlighting (headings, bold, inline code, fences, lists, quotes).
- Section outline sidebar — click a heading to jump.
- Snippet library — insert proven prompt blocks (Role & Mission, Hard
  Constraints, Do/Don't, Commands, Code Style, Testing Rules, Output Format,
  Guardrails, Definition of Done) at the cursor.
- AI Assist — Improve & Tighten, Make More Directive, Add Missing Sections,
  or Fix Grammar Only, powered by your own Anthropic key. ⌘Z undoes a rewrite.
- Version history — every save snapshots the previous version (last 20);
  restore any snapshot from the History menu.
- Rendered preview toggle, live word/char/~token/section stats, dirty-state
  guard, ⌘S saves in place.

**Collapsed tab groups.** Right-click a grouped tab → **Group Tabs** to fold
the group behind a single parent chip: shows the active member, a member
count, and a chevron menu listing every tab (with waiting indicators).
Dropping a tab on the parent joins the group. **Expand Group** restores the
row.

## 1.12.2 — 2026-08-02

- Setting a tab home now seeds a starter `CLAUDE.md` (never overwrites),
  pre-filled from a scan: stack, suggested commands, git branch/remote,
  top-level layout.
- **Engineer Prompt…** added to the tab context menu.

## 1.12.1 — 2026-08-02

- Tab colours (9 presets) via **Change Colour**.
- Tab groups: **Create Group**, drag a tab onto a member to join and adopt
  the group colour, group-wide recolour, **Remove from Group**.
- Tabs with a home folder confirm before closing.

## 1.12.0 — 2026-08-02

- Per-tab home folders: right-click → **Set Home…**; agents spawned into the
  tab start there with no directory prompt.

## 1.11.3 — 2026-08-01

- Tab bar overflow: auto-scroll to the active tab, edge fades, pinned **+**,
  all-tabs menu with waiting indicator.

## 1.11.2 — 2026-08-01

- Kimi Code added as a built-in agent.

## 1.11.1

- Per-tab focus affinity: switching tabs hands keyboard focus to that tab's
  last active terminal.

## 1.11.0

- Enterprise-grade overhaul across the app (stability, performance, UI).
