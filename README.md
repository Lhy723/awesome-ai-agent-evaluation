# Awesome AI Agent Evaluation

![Awesome AI Agent Evaluation social preview](assets/social-preview.png)

<p align="center">
  <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome"></a>
  <a href="README.zh-CN.md">Chinese</a>
</p>

Benchmarks, eval harnesses, papers, datasets, and production checks for AI agents.

Focused on resources that make agent behavior easier to test, compare, debug, or monitor.

<table>
  <tr>
    <th>Included</th>
    <th>Left out</th>
  </tr>
  <tr>
    <td>Benchmarks with clear tasks</td>
    <td>Generic agent demos</td>
  </tr>
  <tr>
    <td>Frameworks for running evals</td>
    <td>Prompt collections without evaluation</td>
  </tr>
  <tr>
    <td>Papers with reusable methods</td>
    <td>Marketing pages with no technical detail</td>
  </tr>
</table>

## Where to start

<table>
  <tr>
    <th>If you care about...</th>
    <th>Read...</th>
  </tr>
  <tr>
    <td>Software engineering tasks</td>
    <td><a href="#coding-agent-evaluation">Coding Agent Evaluation</a></td>
  </tr>
  <tr>
    <td>Website and UI interaction</td>
    <td><a href="#browser--web-agent-evaluation">Browser / Web Agent Evaluation</a></td>
  </tr>
  <tr>
    <td>API and function calling</td>
    <td><a href="#tool-use-and-function-calling">Tool-Use and Function Calling</a></td>
  </tr>
  <tr>
    <td>Regression and recovery</td>
    <td><a href="#reliability--failure-recovery">Reliability & Failure Recovery</a></td>
  </tr>
  <tr>
    <td>Prompt injection and harmful actions</td>
    <td><a href="#safety--robustness">Safety & Robustness</a></td>
  </tr>
  <tr>
    <td>Logs, traces, cost, and drift</td>
    <td><a href="#production-monitoring">Production Monitoring</a></td>
  </tr>
</table>

## Contents

<details open>
<summary>Browse the list</summary>

