---
name: bug-hunter
description: Investigate and fix bugs systematically. Use when debugging issues or tracing errors.
allowed-tools: Bash, Read, Grep, Glob
---

# Bug Hunter

**Version**: 1.0.0
**Purpose**: Systematic bug investigation and resolution

---

## Workflow

### Step 1: Reproduce

```bash
# Run failing test/command
npm test
```

Document:
- Expected behavior
- Actual behavior
- Error message

### Step 2: Locate

```bash
# Search for error
grep -r "error message" src/
```

### Step 3: Trace

1. Find error origin
2. Trace call stack
3. Identify root cause

### Step 4: Fix

1. Write failing test
2. Implement fix
3. Verify test passes

### Step 5: Document

```markdown
## Bug Fix Report

**Issue**: [Description]
**Root Cause**: [Explanation]
**Fix**: [What was changed]
**Test**: [How to verify]
```

---

## Tips

- Check recent commits: `git log --oneline -20`
- Look for similar issues: `git log --grep="bug"`
- Binary search: `git bisect`
