# Compound Engineering Co.

An Agent Companies package that implements [Compound Engineering](https://github.com/EveryInc/compound-engineering-plugin) as a portable AI company, focused on agent-native architecture.

Built for [Paperclip](https://paperclip.ing) using the [Agent Companies](https://agentcompanies.io) protocol.

## What This Is

A ready-to-import company package that organizes 20 AI agents into a structured engineering org running the **Plan → Work → Review → Compound** loop. Every sprint makes the next one easier.

This is not a generic template. Every agent has specific operational instructions derived from the Compound Engineering plugin's 29 specialized agents. The org chart encodes the workflow loop itself.

## Quick Start

```bash
# Import into Paperclip
npx paperclip-ai onboard
# Then import this directory as a company package
```

## Org Chart

```
CEO (Compound Loop Orchestrator)
├── CTO (Architecture Guardian)
│   ├── Lead Researcher
│   │   ├── Repo Research Analyst
│   │   ├── Best Practices Researcher
│   │   ├── Framework Docs Researcher
│   │   ├── Git History Analyzer
│   │   ├── Learnings Researcher
│   │   └── Spec Flow Analyzer
│   └── Lead Designer
│       ├── Design Implementation Reviewer
│       ├── Design Iterator
│       └── Figma Design Sync
├── VP Engineering (Work Phase)
│   ├── Bug Reproduction Validator
│   └── PR Comment Resolver
├── VP Quality (Review Phase)
│   ├── Architecture Strategist
│   ├── Security Sentinel
│   ├── Performance Oracle
│   ├── Code Simplicity Reviewer
│   ├── Pattern Recognition Specialist
│   ├── Data Integrity Guardian
│   ├── Agent-Native Reviewer
│   └── Schema Drift Detector
└── VP Knowledge (Compound Phase)
    ├── Learnings Researcher
    └── Style Editor
```

## The Compound Loop

All work flows through four phases:

| Phase | Owner | What Happens |
|-------|-------|-------------|
| **Plan** | CEO + Lead Researcher | Research codebase, check institutional learnings, design approach |
| **Work** | VP Engineering | Execute plan with atomic commits and verification |
| **Review** | VP Quality | Multi-agent audit (security, performance, architecture, agent-native) |
| **Compound** | VP Knowledge | Capture learnings so the next cycle is easier |

## Agent-Native Architecture

The `agent-native-reviewer` enforces four principles on every PR:

1. **Parity** — Whatever a user can do, an agent can do through tools
2. **Granularity** — Atomic primitives, not workflow bundles
3. **Composability** — New features = new prompts, not new code
4. **Emergent Capability** — Agents can solve problems you didn't design for

## Package Contents

| Component | Count |
|-----------|-------|
| Company manifest | 1 |
| Teams | 7 |
| Agents | 20 |
| Projects | 3 |
| Recurring tasks | 8 |
| Skills (referenced) | 11 |
| Reference docs | 3 |

## Model Strategy

| Tier | Model | Roles |
|------|-------|-------|
| Frontier | Opus | CEO, CTO — judgment and architecture |
| Standard | Sonnet | VPs, Leads, specialized reviewers — depth |
| Volume | Haiku | Research agents, simple reviewers — speed |

Configured in `.paperclip.yaml` with per-agent budgets and approval gates.

## Skills

Skills reference the upstream [Compound Engineering plugin](https://github.com/EveryInc/compound-engineering-plugin) via `metadata.sources`:

- `ce:plan` — Implementation planning with research
- `ce:work` — Execution with atomic commits
- `ce:review` — Multi-agent code review
- `ce:compound` — Knowledge capture
- `ce:brainstorm` — Requirements exploration
- `agent-native-architecture` — Agent-native design principles
- `orchestrating-swarms` — Parallel agent dispatch
- `document-review` — Plan/spec review
- `frontend-design` — Production-grade UI
- `agent-browser` — Browser automation
- `setup` — Review pipeline configuration

## Recurring Tasks

| Task | Assignee | Schedule |
|------|----------|----------|
| Daily Standup | CEO | Daily 9am CT |
| Code Review Sweep | VP Quality | Daily 2pm CT |
| Knowledge Capture | VP Knowledge | Daily 5pm CT |
| Plan Sprint | CEO | Monday 10am CT |
| Research Scan | Lead Researcher | Monday 8am CT |
| Agent-Native Audit | CTO | Monday 1pm CT |
| Design Sync | Lead Designer | Wednesday 10am CT |
| Weekly Compound Review | VP Knowledge | Friday 4pm CT |

## Protocol

This package follows the [Agent Companies v1](https://agentcompanies.io) specification:

- `COMPANY.md` — Root organization definition
- `TEAM.md` — Team structures with manager and member references
- `AGENTS.md` — Individual agent roles with skills and reporting lines
- `PROJECT.md` — Work groupings
- `TASK.md` — Portable starter tasks with schedules
- `SKILL.md` — Referenced capability packages
- `.paperclip.yaml` — Paperclip runtime configuration (optional)

## License

MIT