- [Evaluation Basics](#evaluation-basics)
- [Benchmarks](#benchmarks)
- [Evaluation Frameworks](#evaluation-frameworks)
- [Coding Agent Evaluation](#coding-agent-evaluation)
- [Browser / Web Agent Evaluation](#browser--web-agent-evaluation)
- [Tool-Use and Function Calling](#tool-use-and-function-calling)
- [Multi-Agent Evaluation](#multi-agent-evaluation)
- [Safety & Robustness](#safety--robustness)
- [Reliability & Failure Recovery](#reliability--failure-recovery)
- [Cost, Latency, and Efficiency](#cost-latency-and-efficiency)
- [Human Evaluation Rubrics](#human-evaluation-rubrics)
- [Production Monitoring](#production-monitoring)
- [Papers](#papers)
- [Datasets](#datasets)
- [Reports & Case Studies](#reports--case-studies)
- [Related Awesome Lists](#related-awesome-lists)
- [Contributing](#contributing)

</details>

## Evaluation Basics

- [OpenAI Evals](https://github.com/openai/evals) — Open-source eval framework and registry; useful as a reference for repeatable LLM test design.
  `framework` `evals` `regression`
- [OpenAI Cookbook: Evaluating model performance](https://cookbook.openai.com/examples/evaluation/how_to_eval_abstractive_summarization) — Practical examples for turning a task into a small, inspectable eval.
  `guide` `evaluation-basics` `llm-as-judge`
- [Hamel Husain: Your AI Product Needs Evals](https://hamel.dev/blog/posts/evals/) — A good product-minded primer on why generic benchmarks are not enough.
  `guide` `product-evals` `methodology`
- [Anthropic: Building effective agents](https://www.anthropic.com/research/building-effective-agents) — Useful framing for deciding whether a workflow needs an agent at all.
  `guide` `agent-design` `methodology`
- [LangChain Agent Evals](https://docs.langchain.com/oss/python/langchain/evals) — Trajectory-level checks for tool calls, intermediate steps, and final answers.
  `guide` `agent-trajectory` `framework`
- [Phoenix LLM Evals](https://arize.com/docs/phoenix/evaluation/llm-evals) — Evaluation workflows built around traces, datasets, and experiment runs.
  `guide` `observability` `llm-as-judge`

## Benchmarks

- [SWE-bench](https://www.swebench.com/SWE-bench/) — Real GitHub issues turned into patch tasks for coding agents.
  `benchmark` `coding-agent` `real-world-tasks`
- [SWE-bench Verified](https://www.swebench.com/SWE-bench/) — A smaller SWE-bench split with human-checked task quality.
  `benchmark` `coding-agent` `verified`
- [SWE-bench Live](https://swe-bench-live.github.io/) — Newer issue-resolution tasks, useful when contamination is a concern.
  `benchmark` `coding-agent` `live`
- [SWE-bench Multimodal](https://www.swebench.com/SWE-bench/) — SWE-style issue tasks where visual context also matters.
  `benchmark` `coding-agent` `multimodal`
- [SWE-bench Multilingual](https://www.swebench.com/multilingual-leaderboard.html) — Issue-resolution tasks spread across multiple programming languages.
  `benchmark` `coding-agent` `multilingual`
- [GAIA](https://huggingface.co/gaia-benchmark) — General assistant tasks that often require tools, web search, files, and multi-step reasoning.
  `benchmark` `general-agent` `tool-use`
- [AgentBench](https://github.com/THUDM/AgentBench) — A broad interactive benchmark across OS, database, web, game, and reasoning environments.
  `benchmark` `general-agent` `interactive`
- [OSWorld](https://os-world.github.io/) — Desktop computer-use tasks with execution-based grading.
  `benchmark` `computer-use` `desktop-agent`
- [macOSWorld](https://macos-world.github.io/) — macOS GUI tasks, with multilingual coverage and a safety-oriented subset.
  `benchmark` `computer-use` `gui-agent`
- [AndroidWorld](https://github.com/google-research/android_world) — Android app tasks with programmatic checks for mobile agents.
  `benchmark` `mobile-agent` `computer-use`
- [ClawBench](https://github.com/reacher-z/ClawBench) — Live-website browser-agent benchmark; 283 everyday tasks (V1 153 + V2 130) across 163 platforms. Two-stage scoring: HTTP-request interception at per-task URL/method schema + LLM judge on the intercepted payload. [Paper](https://arxiv.org/abs/2604.08523) · [Live leaderboard](https://claw-bench.com)
- [Dr. Bench](https://github.com/EVIGBYEN/DrBench) — Evaluates deep-research agents on 214 expert-curated report tasks using semantic quality, topical focus, and retrieval-trustworthiness metrics.
  `benchmark` `general-agent` `dataset`
- [WebArena](https://webarena.dev/) — Self-hosted websites for testing whether browser agents actually change state correctly.
  `benchmark` `browser-agent` `web`
- [VisualWebArena](https://github.com/web-arena-x/visualwebarena) — WebArena-style tasks where screenshots and visual grounding matter.
  `benchmark` `browser-agent` `multimodal`
- [WebArena Verified](https://github.com/ServiceNow/webarena-verified) — Verified WebArena tasks with more deterministic evaluators.
  `benchmark` `browser-agent` `verified`
- [WorkArena](https://servicenow.github.io/WorkArena/) — Enterprise-style ServiceNow tasks for browser agents.
  `benchmark` `browser-agent` `enterprise`
- [BrowserGym](https://github.com/ServiceNow/BrowserGym) — Shared browser-agent environment wrapping WebArena, WorkArena, MiniWoB, and related tasks.
  `framework` `browser-agent` `benchmark-suite`
- [Terminal-Bench](https://www.tbench.ai/) — Terminal tasks for shell use, debugging, and system operations.
  `benchmark` `terminal-agent` `tool-use`
- [tau-bench](https://github.com/sierra-research/tau-bench) — Customer-service tasks where the agent must talk, follow policy, and call APIs.
  `benchmark` `tool-use` `multi-turn`
- [tau2-bench / tau3-bench](https://github.com/sierra-research/tau2-bench) — Newer tau-style tasks for tool-agent-user interaction.
  `benchmark` `tool-use` `enterprise`
- [Berkeley Function Calling Leaderboard](https://gorilla.cs.berkeley.edu/leaderboard.html) — Function-calling tests covering API selection, arguments, multi-turn calls, and executability.
  `benchmark` `function-calling` `tool-use`
- [ToolBench](https://github.com/OpenBMB/ToolBench) — API-heavy tasks for studying tool-use behavior at scale.
  `benchmark` `tool-use` `api`
- [API-Bank](https://github.com/AlibabaResearch/DAMO-ConvAI/tree/main/api-bank) — API selection and multi-step tool-use tasks.
  `benchmark` `tool-use` `api`
- [WebShop](https://webshop-pnlp.github.io/) — Shopping tasks that involve search, comparison, and goal-directed web actions.
  `benchmark` `browser-agent` `commerce`
- [Mind2Web](https://osu-nlp-group.github.io/Mind2Web/) — Real website interaction traces for web navigation tasks.
  `benchmark` `browser-agent` `web-navigation`
- [MiniWoB++](https://github.com/Farama-Foundation/miniwob-plusplus) — Small synthetic browser tasks for fast, controlled experiments.
  `benchmark` `browser-agent` `synthetic`

## Evaluation Frameworks

- [Inspect AI](https://inspect.aisi.org.uk/) — Evaluation framework with tools, sandboxes, scorers, logs, and a result viewer.
  `framework` `evals` `safety`
- [Inspect Evals](https://github.com/UKGovernmentBEIS/inspect_evals) — Ready-made Inspect evals, including agent, coding, and safety tasks.
  `framework` `benchmark-registry` `safety`
- [OpenAI Evals](https://github.com/openai/evals) — Custom evals, model-graded checks, and reusable eval registries.
  `framework` `llm-evaluation` `regression`
- [DeepEval](https://deepeval.com/docs/introduction) — Pytest-style evals for LLM apps, with metrics for agents, tools, safety, and conversations.
  `framework` `testing` `agent-eval`
- [promptfoo](https://github.com/promptfoo/promptfoo) — Regression tests for prompts, models, and agents; works well in CI.
  `framework` `regression` `ci`
- [Ragas](https://docs.ragas.io/en/stable/) — Metrics for RAG, tool use, and agent-style workflows.
  `framework` `metrics` `rag`
- [LangSmith](https://docs.langchain.com/langsmith/home) — Tracing, datasets, experiments, human review, online evaluators, and agent trajectory checks.
  `platform` `observability` `agent-eval`
- [LangChain AgentEvals](https://github.com/langchain-ai/agentevals) — Prebuilt evaluators for agent trajectories and tool-call behavior.
  `framework` `agent-trajectory` `tool-use`
- [Arize Phoenix](https://arize.com/docs/phoenix) — Open-source tracing, dataset experiments, and LLM evaluators.
  `platform` `observability` `evaluation`
- [Langfuse](https://langfuse.com/docs) — Traces, prompts, evals, cost, latency, and production health in one place.
  `platform` `observability` `production`
- [Braintrust](https://www.braintrust.dev/docs) — Datasets, experiments, scorers, tracing, and prompt iteration for AI products.
  `platform` `experiments` `regression`
- [Giskard](https://github.com/Giskard-AI/giskard) — Automated checks for quality, bias, hallucination, and security issues.
  `framework` `quality` `safety`
- [TruLens](https://www.trulens.org/) — Instrumentation and feedback functions for LLM application behavior.
  `framework` `observability` `feedback`
- [OpenTelemetry GenAI Semantic Conventions](https://opentelemetry.io/docs/specs/semconv/gen-ai/) — Common trace and metric fields for GenAI calls.
  `standard` `observability` `telemetry`
- [OpenInference](https://github.com/Arize-ai/openinference) — Open instrumentation conventions for LLM, RAG, and agent traces.
  `standard` `observability` `tracing`

## Coding Agent Evaluation

- [SWE-bench](https://www.swebench.com/SWE-bench/) — The default issue-to-patch benchmark family for coding agents.
  `benchmark` `coding-agent` `github-issues`
- [SWE-agent](https://github.com/SWE-agent/SWE-agent) — Open coding agent and harness built around SWE-bench-style tasks.
  `agent` `coding-agent` `swe-bench`
- [OpenHands](https://github.com/All-Hands-AI/OpenHands) — Open-source software development agent for end-to-end coding workflows.
  `agent` `coding-agent` `open-source`
- [Aider](https://github.com/Aider-AI/aider) — Terminal pair-programming agent; useful for repo-editing regression tasks.
  `agent` `coding-agent` `terminal`
- [BigCodeBench](https://github.com/bigcode-project/bigcodebench) — Practical code-generation tasks with execution tests.
  `benchmark` `code-generation` `execution`
- [RepoBench](https://github.com/Leolty/repobench) — Repository-level code completion and retrieval benchmark.
  `benchmark` `coding-agent` `repository-context`
- [HumanEval](https://github.com/openai/human-eval) — Classic execution-based code benchmark; still useful as a baseline.
  `benchmark` `code-generation` `baseline`
- [EvalPlus](https://github.com/evalplus/evalplus) — Harder test suites for HumanEval and MBPP.
  `benchmark` `code-generation` `execution`
- [LiveCodeBench](https://livecodebench.github.io/) — Newer contest-style coding problems, designed with contamination in mind.
  `benchmark` `code-generation` `live`

## Browser / Web Agent Evaluation

- [WebArena](https://webarena.dev/) — Realistic self-hosted web tasks with state-based success checks.
  `benchmark` `browser-agent` `self-hosted`
- [WorkArena](https://servicenow.github.io/WorkArena/) — ServiceNow-based benchmark for enterprise knowledge-work tasks.
  `benchmark` `browser-agent` `enterprise`
- [BrowserGym](https://github.com/ServiceNow/BrowserGym) — Gym-style interface and shared action space for browser-agent benchmarks.
  `framework` `browser-agent` `environment`
- [AgentLab](https://github.com/ServiceNow/AgentLab) — Tooling for running and analyzing BrowserGym-compatible web agents.
  `framework` `browser-agent` `experiments`
- [Mind2Web](https://osu-nlp-group.github.io/Mind2Web/) — Real-website navigation tasks from user instructions.
  `benchmark` `browser-agent` `navigation`
- [WebLINX](https://mcgill-nlp.github.io/weblinx/) — Browser interaction demonstrations from real-world web tasks.
  `dataset` `browser-agent` `demonstrations`
- [VisualWebArena](https://github.com/web-arena-x/visualwebarena) — Web tasks that need visual grounding, not just DOM text.
  `benchmark` `browser-agent` `visual`
- [MiniWoB++](https://github.com/Farama-Foundation/miniwob-plusplus) — Small controlled UI tasks for quick browser-agent iteration.
  `benchmark` `browser-agent` `synthetic`
- [browser-use benchmark](https://github.com/browser-use/benchmark) — Browser automation tasks spanning established and custom task sets.
  `benchmark` `browser-agent` `automation`

## Tool-Use and Function Calling

- [Berkeley Function Calling Leaderboard](https://gorilla.cs.berkeley.edu/leaderboard.html) — Function-calling tests for relevance, arguments, executability, and multi-turn use.
  `benchmark` `function-calling` `tool-use`
- [tau2-bench / tau3-bench](https://github.com/sierra-research/tau2-bench) — Multi-turn tool-use tasks with simulated users, policies, and database-state scoring.
  `benchmark` `tool-use` `customer-service`
- [ToolBench](https://github.com/OpenBMB/ToolBench) — Large API-oriented benchmark for tool learning and tool use.
  `benchmark` `tool-use` `api`
- [API-Bank](https://github.com/AlibabaResearch/DAMO-ConvAI/tree/main/api-bank) — API choice, API calling, and multi-step tool chaining.
  `benchmark` `tool-use` `api`
- [Gorilla](https://github.com/ShishirPatil/gorilla) — Datasets and methods focused on accurate API calls.
  `dataset` `function-calling` `api`
- [ToolSandbox](https://github.com/apple/ToolSandbox) — Stateful tool-use tasks in simulated environments with execution traces.
  `benchmark` `tool-use` `stateful`
- [Ragas Tool Call Metrics](https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/) — Tool-call and agent-goal metrics for application-level evals.
  `metrics` `tool-use` `agent-eval`

## Multi-Agent Evaluation

- [AutoGenBench](https://microsoft.github.io/autogen/0.2/blog/2024/01/25/AutoGenBench/) — Repeatable tasks and metrics for AutoGen multi-agent workflows.
  `benchmark` `multi-agent` `framework`
- [AgentVerse](https://github.com/OpenBMB/AgentVerse) — Framework for simulating groups of collaborating agents.
  `framework` `multi-agent` `simulation`
- [MetaGPT](https://github.com/FoundationAgents/MetaGPT) — Software-company-style multi-agent workflows; useful for coordination studies.
  `framework` `multi-agent` `software-engineering`
- [ChatDev](https://github.com/OpenBMB/ChatDev) — Multi-agent software development via role-based conversation.
  `framework` `multi-agent` `collaboration`
- [CAMEL](https://github.com/camel-ai/camel) — Role-playing and society simulation infrastructure for agent research.
  `framework` `multi-agent` `simulation`

## Safety & Robustness

- [AgentDojo](https://github.com/ethz-spylab/agentdojo) — Indirect prompt-injection benchmark for tool-using agents.
  `benchmark` `safety` `prompt-injection`
- [AgentHarm](https://ukgovernmentbeis.github.io/inspect_evals/evals/safeguards/agentharm/) — Harmful-request tasks for agent settings, including cybercrime and fraud.
  `benchmark` `safety` `agent`
- [b3: Backbone Breaker Benchmark](https://ukgovernmentbeis.github.io/inspect_evals/evals/safeguards/b3/) — Agentic security tasks around exfiltration, compromise, and misuse.
  `benchmark` `security` `agent`
- [Purple Llama CyberSecEval](https://github.com/meta-llama/PurpleLlama) — Cybersecurity safety evals for LLMs and agentic systems.
  `benchmark` `security` `cyber`
- [HarmBench](https://github.com/centerforaisafety/HarmBench) — Standardized adversarial tasks for harmful-behavior robustness.
  `benchmark` `safety` `robustness`
- [PromptBench](https://github.com/microsoft/promptbench) — Prompt robustness and adversarial prompt sensitivity tests.
  `benchmark` `robustness` `prompts`
- [Garak](https://github.com/NVIDIA/garak) — Scanner for jailbreaks, prompt injection, data leakage, and related LLM app risks.
  `tool` `red-teaming` `security`
- [PyRIT](https://github.com/Azure/PyRIT) — Automation framework for AI red-team workflows.
  `tool` `red-teaming` `safety`

## Reliability & Failure Recovery

- [Terminal-Bench](https://www.tbench.ai/) — Good fit for studying recovery in shell-based tasks.
  `benchmark` `reliability` `terminal`
- [tau2-bench / tau3-bench](https://github.com/sierra-research/tau2-bench) — Captures policy, conversation, and tool-use failures in support-style workflows.
  `benchmark` `reliability` `tool-use`
- [LangSmith Online Evaluators](https://docs.langchain.com/langsmith/online-evaluations-llm-as-judge) — Online scoring for production traces and regressions.
  `platform` `monitoring` `regression`
- [promptfoo Assertions](https://www.promptfoo.dev/docs/configuration/expected-outputs/) — Deterministic, model-graded, and custom assertions for regression suites.
  `framework` `regression` `ci`
- [DeepEval Metrics](https://deepeval.com/docs/metrics-introduction) — Agent, tool-use, conversation, safety, and custom metrics.
  `framework` `metrics` `regression`
- [Invariant](https://github.com/invariantlabs-ai/invariant) — Guardrails and tests over agent traces, tool calls, and app behavior.
  `framework` `guardrails` `agent-traces`

## Cost, Latency, and Efficiency

- [Langfuse](https://langfuse.com/docs) — Trace-level cost, latency, model usage, prompts, and eval scores.
  `platform` `cost` `observability`
- [Helicone](https://github.com/Helicone/helicone) — Open-source request logging, cost tracking, and usage analytics.
  `platform` `cost` `monitoring`
- [LiteLLM Proxy](https://docs.litellm.ai/docs/proxy/quick_start) — Model routing, budgets, logging, and spend controls.
  `tool` `cost` `routing`
- [OpenLLMetry](https://github.com/traceloop/openllmetry) — OpenTelemetry-compatible traces and metrics for LLM apps.
  `tool` `observability` `telemetry`
- [OpenTelemetry GenAI Semantic Conventions](https://opentelemetry.io/docs/specs/semconv/gen-ai/) — Shared telemetry fields for GenAI cost, latency, and usage analysis.
  `standard` `telemetry` `metrics`
- [Phoenix Tracing](https://arize.com/docs/phoenix/tracing) — LLM, retrieval, and tool-use traces for debugging and latency analysis.
  `platform` `latency` `tracing`

## Human Evaluation Rubrics

- [LangSmith Annotation Queues](https://docs.langchain.com/langsmith/annotation-queues) — Human review queues for traces and structured feedback.
  `human-eval` `annotation` `platform`
- [Braintrust Human Review](https://www.braintrust.dev/docs/guides/human-review) — Human review over experiments and production traces.
  `human-eval` `annotation` `platform`
- [Phoenix Human Feedback](https://arize.com/docs/phoenix/tracing/concepts-tracing/concepts-annotations) — Human labels and annotations alongside automated evals.
  `human-eval` `annotation` `observability`
- [OpenAI Evals Model-Graded Templates](https://github.com/openai/evals/blob/main/docs/eval-templates.md) — Reusable patterns for rubric-based and model-graded evals.
  `rubric` `llm-as-judge` `templates`
- [Langfuse Scores](https://langfuse.com/docs/scores/overview) — Human, heuristic, and model-based scores on traces.
  `human-eval` `scoring` `monitoring`

## Production Monitoring

- [LangSmith](https://docs.langchain.com/langsmith/home) — Tracing, datasets, online evals, human review, and deployment monitoring.
  `platform` `production` `monitoring`
- [Langfuse](https://langfuse.com/docs) — Open-source observability, prompt management, evals, and production health tracking.
  `platform` `production` `observability`
- [Arize Phoenix](https://arize.com/docs/phoenix) — Tracing, experiments, evals, prompt iteration, and self-hosted debugging.
  `platform` `production` `observability`
- [Braintrust](https://www.braintrust.dev/docs) — Offline experiments, production logging, scorers, and datasets.
  `platform` `production` `evalops`
- [Confident AI](https://docs.confident-ai.com/) — Hosted reports, monitoring, and quality tracking around DeepEval.
  `platform` `production` `monitoring`
- [Helicone](https://github.com/Helicone/helicone) — Request logs, user analytics, cost, latency, and provider behavior.
  `platform` `monitoring` `cost`
- [WhyLabs LangKit](https://github.com/whylabs/langkit) — Text quality, prompt-injection, toxicity, and drift signals.
  `tool` `monitoring` `quality`
- [TruLens](https://www.trulens.org/) — Feedback-based monitoring and evals for LLM applications.
  `platform` `monitoring` `feedback`

## Papers

- [SWE-bench: Can Language Models Resolve Real-World GitHub Issues?](https://arxiv.org/abs/2310.06770) — The paper behind repository-level issue-to-patch evaluation.
  `paper` `coding-agent` `benchmark`
- [AgentBench: Evaluating LLMs as Agents](https://arxiv.org/abs/2308.03688) — Multi-environment benchmark for interactive LLM agents.
  `paper` `general-agent` `benchmark`
- [GAIA: A Benchmark for General AI Assistants](https://arxiv.org/abs/2311.12983) — Hard assistant tasks involving reasoning, tools, and external resources.
  `paper` `general-agent` `benchmark`
- [OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments](https://arxiv.org/abs/2404.07972) — Desktop computer-use benchmark with execution-based grading.
  `paper` `computer-use` `benchmark`
- [WebArena: A Realistic Web Environment for Building Autonomous Agents](https://arxiv.org/abs/2307.13854) — Self-hosted websites for functional browser-agent evaluation.
  `paper` `browser-agent` `benchmark`
- [VisualWebArena: Evaluating Multimodal Agents on Realistic Visual Web Tasks](https://arxiv.org/abs/2401.13649) — WebArena-style tasks with visual grounding requirements.
  `paper` `browser-agent` `multimodal`
- [WorkArena: How Capable Are Web Agents at Solving Common Knowledge Work Tasks?](https://arxiv.org/abs/2403.07718) — Enterprise knowledge-work tasks for browser agents.
  `paper` `browser-agent` `enterprise`
- [The BrowserGym Ecosystem for Web Agent Research](https://arxiv.org/abs/2412.05467) — Shared environment and tooling for browser-agent research.
  `paper` `browser-agent` `framework`
- [tau-bench: A Benchmark for Tool-Agent-User Interaction in Real-World Domains](https://arxiv.org/abs/2406.12045) — Multi-turn tool-agent-user interaction in realistic domains.
  `paper` `tool-use` `multi-turn`
- [Berkeley Function-Calling Leaderboard](https://gorilla.cs.berkeley.edu/blogs/8_berkeley_function_calling_leaderboard.html) — Background on executable function-calling evaluation and BFCL.
  `paper` `function-calling` `tool-use`
- [ToolLLM: Facilitating Large Language Models to Master 16000+ Real-world APIs](https://arxiv.org/abs/2307.16789) — ToolBench and methods for API-using LLM agents.
  `paper` `tool-use` `api`
- [API-Bank: A Comprehensive Benchmark for Tool-Augmented LLMs](https://arxiv.org/abs/2304.08244) — API-augmented LLM evaluation and training.
  `paper` `tool-use` `api`
- [AgentDojo: A Dynamic Environment to Evaluate Prompt Injection Attacks and Defenses for LLM Agents](https://arxiv.org/abs/2406.13352) — Utility-security tradeoffs under prompt-injection attacks.
  `paper` `safety` `prompt-injection`
- [AgentHarm: A Benchmark for Measuring Harmfulness of LLM Agents](https://arxiv.org/abs/2410.09024) — Harmful-behavior benchmark for agentic settings.
  `paper` `safety` `agent`

## Datasets

- [SWE-bench on Hugging Face](https://huggingface.co/datasets/princeton-nlp/SWE-bench) — Dataset of real GitHub issue-resolution tasks for coding-agent evaluation.
  `dataset` `coding-agent` `github-issues`
- [SWE-bench Verified on Hugging Face](https://huggingface.co/datasets/princeton-nlp/SWE-bench_Verified) — Engineer-validated subset for more reliable coding-agent measurement.
  `dataset` `coding-agent` `verified`
- [GAIA Dataset](https://huggingface.co/datasets/gaia-benchmark/GAIA) — General assistant benchmark data with tasks requiring tools and external resources.
  `dataset` `general-agent` `tool-use`
- [Mind2Web Dataset](https://huggingface.co/datasets/osunlp/Mind2Web) — Real website navigation task data for training and evaluating web agents.
  `dataset` `browser-agent` `navigation`
- [WebLINX Dataset](https://huggingface.co/datasets/McGill-NLP/weblinx) — Browser interaction demonstrations for real-world web tasks.
  `dataset` `browser-agent` `demonstrations`
- [AgentHarm Dataset](https://huggingface.co/datasets/ai-safety-institute/AgentHarm) — Harmful-behavior tasks for agent safety evaluation.
  `dataset` `safety` `agent`
- [BFCL Dataset](https://huggingface.co/datasets/gorilla-llm/Berkeley-Function-Calling-Leaderboard) — Function-calling benchmark data for tool invocation evaluation.
  `dataset` `function-calling` `tool-use`
- [ToolBench Dataset](https://github.com/OpenBMB/ToolBench) — Tool-use data for API-oriented agent evaluation and training.
  `dataset` `tool-use` `api`

## Reports & Case Studies

- [SWE-bench Leaderboard](https://www.swebench.com/) — Submitted systems across SWE-bench variants.
  `leaderboard` `coding-agent` `benchmark`
- [GAIA Leaderboard](https://huggingface.co/spaces/gaia-benchmark/leaderboard) — Public submissions for the GAIA assistant benchmark.
  `leaderboard` `general-agent` `benchmark`
- [OSWorld Leaderboard](https://os-world.github.io/) — Computer-use agent results on desktop task suites.
  `leaderboard` `computer-use` `benchmark`
- [Terminal-Bench Leaderboard](https://www.tbench.ai/) — Terminal-agent results and benchmark releases.
  `leaderboard` `terminal-agent` `benchmark`
- [BFCL Leaderboard](https://gorilla.cs.berkeley.edu/leaderboard.html) — Function-calling results across model providers.
  `leaderboard` `function-calling` `tool-use`
- [Inspect Evals Documentation](https://ukgovernmentbeis.github.io/inspect_evals/) — Runnable Inspect evals for safety, coding, agent, and reasoning tasks.
  `docs` `benchmark-registry` `safety`

## Related Awesome Lists

- [Awesome-LLM-Eval](https://github.com/onejune2018/awesome-llm-eval) — Broader LLM evaluation methods, datasets, tools, and leaderboards.
  `awesome-list` `llm-evaluation` `related`
- [awesome-llm-agents](https://github.com/kaushikb11/awesome-llm-agents) — Broader LLM agent papers, projects, frameworks, and resources.
  `awesome-list` `llm-agents` `related`
- [awesome-ai-agents](https://github.com/e2b-dev/awesome-ai-agents) — Agent frameworks, tools, and examples across the ecosystem.
  `awesome-list` `ai-agents` `related`
- [awesome-production-machine-learning](https://github.com/EthicalML/awesome-production-machine-learning) — Useful for connecting agent evaluation to production ML monitoring and operations.
  `awesome-list` `production` `monitoring`

## Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a PR.

## License

This project is released under [CC0-1.0](LICENSE).
