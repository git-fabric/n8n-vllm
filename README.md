<p align="center"><img src="docs/banner.svg" alt="n8n-vllm: n8n-Ops: Ollama model specialized for n8n REST API v1" width="100%"></p>

# n8n-vllm

**n8n-Ops**: an Ollama model specialized for the **n8n REST API v1**, part of git-fabric's **fabric-llm** layer (`L5+L6+L7`).

It answers questions about its domain locally, so the fabric only escalates to Claude when it has to. See [fabric-sdk](https://github.com/git-fabric/sdk) for how requests are routed.

| | |
|---|---|
| Base model | `qwen2.5:14b` |
| Context window | 8,192 tokens |
| Temperature | 0.15 |

## Use it

```bash
ollama create n8n-ops -f Modelfile
ollama run n8n-ops
```

## What's inside

A single [`Modelfile`](Modelfile): the base model, its sampling parameters, and a system prompt that teaches the model the n8n REST API v1.

<!-- org-footer -->
---

<p align="center"><sub>Part of <a href="https://github.com/git-fabric">git-fabric</a> · composable fabric apps for Git-native infrastructure · built by <a href="https://github.com/ry-ops">ry-ops</a></sub></p>
