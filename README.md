# Awesome Agent Evals [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of evaluation resources for AI agents — platforms, open-source frameworks, benchmarks, and methodology.

Strong evals are what separate a viral demo from a production agent. The compounding nature of tool calls makes agent evaluation fundamentally harder than single-turn LLM eval, and the ecosystem is fragmenting fast. This list aims to be a *tightly curated* — not exhaustive — entry point.

## Contents

- [Evaluation Platforms](#evaluation-platforms)
- [Open-Source Eval Libraries](#open-source-eval-libraries)
- [Agent Benchmarks](#agent-benchmarks)
  - [Coding Agents](#coding-agents)
  - [Web / Browser Agents](#web--browser-agents)
  - [Computer-Use / OS Agents](#computer-use--os-agents)
  - [Tool-Use & Function-Calling](#tool-use--function-calling)
  - [Conversational / Customer-Service Agents](#conversational--customer-service-agents)
  - [Research / Deep-Research Agents](#research--deep-research-agents)
  - [General / Multi-Domain](#general--multi-domain)
- [Reading & Methodology](#reading--methodology)
- [Related Lists](#related-lists)
- [Contributing](#contributing)
- [License](#license)

## Evaluation Platforms

Hosted platforms (some with open-source cores) that explicitly target agent trajectories, not just LLM calls.

- [AgentOps](https://github.com/AgentOps-AI/agentops) — Agent-specific tracing + replay + cost/quality eval.
- [LangSmith](https://www.langchain.com/langsmith) — Datasets + LLM-as-judge eval over agent traces; tight LangGraph integration.
- [Langfuse](https://github.com/langfuse/langfuse) — Open-source counterpart with agent-trace observability (MIT).
- [Braintrust](https://www.braintrust.dev/) — Eval-first dev loop with strong agent-trajectory dataset UX.

## Open-Source Eval Libraries

Code-first frameworks built for agent evaluation, drop into a repo and run in CI.

- [Harbor](https://github.com/harbor-framework/harbor) — Containerized agent-eval framework; runs trials at scale across cloud providers (Daytona, Modal). Hosts the Terminal-Bench 2.0 registry.
- [Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai) — UK AISI's eval framework; the de-facto choice for frontier-model agent evals (tool use, multi-step tasks).
- [agentevals](https://github.com/langchain-ai/agentevals) — Ready-made trajectory evaluators for agents.
- [AWS Agent Evaluation](https://github.com/awslabs/agent-evaluation) — Generative-AI-powered framework for testing virtual agents.
- [Strands Evals](https://github.com/strands-agents/evals) — Multi-agent interaction analysis + automated experiment generation.
- [DeepEval](https://github.com/confident-ai/deepeval) — Pytest-style; agent-specific metrics (task completion, tool correctness).
- [RagCiteCheck](https://github.com/ppon1086/ragcitecheck) — Python CLI for evidence-stability checks across RAG/agentic retrieval runs.

## Agent Benchmarks

### Coding Agents
- [SWE-bench / SWE-bench Verified](https://www.swebench.com/) — Resolve real GitHub issues end-to-end. The standard.
- [Terminal-Bench](https://www.tbench.ai/) — Agents operating a real shell across multi-step tasks; v2 ships via Harbor.
- [LoCoBench-Agent](https://arxiv.org/abs/2511.13998) — Long-context software engineering in an interactive setting.

### Web / Browser Agents
- [WebArena](https://webarena.dev/) — Realistic self-hosted web environments (e-commerce, GitLab, Reddit clone).
- [VisualWebArena](https://jykoh.com/vwa) — Multimodal extension of WebArena.
- [BrowserGym](https://github.com/ServiceNow/BrowserGym) — Gym-style toolkit for browser agents; common substrate.
- [AgentLab](https://github.com/ServiceNow/AgentLab) — ServiceNow's dev+eval framework atop BrowserGym.
- [Mind2Web](https://github.com/OSU-NLP-Group/Mind2Web) — Generalist web agent benchmark.
- [WebVoyager](https://github.com/MinorJerry/WebVoyager) — Live-website multimodal agent eval.

### Computer-Use / OS Agents
- [OSWorld](https://os-world.github.io/) — Multimodal benchmark for desktop computer-use agents.
- [WindowsAgentArena](https://github.com/microsoft/WindowsAgentArena) — Windows-focused computer-use eval.
- [Android in the Wild (AitW)](https://github.com/google-research/google-research/tree/master/android_in_the_wild) — Mobile UI control.
- [AndroidWorld](https://github.com/google-research/android_world) — Reproducible Android benchmark.

### Tool-Use & Function-Calling
- [ToolBench](https://github.com/OpenBMB/ToolBench) — 16k+ real-world API tasks for multi-step tool-using agents.
- [MCPEval](https://arxiv.org/abs/2507.12806) — MCP-based automated task generation + deep eval for tool-using agents.

### Conversational / Customer-Service Agents
- [τ-bench / τ²-bench](https://arxiv.org/abs/2406.12045) — Sierra's go-to benchmark for conversational tool-use agents; policy-bound, dual-control.

### Research / Deep-Research Agents
- [GAIA](https://huggingface.co/datasets/gaia-benchmark/GAIA) — General-assistant benchmark; multi-step research with tools.
- [BrowseComp](https://openai.com/index/browsecomp/) — Hard browsing/research questions for autonomous browsing agents.

### General / Multi-Domain
- [AgentBench](https://github.com/THUDM/AgentBench) — 8 environments covering OS, DB, web, code, games.
- [AgentBoard](https://github.com/hkust-nlp/AgentBoard) — Fine-grained progress-rate metric across domains.
- [AgentQuest](https://arxiv.org/abs/2404.06411) — Modular framework for measuring agent progress.

## Reading & Methodology

- Anthropic — [Demystifying evals for AI agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents).
- Anthropic — [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents).
- [VoltAgent/awesome-ai-agent-papers](https://github.com/VoltAgent/awesome-ai-agent-papers) — recent agent papers, with an eval section.

## Related Lists

This repo focuses tightly on *agent* evaluation. For broader scope, see:

- [Vvkmnn/awesome-ai-eval](https://github.com/Vvkmnn/awesome-ai-eval) — broader "AI reliability" eval list.
- [onejune2018/Awesome-LLM-Eval](https://github.com/onejune2018/Awesome-LLM-Eval) — LLM eval (EN + 中文), widely referenced.
- [zhangxjohn/LLM-Agent-Benchmark-List](https://github.com/zhangxjohn/LLM-Agent-Benchmark-List) — benchmark-only list.
- [CSHaitao/Awesome-LLMs-as-Judges](https://github.com/CSHaitao/Awesome-LLMs-as-Judges) — LLM-as-judge survey.
- [tjunlp-lab/Awesome-LLMs-Evaluation-Papers](https://github.com/tjunlp-lab/Awesome-LLMs-Evaluation-Papers) — academic survey-driven.
- [BenchGecko/awesome-llm-benchmarks](https://github.com/BenchGecko/awesome-llm-benchmarks) — benchmarks + leaderboards.
- [ianwieds/awesome-ai-agents](https://github.com/ianwieds/awesome-ai-agents) — general agent list; its evaluation section covers benchmarks and tracing tools.

## Contributing

PRs welcome. See [CONTRIBUTING.md](CONTRIBUTING.md). Quality bar:

- **Agent-focused.** Pure LLM benchmarks belong elsewhere unless heavily used for agent eval.
- **One line per entry.** Link first, terse description after. No marketing copy.
- **Stable.** Prefer projects with active maintenance and real adoption over preprints with no code.
- **Honest.** If a tool overlaps heavily with another, note the difference rather than duplicating.

## License

[CC0 1.0 Universal](LICENSE) — Public Domain.
