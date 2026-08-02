# AgentDeck

A native macOS command deck for AI coding agents. Run Claude Code, Codex,
Gemini, Grok, Aider, opencode, Cursor Agent, Qwen Code, Kimi Code — or any
custom CLI agent — side by side in a tabbed grid of live terminals, and always
know which one needs you next.

> This repository distributes the **notarized app builds** and documentation
> only. The source code is private. Downloads are on the
> [Releases](https://github.com/ijasonwhite/agentdeck-releases/releases) page
> with SHA-256 checksums.

---

## Features

- **Agent grid** — every agent in its own live terminal tile; zoom any tile to
  full-tab focus mode (⌘⏎) and back without interrupting the session.
- **Knows when an agent needs you** — precise Claude Code hook integration and
  an output heuristic for everything else. Waiting agents pulse amber across
  tabs; ⌘J jumps to the next one, wherever it is.
- **Workspace tabs** — group agents by project. Colours, drag-to-join tab
  groups (collapsible behind a single parent chip with a member chevron), and
  per-tab **home folders**: set a home once and every agent spawned into the
  tab starts there, no directory prompt.
- **Engineer Prompt** — a built-in prompt studio for each home's `CLAUDE.md`
  (the standing briefing agents load at boot): markdown editor with syntax
  highlighting, native find (⌘F), section outline, a snippet library of
  prompt-engineering blocks, AI-assisted rewrites, version history on every
  save, and live word/token stats. A starter file is auto-generated from a
  scan of the project when you set a home.
- **AI copilot for your agents** — optional TLDR summaries of what each agent
  is doing, a Discuss panel to reason about an agent's output before you
  reply, and Consult to get a second model's opinion (bring your own
  Anthropic API key).
- **Flows** — scripted multi-step agent runs.
- **Remote** — pair with AgentDeck on another machine over an encrypted relay
  and drive agents remotely.
- **Session history & library** — every session logged and resumable; recent
  work searchable from the command palette (⇧⌘P).
- **Native & fast** — SwiftUI + AppKit, universal binary (Apple Silicon +
  Intel), no Electron.

## Install

1. Download `AgentDeck.zip` from the latest
   [release](https://github.com/ijasonwhite/agentdeck-releases/releases).
2. Unzip and drag **AgentDeck.app** into **/Applications**.
3. Launch. The app is signed with a Developer ID and notarized by Apple, so
   Gatekeeper opens it without warnings.

**Requirements:** macOS 14 (Sonoma) or later. Universal binary.

Verify a download against the release's `CHECKSUMS.txt`:

```
shasum -a 256 -c CHECKSUMS.txt
```

## Getting started

1. Launch AgentDeck — it detects the agent CLIs installed on your PATH.
2. Press **+** (or ⌘T for a new tab), pick an agent, choose a folder.
3. Right-click the tab → **Set Home…** to pin the tab to a project, then
   **Engineer Prompt…** to write the standing briefing every agent in that
   tab will load.

## License

Free to download and use. See [LICENSE.txt](LICENSE.txt) — binaries only, no
redistribution, source code remains private.
