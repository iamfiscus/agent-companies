---
name: Knowledge & Compounding
description: Knowledge management team that captures solutions, maintains institutional memory, and ensures learnings compound across sprints
slug: knowledge
manager: ../../agents/vp-knowledge/AGENTS.md
includes:
  - ../../agents/vp-knowledge/AGENTS.md
  - ../../agents/learnings-researcher/AGENTS.md
  - ../../agents/style-editor/AGENTS.md
  - ../../skills/ce-compound/SKILL.md
  - ../../skills/document-review/SKILL.md
---

This team owns the Compound phase. After every review cycle, solved problems are documented in `docs/solutions/` using the compound-docs format.

Solution doc format (YAML frontmatter):
- module, problem_type, component
- symptoms, root_cause, solution, prevention
- tags, severity

Categories: `build-errors/`, `performance-issues/`, `database-issues/`, `security-issues/`, `logic-errors/`, `best-practices/`

Critical patterns are promoted to `docs/solutions/patterns/critical-patterns.md`.
