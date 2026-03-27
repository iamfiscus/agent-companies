---
name: Knowledge Capture
description: VP Knowledge runs ce:compound on all recently completed tasks to capture learnings before they are lost.
slug: knowledge-capture
assignee: vp-knowledge
project: compound-loop
schedule:
  timezone: America/Chicago
  startsAt: "2026-03-27T17:00:00-05:00"
  recurrence: daily
---

Every day at end-of-day:

1. Review all tasks marked complete since last capture
2. For each: did it involve a non-trivial problem?
3. If yes, run `ce:compound` to extract and document the learning
4. Verify solution doc includes: module, symptoms, root cause, solution, prevention
5. Check for duplicates against existing solutions
