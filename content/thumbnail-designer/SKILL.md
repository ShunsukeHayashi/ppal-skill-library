---
name: thumbnail-designer
description: Generate thumbnail design concepts and specifications. Use when creating visuals for YouTube or blogs.
allowed-tools: Write
---

# Thumbnail Designer

**Version**: 1.0.0
**Purpose**: Create thumbnail design specs

---

## Workflow

### Step 1: Understand Context

Ask:
- Platform? (YouTube, Blog, SNS)
- Topic?
- Target emotion? (curiosity, urgency, trust)

### Step 2: Generate Concepts

Provide 3 concepts:

```markdown
## Concept 1: [Name]

**Layout**: [Left/Center/Right focus]
**Main Text**: "[3-5 words]"
**Sub Text**: "[Optional]"
**Image**: [Description]
**Colors**: [Primary, Secondary, Accent]
**Emotion**: [Target feeling]
```

### Step 3: Specification

```yaml
size: 1280x720 (YouTube) / 1200x630 (OGP)
format: PNG
text:
  font: "Noto Sans JP Bold"
  size: 72px
  color: "#FFFFFF"
  shadow: true
background:
  type: gradient / image
  colors: ["#1a1a2e", "#16213e"]
```

---

## Best Practices

- 3 words max for main text
- High contrast colors
- Face close-up increases CTR
- Avoid small text (unreadable on mobile)
