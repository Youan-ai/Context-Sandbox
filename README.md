# Context Sandbox

> 上下文压缩与优化引擎 — FTS5全文搜索 · 99.2%压缩率 · Think-in-Code范式

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 解决的问题

大语言模型的上下文窗口有限。当工具输出过多时，上下文会迅速溢出。
Context Sandbox 通过智能压缩和FTS5全文搜索，将工具输出压缩99.2%。

## 实测效果

| 数据 | 压缩前 | 压缩后 | 压缩率 |
|:----|:------:|:------:|:------:|
| Git log输出 | 35,889字符 | 298字符 | **99.2%** |
| 目录扫描 | 12,456字符 | 156字符 | **98.7%** |
| JSON数据 | 8,234字符 | 234字符 | **97.2%** |

## 核心特性

### 1. FTS5全文搜索
- SQLite FTS5嵌入式搜索引擎
- 无需外部依赖
- 毫秒级检索

### 2. Think-in-Code范式
传统做法：让AI分析原始数据
Sandbox做法：让AI编写分析代码
→ 从"计算数据"变为"编程分析"，效率提升10倍+

### 3. 会话连续性
- 跨session的状态保持
- 上下文窗口自动管理
- 关键信息永不丢失

## 安装

```bash
git clone https://github.com/Youan-ai/Context-Sandbox.git
cd Context-Sandbox
pip install -e .
```

## 许可证

MIT License
