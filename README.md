# Awesome-AI-Context-Memory

# Awesome-AI-Context-Memory

# Top AI Context Memory Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Persistent Memory, Context Window Optimization & Session Continuity for AI Agents*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **AI Context & Memory**. These tools give AI agents the ability to remember user preferences, retain session state, and optimize context windows—preventing "context rot" where models degrade under the weight of accumulated history, tool outputs, and noise.

**Examples** include LangSmith, GitHub Copilot Enterprise, Mem0, Zep, Langfuse, Arize Phoenix, Pinecone, Weaviate, Qdrant, and Chroma (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, session persistence, and open memory layers—ideal for AI engineers, platform teams, and developers seeking transparent, vendor-independent agent memory infrastructure.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Mem0 Platform](https://mem0.ai/)**  
  Managed memory layer for AI agents with **+26% accuracy over OpenAI Memory** on the LOCOMO benchmark, **91% faster responses**, and **90% fewer tokens** than full-context approaches . Features **multi-level memory** (User, Session, Agent state), **entity linking** across memories, **multi-signal retrieval** (semantic, BM25 keyword, entity matching), and **temporal reasoning** for queries about current state, past events, and upcoming plans . Hosted platform for zero-ops production use.

- **[Zep Cloud](https://www.getzep.com/)**  
  Managed agent memory platform with **Fact Extraction** (automatically build fact tables from conversations), **Dialog Classification** (classify chat dialog for intent and emotion), and **Structured Data Extraction** (extract business data using schema you define) . Persists and recalls chat histories, automatically generates summaries, and embeds messages for relevant context retrieval—all asynchronously . Agent plugins for Claude Code, Codex, and Cursor available .

- **[LangSmith](https://smith.langchain.com/)**  
  LangChain's observability and evaluation platform with detailed tracing of every LLM call, chain execution, and agent step—showing inputs, outputs, latency, token usage, and cost. **Free Developer plan** (1 seat, 5k base traces/month), **Plus at $39/seat/month** .

- **[GitHub Copilot Enterprise](https://github.com/features/copilot)**  
  Enterprise AI coding assistant with repository-wide context awareness, custom knowledge bases, and organizational memory.

- **[Langfuse](https://langfuse.com/)**  
  Open-source LLM engineering platform with tracing, evaluations, prompt management, and datasets. **35,000+ GitHub stars**. Self-hostable. **Acquired by ClickHouse in January 2026 with commitment to keep it open source** .

- **[Arize Phoenix](https://phoenix.arize.com/)**  
  Open-source LLM observability platform built on OpenTelemetry and OpenInference. **2.5M+ monthly downloads**, **10,800+ GitHub stars**. Strong RAG debugging with nested spans .

- **[Pinecone](https://www.pinecone.io/)**  
  Managed vector database for AI applications. Features serverless architecture, metadata filtering, and hybrid search.

- **[Weaviate](https://weaviate.io/)**  
  Open-source vector database with hybrid search and automatic vectorization modules.

- **[Qdrant](https://qdrant.tech/)**  
  Rust-based vector search engine with filtered ANN and payload filtering.

- **[Chroma](https://www.trychroma.com/)**  
  Developer-favorite embedding database for local development and prototyping.

## Open-Source GitHub Projects

- **[context-mode](https://github.com/mksglu/context-mode)**  
  **The most comprehensive open-source context optimization framework for AI coding agents** (23k GitHub stars, 2k forks) . **98% reduction** in tool output through sandboxed code execution—agents write code that processes data inside the sandbox, and only results enter the context window . Features **session persistence across compaction**: PreCompact hook builds a priority-tiered XML snapshot (≤2 KB) with critical state (active files, tasks, rules, decisions), stored in SQLite and restored at SessionStart . **17 platforms supported** including Claude Code, Gemini CLI, VS Code Copilot, OpenCode, Codex CLI, Cursor, and more . **Think in Code** reports show 99.4% context savings—536 KB processed, only 3.2 KB entered context window .

- **[Mem0](https://github.com/mem0ai/mem0)**  
  **Universal memory layer for AI Agents** (open-source, Apache-2.0) . **92.5 on LoCoMo** (+21 points over previous algorithm), **94.4 on LongMemEval** (+27 points), **64.1 on BEAM (1M)** for production-scale memory at 1M tokens . Features **multi-level memory** (User, Session, Agent), **entity linking** across memories, **multi-signal retrieval** (semantic + BM25 + entity), **temporal reasoning** for time-aware queries, and **MCP support** for Claude Code, Cursor, and other agents . Library (`pip install mem0ai`), self-hosted server (`docker compose up`), or managed cloud .

- **[Zep Community Edition (Legacy)](https://github.com/getzep/zep)**  
  **Deprecated but historically significant**—the original open-source Zep Community Edition has been moved to `legacy/` and is no longer supported . **Zep Cloud is now the managed offering**. The `zep-js` SDK on the `oss` branch remains compatible with the open-source edition for those maintaining legacy deployments .

- **[engrim](https://pypi.org/project/engrim/)**  
  **Cross-platform persistent memory for AI coding agents** (open-source). Features **hybrid ranking** (semantic + keyword), **provenance tracking** (`origin_agent` field records which agent created each memory), and **MCP server** with core tools: `engrim_recall`, `engrim_add`, `engrim_context`, `engrim_review` . **Works across Google Antigravity, Claude Code, Cursor, Windsurf, Codex CLI, and GitHub Copilot CLI** . `engrim doctor` runs comprehensive health diagnostics across SQLite, semantic engine, and hooks . **Token efficiency**: 90% reduction at 100 sessions (~6,960 tokens → ~670 tokens) .

- **[graymatter](https://github.com/angelnicolasc/graymatter)**  
  **Memory and knowledge graph layer for AI coding agents** (open-source, Go). Features **seven memory tools** live via MCP, **knowledge graph rendering** (`graymatter kg render --out kg-graph.html`), and **consolidation** for long-term memory management . **Token efficiency**: 71% reduction at 30 sessions, 90% reduction at 100 sessions . Pre-built binaries for Linux, macOS, and Windows. Homebrew, Scoop, and Nix packages available.

- **[TurboAgent](https://pypi.org/project/turboagent-ai/)**  
  **TurboQuant-powered agentic AI framework for long-context LLMs on consumer hardware** (open-source, MIT). Brings Google Research's **TurboQuant KV-cache compression** to open-source LLMs—**6x+ memory reduction** and **up to 8x attention speedup** with zero measurable accuracy loss . Enables **32k-1M+ effective context on a single RTX 4090**. Features **hardware-aware auto-tuning**, **persistent multi-turn memory**, **RAG with vector-search**, and **multi-agent swarms** .

- **[montycat](https://pub.dev/packages/montycat)**  
  **Self-hosted NoSQL + vector database in one Rust-powered engine** (open-source). Positioned as **Pinecone/Weaviate/Chroma/Qdrant alternative** with a NoSQL store built in . Features **on-device embeddings** (no OpenAI bill, no data egress), **hybrid search** (semantic kNN + BM25 keyword + reciprocal-rank fusion), and **bring-your-own-vectors** for migrations from OpenAI, Pinecone, Qdrant, or Milvus pipelines . Native Dart & Flutter support for mobile, web, and desktop .

### Additional Strong Open-Source Options

- **[LangChain Deep Agents](https://github.com/langchain-ai/deepagents)** — Open-source agent harness with **middleware for context engineering**: offloading (large tool results to filesystem), summarization (condensing older messages), skills (load when relevant), subagents (noisy work in separate context), and long-term memory (persist across conversations) .
- **[OpenMemory MCP](https://github.com/mem0ai/mem0)** — Local and secure memory management via MCP, part of the Mem0 ecosystem .
- **[Zep Cloud Integrations](https://github.com/getzep/zep)** — Framework integrations for Google ADK, Microsoft Agent Framework, AutoGen, CrewAI, LangGraph, LiveKit, Pydantic AI, Strands Agents, and TypeScript frameworks (Google ADK, Mastra, Vercel AI SDK) .
- Community **n8n** workflows for memory alert routing and agent session monitoring.

**Frameworks for building custom systems**: Combine **context-mode** for context window optimization and session persistence with **Mem0** for long-term agent memory, **Zep Cloud** for fact extraction and dialog classification, **montycat** for self-hosted vector storage, and **PostgreSQL/SQLite** for persistence—creating a fully self-hosted, enterprise-grade AI context and memory platform.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- AI memory systems handling conversation history and user preferences must comply with data protection regulations (GDPR, CCPA, etc.) and provide appropriate retention controls.
- **Context rot is the fundamental problem.** As agents take on longer tasks, they accumulate more information—instructions, tool results, files—until context windows overflow and reasoning accuracy degrades . **Context engineering techniques fall into two categories**: preventing unnecessary information from entering the context window, and managing/filtering what's already there .
- **Open-source context optimization is mature and production-ready.** context-mode achieves **98% reduction in tool output** through sandboxed code execution . Mem0 delivers **92.5 on LoCoMO** and **94.4 on LongMemEval** with open-source code and reproducible evaluations . **These are genuine alternatives to commercial platforms.**
- **Session persistence across compaction is critical for coding agents.** When context windows compact, agents lose working state—active files, tasks, decisions, and user corrections. context-mode's PreCompact hook builds a priority-tiered snapshot (≤2 KB) with critical state preserved and lower-priority events dropped first . **Without session persistence, agents ask "what were we doing?" after every compaction.**
- **Token efficiency compounds over sessions.** engrim demonstrates **90% reduction at 100 sessions** (~6,960 tokens → ~670 tokens) . GrayMatter shows **71% reduction at 30 sessions** . **Every session without memory management adds permanent context weight.**
- Self-hosted open-source solutions require proper security hardening, memory pruning policies, and ongoing maintenance. **Agent memory is a privacy-sensitive data store**—access controls and retention limits are essential.

---

**Made for AI engineers, platform teams, and developers building transparent agent memory solutions.**  
Let's make AI Context & Memory more open, data-driven, and context-efficient.
