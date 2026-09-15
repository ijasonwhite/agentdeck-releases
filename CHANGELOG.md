# Changelog

## 1.16.0 — 2026-09-15

**The Watcher.** Right-click a tab, Enable Watcher, and finished or stuck
agent turns in that tab are triaged automatically: the watcher answers
simple questions itself so agents stop hanging, fans work out to a
configurable roster of experts (Peer Reviewer, UI Expert, Data Expert, Test
Engineer, or your own), or escalates anything destructive or
judgement-shaped to you.

- Experts spawn as real agent tiles in the tab, pre-briefed; their findings
  are folded into direction and relayed back to the original agent.
- Experts can ask follow-up questions: the watcher relays the question to
  the primary agent and the answer back, capped at three rounds.
- Suggest mode (default) drafts watcher replies into Discuss for approval;
  Auto mode types them straight into the agent.
- Per-expert agent choice (run your reviewer on Claude, your data expert on
  Kimi…), with an Automatic fallback to the first detected CLI.
- Full audit: every decision, brief, question, answer, findings relay and
  escalation in the new Watcher Log window, and appended to
  watcher-audit.jsonl in Application Support.
- Guardrails: hard per-session action budget, cooldown between actions, and
  permission or destructive prompts always escalate to you.

Uses your Anthropic API key (Settings → AI summaries); idle without one.

## 1.15.3 — 2026-08-29

- Hovering over an agent terminal no longer moves the TUI's input cursor:
  bare mouse motion is no longer reported to apps using any-event mouse
  tracking (Claude Code moved its caret to follow the pointer, so keystrokes
  landed mid-sentence). Clicks, drags and scrolling report as before.
- Collapsed tab groups can rename the selected tab: double-click the parent
  chip, or right-click and choose Rename.

## 1.15.2 — 2026-08-04

- Agent launches no longer pollute your shell history: the auto-typed launch
  command is space-prefixed and flagged (HISTORY_IGNORE / HISTCONTROL) so
  zsh, bash and fish leave it out of the history file. Toggle in Settings →
  Interface ("Keep agent launches out of shell history", on by default).

## 1.15.1 — 2026-08-04

- Updater validation release (no functional changes).

## 1.15.0 — 2026-08-04

**Live status bar.** A realtime state-of-play strip along the bottom of the
window: session counts by state (the amber *waiting* cell pulses and clicking
it jumps to the next agent needing input, like ⌘J), tab count + active tab
and its home folder, the focused session's git branch/dirty/ahead-behind
state, relay and remote session counts, the hook-server port, and the app
version. Sections appear only when relevant.

## 1.14.1 — 2026-08-03

- Collapsed tab groups keep the home-folder indicator: the parent chip shows
  the house glyph (path on hover) for the member it displays, and the member
  menu marks homed tabs with a house icon / ⌂.

## 1.14.0 — 2026-08-02

**Automatic updates.** AgentDeck now updates itself via Sparkle: it checks the
public update feed in the background and offers new versions in-app, or on
demand via **AgentDeck → Check for Updates…**. Updates are EdDSA-signed and
the app remains notarized end to end. This is the last version you'll need to
download by hand.

## 1.13.1 — 2026-08-02

**Lazy tab loading.** Launching AgentDeck no longer starts every agent in
every tab at once. Restored sessions register as **sleeping** (grey) and a
tab's agents launch the first time you open that tab in the session — the
visible tab still wakes immediately, so launch feels identical but is far
lighter with many tabs.

**Auto Load per agent.** Each agent tile's new **⋯** menu has an
**Auto Load on Launch** toggle for sessions that rely on running from the
moment the app is up — they start at launch in any tab, exactly like the old
behaviour. Turning it on while a session sleeps wakes it immediately.

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
