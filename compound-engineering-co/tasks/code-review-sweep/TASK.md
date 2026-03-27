---
name: Code Review Sweep
description: VP Quality runs ce:review on all pending PRs using the configured review agent set.
slug: code-review-sweep
assignee: vp-quality
project: compound-loop
schedule:
  timezone: America/Chicago
  startsAt: "2026-03-27T14:00:00-05:00"
  recurrence: daily
---

Every afternoon:

1. Run `ce:review` on all open PRs
2. Activate the standard review set (architecture, security, performance, simplicity, agent-native)
3. Add extended reviewers based on change type (data changes, frontend changes)
4. Merge and deduplicate findings
5. Assign todos for each actionable finding
