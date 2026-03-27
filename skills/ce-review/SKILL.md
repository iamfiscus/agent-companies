---
name: ce-review
description: "Structured multi-agent code review with tiered personas, confidence-gated findings, and merge/dedup pipeline. Use during the Review phase."
slug: ce-review
tags:
  - workflow
  - review
metadata:
  sources:
    - kind: github-dir
      repo: EveryInc/compound-engineering-plugin
      path: plugins/compound-engineering/skills/ce-review
      commit: main
      url: https://github.com/EveryInc/compound-engineering-plugin
---

Referenced from compound-engineering plugin. Launches parallel review agents, collects findings, deduplicates, and presents prioritized results.
