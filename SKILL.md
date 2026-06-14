---
name: api-cost-compare
description: Compare LLM API pricing across Anthropic, OpenAI, DeepSeek, Google, OpenRouter, Mistral, and 10+ providers. Sort by cost, filter by capability, and find the cheapest model for any task. 40+ models tracked.
version: 1.2.0
author: minirr890112-byte
license: MIT
metadata:
  hermes:
    tags: [API, Pricing, LLM, Cost-Comparison, OpenAI, Anthropic, DeepSeek, Budget]
    homepage: https://github.com/minirr890112-byte/api-cost-compare
---

# api-cost-compare

## Problem → Solution

**The problem**: You need to pick an LLM for your project. OpenAI says $2/M, Anthropic says $3/M, DeepSeek says $0.27/M — but which one actually fits your task? You open 6 browser tabs, each with a different pricing page, and try to mental-math the comparison. You guess. You overspend.

**The solution**: One command compares 40+ models across all major providers. Sort by cost, filter by capability (coding/reasoning/chat), see context windows — all in a clean terminal table. No more guesswork.

## Quick Start

```bash
pip install git+https://github.com/minirr890112-byte/api-cost-compare.git

api-cost-compare list
api-cost-compare compare gpt-4.1 claude-sonnet-4 deepseek-chat
api-cost-compare cheapest --task coding
api-cost-compare filter --provider openai --context 128k
```

## Real Output

```
$ api-cost-compare list

┌────────────────────────────────────┬──────────┬─────────┬─────────┬──────┐
│ Model                              │ Provider │ In/M    │ Out/M   │ Ctx  │
├────────────────────────────────────┼──────────┼─────────┼─────────┼──────┤
│ Gemini 1.5 Flash                   │ Google   │ $0.07   │ $0.30   │ 1M   │
│ DeepSeek Chat                      │ DeepSeek │ $0.27   │ $1.10   │ 128K │
│ GPT-4.1 mini                       │ OpenAI   │ $0.40   │ $1.60   │ 1M   │
│ Claude Haiku                       │Anthropic │ $0.80   │ $4.00   │ 200K │
│ GPT-4.1                            │ OpenAI   │ $2.00   │ $8.00   │ 1M   │
│ Claude Sonnet 4                    │Anthropic │ $3.00   │ $15.00  │ 200K │
└────────────────────────────────────┴──────────┴─────────┴─────────┴──────┘
```

## Commands

| Command | Description |
|---------|-------------|
| `list` | Show all 40+ models sorted by input price |
| `compare <m1> <m2> [m3...]` | Side-by-side comparison of specific models |
| `cheapest --task <type>` | Find cheapest model for coding/reasoning/chat |
| `filter --provider X --context N` | Filter by provider and minimum context window |

---
⭐ **Star this repo if it saved you money**: [github.com/minirr890112-byte/api-cost-compare](https://github.com/minirr890112-byte/api-cost-compare)
