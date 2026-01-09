---
name: project-initializer
description: Initialize new projects with best practices. Use when starting new codebases or setting up repos.
allowed-tools: Bash, Write, Read
---

# Project Initializer

**Version**: 1.0.0
**Purpose**: Bootstrap projects with standard structure

---

## Workflow

### Step 1: Determine Project Type

Ask:
- Language/Framework? (Node.js, Python, Rust, etc.)
- Project type? (CLI, Web, Library, MCP Server)

### Step 2: Create Structure

#### Node.js/TypeScript
```bash
mkdir -p src tests docs
npm init -y
npm install -D typescript @types/node
npx tsc --init
```

#### Python
```bash
mkdir -p src tests docs
python -m venv .venv
pip install pytest black ruff
```

### Step 3: Add Standard Files

- README.md
- .gitignore
- LICENSE
- CLAUDE.md (for Claude Code)

### Step 4: Initialize Git

```bash
git init
git add .
git commit -m "Initial commit"
```

---

## Templates

### CLAUDE.md Template
```markdown
# CLAUDE.md

## Project Overview
[Description]

## Commands
- `npm run build` - Build
- `npm run test` - Test
```
