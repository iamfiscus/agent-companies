# Review Agent Catalog

## Standard Set (Always Active)

| Agent | Specialization | Trigger Conditions |
|-------|---------------|-------------------|
| architecture-strategist | System design, component boundaries, patterns | All PRs |
| security-sentinel | OWASP top 10, injection, auth, secrets | All PRs |
| performance-oracle | N+1 queries, caching, bottlenecks | All PRs |
| code-simplicity-reviewer | YAGNI, premature abstraction, dead code | All PRs |
| agent-native-reviewer | Parity, granularity, composability | All PRs |

## Extended Set — Data Changes

| Agent | Specialization | Trigger Conditions |
|-------|---------------|-------------------|
| data-integrity-guardian | Migrations, transactions, referential integrity | PRs touching models, migrations, schemas |
| schema-drift-detector | Unrelated schema.rb changes | PRs containing schema.rb changes |

## Extended Set — Frontend

| Agent | Specialization | Trigger Conditions |
|-------|---------------|-------------------|
| design-implementation-reviewer | Figma-to-code visual fidelity | PRs touching views, components, CSS |

## Extended Set — Patterns

| Agent | Specialization | Trigger Conditions |
|-------|---------------|-------------------|
| pattern-recognition-specialist | Convention adherence, code smells | Large refactors, new patterns |

## Finding Severity Scale

| Level | Label | Action |
|-------|-------|--------|
| P1 | CRITICAL | Must fix before merge |
| P2 | IMPORTANT | Should fix, can negotiate |
| P3 | MINOR | Nice to fix, optional |

## Confidence Gating

Review agents only surface findings they are confident about. If confidence is below threshold, the finding is suppressed. This reduces noise and ensures actionable signal.
