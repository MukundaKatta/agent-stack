# agent-stack

> Six small, single-concern reliability libraries for production LLM agents — TypeScript, Python, and MCP servers. Zero runtime dependencies. Adopt one or all.

[![Zenodo DOI](https://img.shields.io/badge/Zenodo%20DOI-10.5281%2Fzenodo.20074702-D4A853?style=flat-square&labelColor=1a1a1a)](https://doi.org/10.5281/zenodo.20074702)
[![HF DOI](https://img.shields.io/badge/HF%20DOI-10.57967%2Fhf%2F8720-D4A853?style=flat-square&labelColor=1a1a1a)](https://doi.org/10.57967/hf/8720)
[![License](https://img.shields.io/badge/License-MIT-D4A853?style=flat-square&labelColor=1a1a1a)](#license)
[![Live demo](https://img.shields.io/badge/🤗%20Try%20it%20live-D4A853?style=flat-square&labelColor=1a1a1a)](https://huggingface.co/spaces/mukunda1729/agent-stack-demo)

**Landing page:** https://mukundakatta.github.io/agent-stack/
**Paper:** [Six Reliability Primitives for LLM Agents: An Artifact Pattern for Stackable, Single-Concern Libraries](https://doi.org/10.5281/zenodo.20074702)
**HuggingFace Hub:** [mukunda1729/agent-stack](https://huggingface.co/mukunda1729/agent-stack)

## The six primitives

| Library | Concern |
| --- | --- |
| **AgentFit** | Token-aware context-window fitting |
| **AgentGuard** | Network egress allowlist for tool calls |
| **AgentSnap** | Snapshot tests for tool-call traces |
| **AgentVet** | Tool-arg validation with retry hints |
| **AgentCast** | Structured-output validate-and-retry for LLM JSON |
| **AgentBudget** | Per-run token + dollar caps |

Each ships in three forms: TypeScript on npm, Python on PyPI, MCP-server variant.

## Install

```bash
# TypeScript
npm i @mukundakatta/agentfit @mukundakatta/agentguard @mukundakatta/agentsnap \
       @mukundakatta/agentvet @mukundakatta/agentcast @mukundakatta/agentbudget

# Python
pip install agentfit agentguard agentsnap agentvet agentcast agentbudget
```

```json
// MCP server (Claude Desktop config)
{
  "mcpServers": {
    "agentvet": { "command": "npx", "args": ["-y", "@mukundakatta/agentvet-mcp"] },
    "agentguard": { "command": "npx", "args": ["-y", "@mukundakatta/agentguard-mcp"] }
  }
}
```

## Read more

- 📖 [Medium](https://medium.com/@mukunda.vjcs6/six-reliability-primitives-for-llm-agents-5fc1dfa33d93)
- ⚙️ [dev.to](https://dev.to/mukundakatta/six-reliability-primitives-for-llm-agents-m13)
- ✍️ [Hashnode](https://mukundakatta.hashnode.dev/six-reliability-primitives-for-llm-agents)
- 📝 [Paper (Zenodo)](https://doi.org/10.5281/zenodo.20074702)

## Find them all

GitHub topic search across the family: [`topic:agent-stack` on user MukundaKatta](https://github.com/search?q=user%3AMukundaKatta+topic%3Aagent-stack) — 24 repos pinned.

## Citation

```bibtex
@misc{katta2026agentstack,
  author    = {Katta, Mukunda Rao},
  title     = {Six Reliability Primitives for LLM Agents:
               An Artifact Pattern for Stackable, Single-Concern Libraries},
  year      = {2026},
  publisher = {Zenodo},
  doi       = {10.5281/zenodo.20074702},
  url       = {https://doi.org/10.5281/zenodo.20074702}
}
```

## Local dev

To preview the landing page locally:

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## License

MIT.
