# Research & Knowledge Kit

Research with cited sources, deep-read papers into Markdown or Obsidian-style vaults, keep a living wiki, and hand work between sessions without losing context or project memory.

A setup for AI coding agents, made by [Kitloom](https://kitloom.site). One source, generated for every major agent: Claude Code, OpenAI Codex, Cursor, Google Antigravity, Gemini CLI, GitHub Copilot, Windsurf (Devin), opencode and Aider.

## Install

1. Download this repository as a ZIP, or use the **Check and download** button on its Kitloom page, which checks it first.
2. Read the files. Nothing here runs on its own: the kit has no hooks and no install scripts.
3. Copy the folders and files you want into the root of your project. `AGENTS.md` is the shared instructions file; edit it to fit your project.

## What is inside

### Skills

- `research` — Investigate a question against primary sources and save the findings as a Markdown file in the repo.
- `deeppapernote` — Turn one paper (title, DOI, arXiv ID or PDF) into a polished deep-reading note in an Obsidian-style vault.
- `wiki-ingest` — Add a new raw source to the wiki: extract key facts, update pages and cross-references, log the change.
- `wiki-query` — Answer a question from the wiki with citations, and file valuable answers back as pages.
- `wiki-lint` — Periodically check the wiki for contradictions, stale claims, orphan pages and missing links.
- `grounded-vault` — Keep every number or quote in a compiled page traceable to an immutable source, with cheap drift detection.
- `handoff` — Compact the current conversation into a handoff document so another session or agent can continue.
- `context-engineering` — Set up rules and context files at session start, or when output quality degrades mid-task.
- `neat-freak` — At the end of a work stretch, reconcile project docs and rule files with what is actually true.
- `retro` — Run a short retrospective after a session and capture what to do differently next time.

### Commands

Invoke by name (for example `/start-research`).

- `start-research` — Research a question from primary sources and write a cited findings note.
- `write-handoff` — Write a compact handoff note so a fresh session can continue the work.
- `capture` — Save a decision, fact or lesson from this session into the project memory notes.

### Sub-agents

- `source-reader` — Delegate to read one long document or paper and return a faithful, cited summary without polluting the main context.
- `vault-librarian` — Delegate to audit the notes folder for broken links, orphan notes, duplicates and uncited claims.

### Scoped rules

- `cite-sources` — Always on: every factual claim in research output names its source, and unverified claims are labelled.
- `vault-notes` — Conventions for Markdown notes, links and frontmatter in the notes, research and wiki folders.
- `handoff-files` — Format and hygiene for handoff and project-memory files.

## Where each agent finds it

| Agent | Instructions | Skills and commands | Rules | Sub-agents |
|---|---|---|---|---|
| Claude Code | `CLAUDE.md` (imports `AGENTS.md`) | `.claude/skills/` | `.claude/rules/` | `.claude/agents/` |
| OpenAI Codex | `AGENTS.md` | `.agents/skills/` | listed in `AGENTS.md` | `.codex/agents/` |
| Cursor | `AGENTS.md` | `.agents/skills/`, `.claude/skills/` | `.cursor/rules/` | `.claude/agents/` |
| Google Antigravity | `AGENTS.md` | `.agents/skills/` | `.agents/rules/` | `.agents/agents/` |
| Gemini CLI | `AGENTS.md` via `.gemini/settings.json` | `.agents/skills/`, `.gemini/commands/` | listed in `AGENTS.md` | `.gemini/agents/` |
| GitHub Copilot | `AGENTS.md` | `.agents/skills/`, `.github/prompts/` | `.github/instructions/` | `.claude/agents/` |
| Windsurf (Devin) | `AGENTS.md` | `.agents/skills/`, `.windsurf/workflows/` | `.windsurf/rules/` | — |
| opencode | `AGENTS.md` | `.agents/skills/`, `.opencode/commands/` | listed in `AGENTS.md` | `.opencode/agents/` |
| Aider | `AGENTS.md` via `.aider.conf.yml` | — | — | — |

Skills are stored twice (`.agents/skills/` and `.claude/skills/`) because Claude Code reads only its own folder. Agents that read both may list a skill twice; delete the copy you do not need.

## Credits

The skills come from these open-source repositories, each under its own licence. Their licence and a notice are kept beside every copied skill.

| Skill | Source | Licence |
|---|---|---|
| `research` | [mattpocock/skills](https://github.com/mattpocock/skills) at `49dd158` | MIT |
| `deeppapernote` | [917Dhj/DeepPaperNote](https://github.com/917Dhj/DeepPaperNote) at `479c662` | MIT |
| `wiki-ingest` | [open-gitagent/opengap](https://github.com/open-gitagent/opengap) at `d7a8e2e` | MIT |
| `wiki-query` | [open-gitagent/opengap](https://github.com/open-gitagent/opengap) at `d7a8e2e` | MIT |
| `wiki-lint` | [open-gitagent/opengap](https://github.com/open-gitagent/opengap) at `d7a8e2e` | MIT |
| `grounded-vault` | [wshobson/agents](https://github.com/wshobson/agents) at `46891e7` | MIT |
| `handoff` | [mattpocock/skills](https://github.com/mattpocock/skills) at `49dd158` | MIT |
| `context-engineering` | [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) at `aeac41d` | MIT |
| `neat-freak` | [KKKKhazix/khazix-skills](https://github.com/KKKKhazix/khazix-skills) at `322346d` | MIT |
| `retro` | [mattpocock/skills](https://github.com/mattpocock/skills) at `49dd158` | MIT |

Everything else in this repository (instructions, rules, commands, sub-agents) is by Kitloom under the MIT licence.

## Use at your own risk

Read every file before you use it. Agent instructions can make an agent run commands on your machine. This kit was checked with Kitloom's pre-download check, which looks for warning signs but cannot prove anything is safe.
