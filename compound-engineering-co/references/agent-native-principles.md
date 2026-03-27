# Agent-Native Architecture Principles

## The Four Principles

### 1. Parity
Whatever the user can do through the UI, the agent must be able to achieve through tools.

**Capability Map Template:**

| User Action | Agent Method | Status |
|-------------|-------------|--------|
| Create item | `write_file` or `create_item` tool | |
| Update item | `update_file` or `update_item` tool | |
| Delete item | `delete_file` or `delete_item` tool | |
| Search | `search_files` or `search` tool | |

**Test:** Pick any UI action. Can the agent accomplish it?

### 2. Granularity
Prefer atomic primitives. Features are outcomes achieved by an agent in a loop.

```
# Wrong - logic in code
Tool: classify_and_organize_files(files)

# Right - agent decides
Tools: read_file, write_file, move_file, list_directory, bash
Prompt: "Organize downloads by content and recency"
```

**Test:** To change behavior, do you edit prose or refactor code?

### 3. Composability
New features = new prompts (when tools are atomic and parity exists).

```
Prompt: "Review files modified this week. Summarize changes. Suggest three priorities."
```

No code written. Agent uses `list_files`, `read_file`, and judgment.

### 4. Emergent Capability
Agent can accomplish things you didn't explicitly design for.

Build atomic tools -> Users ask unexpected things -> Agent composes solutions -> You observe patterns -> Optimize common patterns -> Repeat.

## Anti-Patterns

| Anti-Pattern | Fix |
|-------------|-----|
| Agent as router only | Let agent act, not just route |
| Workflow-shaped tools | Break into primitives |
| Orphan UI actions | Maintain parity |
| Context starvation | Inject resources into system prompt |
| Gates without reason | Default to open, keep primitives available |
| Heuristic completion detection | Explicit completion tool |
| Static API mapping | Dynamic capability discovery |

## Architecture Review Checklist

- [ ] Agent can achieve anything users can (parity)
- [ ] Tools are atomic primitives (granularity)
- [ ] New features = new prompts (composability)
- [ ] Agent handles unexpected requests (emergent capability)
- [ ] System prompt includes resources and capabilities
- [ ] Agent and user share same data space
- [ ] Agent actions reflect immediately in UI
- [ ] Every entity has full CRUD
- [ ] Agents explicitly signal completion

**Ultimate test:** Describe an outcome in your domain that you didn't build a feature for. Can the agent figure it out?
