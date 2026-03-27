# Compound Loop Runbook

## The Four Phases

```
Plan -> Work -> Review -> Compound -> Repeat
```

80% of time is in Plan and Review. 20% in Work and Compound. Most thinking happens before and after code gets written.

## Phase 1: PLAN

### Steps
1. Understand the requirement — what, why, constraints
2. Research the codebase — `repo-research-analyst` finds existing patterns
3. Check institutional learnings — `learnings-researcher` searches `docs/solutions/`
4. Research externally — `best-practices-researcher` + `framework-docs-researcher`
5. Design the solution — approach, files, edge cases
6. Validate the plan — CTO reviews for agent-native compliance

### Plan Fidelities
- **Small:** Bug fixes, single-file changes. Minimal research.
- **Medium:** New features, multi-file changes. Standard research.
- **Large:** Architectural changes. Multiple research agents in parallel.

### A Good Plan Includes
- Context: Why are we doing this?
- Approach: How will we solve it?
- Files: What needs to change?
- Edge cases: What could go wrong?
- Tests: What validates this works?
- Rollback: How do we revert?

## Phase 2: WORK

### Steps
1. Set up isolation (worktree or branch)
2. Execute the plan step by step
3. Atomic commit after each task item
4. Run tests after significant changes
5. Create PR when done

### When to Intervene
- Tests failing repeatedly
- Agent clearly stuck
- Fundamental flaw in the plan -> send back to Plan phase

## Phase 3: REVIEW

### Steps
1. VP Quality selects review agent set
2. Launch review agents in parallel
3. Confidence-gated findings only
4. Merge and deduplicate across agents
5. Prioritize: P1 (must fix), P2 (should fix), P3 (nice to fix)
6. Resolve findings (parallel where possible)

### Three Questions (When No Tooling)
1. "What was the hardest decision you made here?"
2. "What alternatives did you reject, and why?"
3. "What are you least confident about?"

## Phase 4: COMPOUND

### Steps
1. Identify what was learned
2. Document using compound-docs format
3. Categorize and tag for searchability
4. Check for duplicates
5. Promote critical patterns

### Solution Doc Format
```yaml
---
title: "Issue Title"
module: affected-module
problem_type: category
component: specific-component
symptoms: how it manifested
root_cause: why it happened
solution: how it was fixed
prevention: how to prevent recurrence
tags: [searchable, tags]
severity: impact-level
---
```

## Escalation Paths
- **Blocked work** -> CEO unblocks or reassigns
- **Architecture concern** -> CTO reviews
- **Unresolved P1 findings** -> VP Quality escalates to CEO
- **Missing learnings** -> VP Knowledge flags to CEO
