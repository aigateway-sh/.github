<div align="center">

# AIgateway

**One OpenAI-compatible endpoint to every frontier model — text, image, video, voice, audio, embeddings.**

[![Website](https://img.shields.io/badge/web-aigateway.sh-000)](https://aigateway.sh)
[![Docs](https://img.shields.io/badge/docs-aigateway.sh%2Fdocs-000)](https://aigateway.sh/docs)
[![Status](https://img.shields.io/badge/status-live-16a34a)](https://aigateway.sh/status)
[![License](https://img.shields.io/badge/license-MIT-blue)](https://opensource.org/licenses/MIT)

</div>

---

## What this is

A single API that gives you **150+ models across 44 labs** — Anthropic, OpenAI, Google, Moonshot, Meta, Mistral, DeepSeek, Black Forest Labs, Stability, Deepgram, ElevenLabs, Runway, and more — behind one key and one OpenAI-compatible endpoint.

```bash
curl https://api.aigateway.sh/v1/chat/completions \
  -H "Authorization: Bearer sk-aig-..." \
  -d '{"model":"anthropic/claude-opus-4.7","messages":[{"role":"user","content":"hi"}]}'
```

No code rewrite. Drop-in for the `openai` SDK. Pay **cost + 5%** — no markup games.

## Repos in this org

| Repo | What it is |
|---|---|
| [**cli**](https://github.com/aigateway-sh/cli) | `aig` — call any model, mint keys, run evals, tail traffic from your terminal. [npm · `aigateway-cli`](https://www.npmjs.com/package/aigateway-cli) |
| [**sdk-node**](https://github.com/aigateway-sh/sdk-node) | TypeScript SDK for async jobs, sub-accounts, evals, replays, webhooks. [npm · `aigateway-js`](https://www.npmjs.com/package/aigateway-js) |
| [**sdk-python**](https://github.com/aigateway-sh/sdk-python) | Python SDK — same surface. [PyPI · `aigateway-py`](https://pypi.org/project/aigateway-py/) |
| [**examples**](https://github.com/aigateway-sh/examples) | Runnable code — chat, embeddings, image, voice, multimodal agents. One-click Vercel deploys. |
| [**mcp-server**](https://github.com/aigateway-sh/mcp-server) | Reference Model Context Protocol server. Hosted mirror at `api.aigateway.sh/mcp`. |
| [**openapi**](https://github.com/aigateway-sh/openapi) | Canonical OpenAPI 3.1 spec. Generate clients, import to Postman, feed to agents. |
| [**llms-txt**](https://github.com/aigateway-sh/llms-txt) | `llms.txt`, `llms-full.txt`, `agents.md` — the capability map agents can self-configure against. |
| [**awesome-ai-gateway**](https://github.com/aigateway-sh/awesome-ai-gateway) | Curated list of integrations, agents, frameworks, and community projects. |

## 30-second start

```bash
pip install aigateway-py
pnpm add aigateway-js
npm i -g aigateway-cli && aig init
```

Or keep the OpenAI SDK you already have — just change the base URL:

```python
from openai import OpenAI
client = OpenAI(
    base_url="https://api.aigateway.sh/v1",
    api_key="sk-aig-...",
)
```

Get a key at [aigateway.sh/signin](https://aigateway.sh/signin) — free tier included.

## For coding agents

Point your agent at our capability map and it will self-configure:

```
https://aigateway.sh/llms.txt        → short capability map
https://aigateway.sh/llms-full.txt   → full model catalog with pricing
https://aigateway.sh/agents.md       → agent onboarding guide
https://aigateway.sh/openapi.json    → OpenAPI 3.1 spec
https://api.aigateway.sh/mcp         → MCP (Streamable HTTP)
https://api.aigateway.sh/mcp/sse     → MCP (SSE, legacy)
```

Works out of the box with Claude Code, Cursor, Cline, Aider, Continue.dev, OpenClaw, Mastra, LangChain, LlamaIndex, Vercel AI SDK, n8n, LiteLLM, and Promptfoo.

## Why AIgateway

- **No per-provider dance.** One key replaces 10+ accounts.
- **Failover built in.** If one provider dies, we route around it.
- **Sub-accounts per customer.** Mint scoped keys with spend caps and tags in one API call.
- **Evals, replays, job primitives.** Things the OpenAI SDK doesn't model but production needs.
- **MCP-native.** Every primitive is callable from any MCP-aware agent.
- **Cost + 5%.** Transparent pricing. No tier games.

## Support

- Issues → open one on the relevant repo
- Security → [security@aigateway.sh](mailto:security@aigateway.sh)
- General → [support@aigateway.sh](mailto:support@aigateway.sh) · [aigateway.sh/support](https://aigateway.sh/support)

## Follow

[github.com/aigateway-sh](https://github.com/aigateway-sh) · [x.com/buildwithrakesh](https://x.com/buildwithrakesh) · [linkedin.com/in/rakeshroushan1002](https://www.linkedin.com/in/rakeshroushan1002/)

---

<sub>MIT licensed across the org. Made with care by one engineer on Cloudflare Workers in San Francisco.</sub>
