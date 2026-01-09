---
name: daily-reporter
description: Generate daily operation reports automatically. Use when creating EOD reports or summarizing work.
allowed-tools: Bash, Read, Write
---

# Daily Reporter

**Version**: 1.0.0
**Purpose**: Automated daily report generation

---

## Workflow

### Step 1: Gather Data

```bash
# Git activity
git log --since="yesterday" --oneline

# Todo completion
cat ~/todos.md | grep "✅"
```

### Step 2: Generate Report

```markdown
# Daily Report - [DATE]

## Summary
[1-2 sentence overview]

## Completed
- [Task 1]
- [Task 2]

## In Progress
- [Task 3]

## Blockers
- [Issue if any]

## Tomorrow
- [Next priority]
```

### Step 3: Distribute

Options:
- Save to file
- Send via Slack
- Post to Notion
- Email

---

## Automation

### cron setup
```bash
0 18 * * * ~/.claude/skills/daily-reporter/run.sh
```

### GitHub Action
```yaml
on:
  schedule:
    - cron: '0 9 * * *'
```
