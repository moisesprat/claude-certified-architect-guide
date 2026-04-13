# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repo Is

A self-contained, offline study guide for the **Claude Certified Architect – Foundations** certification exam. All files are standalone HTML with embedded CSS and JS — no build step, no package manager, no server required.

Open any file directly in a browser:
- `architect_exam_checklist.html` — progress tracker (30 tasks across 5 domains, state saved to localStorage)
- `domain1-offline.html` through `domain5-offline.html` — one lesson per exam domain

## Exam Domain Structure

| File | Domain | Exam Weight |
|------|--------|-------------|
| domain1-offline.html | Agentic Architecture & Orchestration | 27% |
| domain2-offline.html | Tool Design & MCP Integration | 18% |
| domain3-offline.html | Claude Code Configuration & Workflows | 20% |
| domain4-offline.html | Prompt Engineering & Structured Output | 20% |
| domain5-offline.html | Context Management & Reliability | 15% |

Pass score: 720/1000.

## HTML File Architecture

Each domain lesson follows a consistent internal structure:

- **Sticky header** — domain badge, exam weight badge, section progress dots
- **Left sidebar** (250px, sticky) — navigation links grouped by task (`ts11`, `ts12`, …)
- **Main content area** — sections per task skill, each containing:
  - `#tsXY` — title block with task statement
  - `#tsXY-concept` — core concept explanation
  - `#tsXY-*` — implementation details, architecture diagrams (ASCII/code), anti-patterns, exam traps
  - `#tsXY-task` — hands-on implementation exercise
  - `#tsXY-questions` — MCQ exam simulation with reveal-on-click answers

All styles and scripts are inline (no external dependencies except Google Fonts in the checklist file). The domain files are explicitly marked `Self-contained: no external resources required`.

## Checklist Data Model

Task IDs follow the pattern `{domain}.{task}` (e.g., `1.1`, `3.6`). State is persisted to `localStorage` under the key `architect_exam_checklist_v1` as a plain object `{ "1.1": true, "2.3": true, … }`.
