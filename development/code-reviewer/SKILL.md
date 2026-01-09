---
name: code-reviewer
description: Review code for bugs, security issues, and best practices. Use when checking PRs or analyzing code quality.
allowed-tools: Read, Grep, Glob
---

# Code Reviewer

**Version**: 1.0.0
**Purpose**: Comprehensive code review

---

## Workflow

### Step 1: Gather Context

```bash
git diff main...HEAD
git log --oneline -10
```

### Step 2: Review Checklist

| Category | Check |
|----------|-------|
| **Security** | No hardcoded secrets, SQL injection, XSS |
| **Performance** | No N+1 queries, unnecessary loops |
| **Maintainability** | Clear naming, single responsibility |
| **Testing** | Test coverage, edge cases |

### Step 3: Generate Report

```markdown
## Code Review Report

### Summary
[Overall assessment]

### Issues Found
1. [Critical] ...
2. [Warning] ...

### Suggestions
- ...

### Approved: Yes/No
```

---

## Output Format

Always provide:
1. Summary (1-2 sentences)
2. Issues by severity (Critical > Warning > Info)
3. Specific line references
4. Suggested fixes with code examples
