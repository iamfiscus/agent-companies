---
name: Engineering
description: Execution team that implements plans systematically with atomic commits and continuous verification
slug: engineering
manager: ../../agents/vp-engineering/AGENTS.md
includes:
  - ../../agents/vp-engineering/AGENTS.md
  - ../../agents/bug-reproduction-validator/AGENTS.md
  - ../../agents/pr-comment-resolver/AGENTS.md
  - ../../skills/ce-work/SKILL.md
  - ../../skills/orchestrating-swarms/SKILL.md
  - ../../skills/agent-browser/SKILL.md
  - ../../skills/frontend-design/SKILL.md
---

This team activates during the Work phase. VP Engineering coordinates execution, ensuring agents commit after each completed task item and run verification checks before marking anything done.

Capabilities:
- Swarm mode for parallel execution of independent tasks
- Browser-based verification via `agent-browser`
- Bug reproduction and validation before fixes are attempted
- PR comment resolution in batch
