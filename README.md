# Context-Sandbox

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://python.org)

An intelligent context optimization sandbox that reduces tool output by over 99%. Uses FTS5 full-text search to maintain session continuity through the 'Think in Code' paradigm.

智能上下文优化沙盒，将工具输出压缩99%以上。通过FTS5全文搜索和"用代码思考"范式维护会话连续性。

## Quick Start

```bash
pip install context-sandbox
from sandbox import ContextSandbox
sandbox = ContextSandbox()
sandbox.optimize(tool_output)
```

## Core API

- `ContextSandbox()` - Initialize the context sandbox
- `.optimize(data)` - Compress tool output by 99%+
- `.search(query)` - FTS5 full-text search across compressed context
- `.continuity_check()` - Ensure session continuity between turns

## Features

- 📦 **99%+ Compression** - Radical tool output reduction
- 🔍 **FTS5 Search** - Full-text search on compressed data
- 🔄 **Session Continuity** - Maintain context across overflow events
- 💡 **Think in Code** - Let AI analyze with code, not raw data

## License

Apache 2.0
