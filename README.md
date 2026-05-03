# 📦 Context Sandbox — 99.2% AI Context Compression

> **From 35,889 tokens to 298. Unlock unlimited conversation history.**

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.9%2B-brightgreen)](https://python.org)

Context Sandbox is a **tool output compression engine** that reduces agent context usage by 99.2%. Instead of loading raw tool outputs into every LLM call, Context Sandbox stores them in an FTS5-indexed sandbox and retrieves only what's needed — when it's needed.

---

## ✨ Features

- **99.2% Compression** — Full tool outputs (35,889 tokens) → compressed summary (298 tokens)
- **FTS5 Full-Text Search** — SQLite-powered semantic retrieval across sessions
- **"Think in Code" Paradigm** — Let AI analyze programmatically instead of loading raw data
- **Session Continuity** — No more "I forgot what we did 3 turns ago"
- **Tool Output Caching** — Each unique output is stored once, referenced by hash

## 📦 Installation

```bash
git clone https://github.com/Youan-ai/Context-Sandbox.git
cd context-sandbox
```

## 🚀 Quick Start

```python
from sandbox import ContextSandbox

sandbox = ContextSandbox()

# Instead of loading 35K tokens into context:
summary = sandbox.compress(large_tool_output)
# → Returns 298 tokens with FTS5 index for retrieval

# Later, search across all compressed outputs
results = sandbox.search("What was that Python function?")
# Found instantly, no context waste
```

## 🏗️ Architecture

```
┌────────────────────────────────────────┐
│           Context Sandbox               │
├──────────────┬─────────────────────────┤
│ Compression   │ FTS5 Index              │
├──────────────┼─────────────────────────┤
│ hash dedup   │ SQLite full-text search  │
│ strip noise  │ cross-session retrieval  │
│ summarize    │ relevant snippets only   │
└──────────────┴─────────────────────────┘
```

## 📚 API Overview

| Method | Description |
|--------|-------------|
| `compress(output)` | Compress tool output to ~298 tokens |
| `search(query)` | FTS5 search across all stored contexts |
| `get_stats()` | Compression ratio, storage usage |
| `clear_session(sid)` | Clear context for a specific session |

## 🤝 Contributing

Less context, more intelligence. Contributions welcome.

## 📄 License

Apache 2.0 — see [LICENSE](LICENSE).
