---
name: Planning & Research
description: Research-first planning team that grounds every implementation plan in codebase analysis, institutional learnings, and external best practices
slug: planning
manager: ../../agents/lead-researcher/AGENTS.md
includes:
  - ../../agents/lead-researcher/AGENTS.md
  - ../../agents/repo-research-analyst/AGENTS.md
  - ../../agents/best-practices-researcher/AGENTS.md
  - ../../agents/framework-docs-researcher/AGENTS.md
  - ../../agents/git-history-analyzer/AGENTS.md
  - ../../agents/learnings-researcher/AGENTS.md
  - ../../agents/spec-flow-analyzer/AGENTS.md
  - ../../skills/ce-plan/SKILL.md
  - ../../skills/ce-brainstorm/SKILL.md
  - ../../skills/document-review/SKILL.md
---

This team activates during the Plan phase. Before any implementation plan is written, researchers analyze the repo structure, search institutional learnings from `docs/solutions/`, check framework documentation, and review git history for relevant patterns.

Workflow:
1. `ce:brainstorm` explores requirements for new features
2. Research agents gather context in parallel
3. `ce:plan` produces a grounded implementation plan
4. `spec-flow-analyzer` identifies gaps in specifications before work begins
