---
name: Quality & Review
description: Multi-agent review team that audits code changes across security, performance, architecture, data integrity, patterns, simplicity, and agent-native compliance
slug: review
manager: ../../agents/vp-quality/AGENTS.md
includes:
  - ../../agents/vp-quality/AGENTS.md
  - ../../agents/architecture-strategist/AGENTS.md
  - ../../agents/security-sentinel/AGENTS.md
  - ../../agents/performance-oracle/AGENTS.md
  - ../../agents/code-simplicity-reviewer/AGENTS.md
  - ../../agents/pattern-recognition-specialist/AGENTS.md
  - ../../agents/data-integrity-guardian/AGENTS.md
  - ../../agents/agent-native-reviewer/AGENTS.md
  - ../../agents/schema-drift-detector/AGENTS.md
  - ../../skills/ce-review/SKILL.md
---

This team activates during the Review phase. Every code change runs through a configurable set of review agents.

Review agents operate with confidence-gated findings — they only surface issues they are confident about, reducing noise. Findings are merged and deduplicated before presentation.

Standard review set: architecture-strategist, security-sentinel, performance-oracle, code-simplicity-reviewer, agent-native-reviewer.

Extended sets:
- **Data changes:** Add data-integrity-guardian, schema-drift-detector
- **Frontend changes:** Add design-implementation-reviewer
