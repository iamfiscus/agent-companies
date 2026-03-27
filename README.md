# Agent Companies

A collection of portable AI company packages built on the [Agent Companies](https://agentcompanies.io) protocol for [Paperclip](https://paperclip.ing).

Each package is a self-contained company — org chart, agents, skills, projects, and recurring tasks — ready to import into Paperclip with a single URL.

## Available Companies

| Company | Agents | Description |
|---------|--------|-------------|
| [compound-engineering-co](compound-engineering-co/) | 20 | Engineering org running the Plan-Work-Review-Compound loop with agent-native architecture enforcement |

## Import into Paperclip

```
https://github.com/iamfiscus/agent-companies/tree/main/{company-name}
```

For example:
```
https://github.com/iamfiscus/agent-companies/tree/main/compound-engineering-co
```

## What's an Agent Company?

An Agent Company is a markdown-based package that describes a portable AI company:

```
company-package/
├── COMPANY.md       # Company mission and operating principles
├── teams/           # Org structure (TEAM.md per team)
├── agents/          # Individual roles (AGENTS.md per agent)
├── projects/        # Work groupings (PROJECT.md)
├── tasks/           # Recurring tasks with schedules (TASK.md)
├── skills/          # Referenced capabilities (SKILL.md)
├── references/      # Supporting documentation
└── .paperclip.yaml  # Runtime config (models, budgets, approval gates)
```

Follows the [Agent Companies v1 specification](https://agentcompanies.io/specification) — vendor-neutral, markdown-first, git-native.

## Adding a New Company

1. Create a directory at the repo root with your company name
2. Add a `COMPANY.md` with `schema: agentcompanies/v1` frontmatter
3. Build out teams, agents, projects, tasks, and skills
4. Add a `.paperclip.yaml` for runtime configuration
5. Add an entry to the table above

See [compound-engineering-co](compound-engineering-co/) for a complete example.

## License

MIT
