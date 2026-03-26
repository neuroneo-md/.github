# neuroneo.md

**Open standards for learning and assessment in plain Markdown.**

We maintain two complementary open formats designed for the modern web of learning — human-readable, Git-native, and AI-native.

---

## 📦 Standards

| Format | Purpose | File | Spec |
|--------|---------|------|------|
| [**LearnMD**](https://github.com/neuroneo-md/learnmd) | Write lessons, examples, and learning paths | `.learn.md` | [SPEC.md](https://github.com/neuroneo-md/learnmd/blob/main/SPEC.md) |
| [**QuizMD**](https://github.com/neuroneo-md/quizmd) | Write quizzes, assessments, and certifications | `.quiz.md` | [SPEC.md](https://github.com/neuroneo-md/quizmd/blob/main/SPEC.md) |

Both formats are valid Markdown — readable in any editor, versionable in any repository, playable in any compatible player. MIT licensed.

---

## 🌐 Platform

[**neuroneo.md**](https://www.neuroneo.md) is the reference implementation and community platform built on top of these standards. It provides a hosted player, a community catalogue, and an MCP server to integrate both formats into AI assistants.

The standards are open and independent — anyone can build their own implementation.

---

## ⚡ Quick start

**Play a quiz in your AI assistant** — add the neuroneo MCP server to Claude Desktop or Cursor:

```json
{
  "mcpServers": {
    "neuroneo": {
      "command": "npx",
      "args": ["-y", "mcp-remote", "https://api.neuroneo.md/mcp/"]
    }
  }
}
```

**Write a lesson:**

```markdown
---
lang: en
tags: [python]
estimated_time: 10min
---

# Python Variables

A variable is a named reference to a value in memory.

```quiz
? What operator assigns a value in Python?
- [x] =
- [ ] ==
```
```

**Write a quiz:**

```markdown
# Capital cities

## Q1 · Capital of France?

- [ ] London
- [x] Paris
- [ ] Berlin

> Paris has been the capital since the 10th century.
```

---

## 🤝 Contributing

Both specs are open for contributions — proposals, samples, test cases, and implementations are welcome.
See [CONTRIBUTING.md](https://github.com/neuroneo-md/quizmd/blob/main/CONTRIBUTING.md) in each repo.
