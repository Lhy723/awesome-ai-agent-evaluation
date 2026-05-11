# Awesome AI Agent Evaluation

![Awesome AI Agent Evaluation social preview](assets/social-preview.png)

<p align="center">
  <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome"></a>
  <a href="README.zh-CN.md">Chinese</a>
</p>

Benchmarks, eval harnesses, papers, datasets, and production checks for AI agents.

Agent evaluation is still a scattered field. Some resources are academic benchmarks, some are engineering test harnesses, some are observability tools, and some are production practices that only make sense after you have traces from real users.

This list keeps those pieces in one place, with a bias toward resources that help answer concrete engineering questions: what was tested, how it was scored, what failed, and whether the result is useful outside a demo.

<table>
  <tr>
    <th>Included</th>
    <th>Left out</th>
  </tr>
  <tr>
    <td>Benchmarks with clear tasks or scoring</td>
    <td>Generic agent demos</td>
  </tr>
  <tr>
    <td>Frameworks that help run or track evals</td>
    <td>Prompt collections without evaluation</td>
  </tr>
  <tr>
    <td>Papers and reports with reusable methodology</td>
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

- [OpenAI Evals](https://github.com/openai/evals) — Provides an open-source framework and registry for building repeatable LLM system evaluations.
  `framework` `evals` `regression`
- [OpenAI Cookbook: Evaluating model performance](https://cookbook.openai.com/examples/evaluation/how_to_eval_abstractive_summarization) — Shows practical patterns for creating task-specific evaluations and comparing model outputs.
  `guide` `evaluation-basics` `llm-as-judge`
- [Hamel Husain: Your AI Product Needs Evals](https://hamel.dev/blog/posts/evals/) — Explains how to design evals for real product workflows instead of relying only on generic benchmarks.
  `guide` `product-evals` `methodology`
- [Anthropic: Building effective agents](https://www.anthropic.com/research/building-effective-agents) — Clarifies agent patterns and helps frame which behaviors are worth evaluating.
  `guide` `agent-design` `methodology`
- [LangChain Agent Evals](https://docs.langchain.com/oss/python/langchain/evals) — Introduces trajectory-level agent evaluation with deterministic and judge-based comparison.
  `guide` `agent-trajectory` `framework`
- [Phoenix LLM Evals](https://arize.com/docs/phoenix/evaluation/llm-evals) — Documents practical LLM and agent evaluation workflows over traces, datasets, and experiments.
  `guide` `observability` `llm-as-judge`

## Benchmarks

- [SWE-bench](https://www.swebench.com/SWE-bench/) — Evaluates coding agents on real GitHub issues that require repository-level patches.
  `benchmark` `coding-agent` `real-world-tasks`
- [SWE-bench Verified](https://www.swebench.com/SWE-bench/) — Curates engineer-confirmed solvable SWE-bench tasks for more reliable coding-agent comparison.
  `benchmark` `coding-agent` `verified`
- [SWE-bench Live](https://swe-bench-live.github.io/) — Tracks newer issue-resolution tasks to reduce benchmark contamination for coding agents.
  `benchmark` `coding-agent` `live`
- [SWE-bench Multimodal](https://www.swebench.com/SWE-bench/) — Extends software issue evaluation to tasks with visual or multimodal context.
  `benchmark` `coding-agent` `multimodal`
- [SWE-bench Multilingual](https://www.swebench.com/multilingual-leaderboard.html) — Evaluates issue-resolution ability across multiple programming languages.
  `benchmark` `coding-agent` `multilingual`
- [GAIA](https://huggingface.co/gaia-benchmark) — Tests general assistant agents on questions requiring reasoning, tool use, web use, and file handling.
  `benchmark` `general-agent` `tool-use`
- [AgentBench](https://github.com/THUDM/AgentBench) — Evaluates LLM agents across interactive environments such as OS, database, web browsing, and games.
  `benchmark` `general-agent` `interactive`
- [OSWorld](https://os-world.github.io/) — Evaluates multimodal computer-use agents on real desktop tasks with execution-based grading.
  `benchmark` `computer-use` `desktop-agent`
- [macOSWorld](https://macos-world.github.io/) — Tests GUI agents in multilingual macOS tasks, including a safety-focused subset.
  `benchmark` `computer-use` `gui-agent`
- [AndroidWorld](https://github.com/google-research/android_world) — Evaluates mobile agents on Android tasks with app-level interaction and programmatic checks.
  `benchmark` `mobile-agent` `computer-use`
- [WebArena](https://webarena.dev/) — Provides self-hosted realistic websites for evaluating browser agents on functional task completion.
  `benchmark` `browser-agent` `web`
- [VisualWebArena](https://github.com/web-arena-x/visualwebarena) — Adds visually grounded website tasks for agents that use screenshots and page state.
  `benchmark` `browser-agent` `multimodal`
- [WebArena Verified](https://github.com/ServiceNow/webarena-verified) — Curates verified WebArena tasks and deterministic evaluators for more reproducible web-agent testing.
  `benchmark` `browser-agent` `verified`
- [WorkArena](https://servicenow.github.io/WorkArena/) — Evaluates browser agents on enterprise-style ServiceNow knowledge-work tasks.
  `benchmark` `browser-agent` `enterprise`
- [BrowserGym](https://github.com/ServiceNow/BrowserGym) — Standardizes browser-agent environments and bundles benchmarks including WebArena, WorkArena, and MiniWoB.
  `framework` `browser-agent` `benchmark-suite`
- [Terminal-Bench](https://www.tbench.ai/) — Measures agents on terminal-based tasks that require shell use, debugging, and system operations.
  `benchmark` `terminal-agent` `tool-use`
- [tau-bench](https://github.com/sierra-research/tau-bench) — Evaluates customer-service agents that must converse, follow policies, and call domain APIs.
  `benchmark` `tool-use` `multi-turn`
- [tau2-bench / tau3-bench](https://github.com/sierra-research/tau2-bench) — Updates tau-bench with fixed tasks and newer domains for tool-agent-user interaction.
  `benchmark` `tool-use` `enterprise`
- [Berkeley Function Calling Leaderboard](https://gorilla.cs.berkeley.edu/leaderboard.html) — Compares model function-calling ability across languages, APIs, multi-turn calls, and executability.
  `benchmark` `function-calling` `tool-use`
- [ToolBench](https://github.com/OpenBMB/ToolBench) — Benchmarks tool-use learning and execution across a large API-oriented task set.
  `benchmark` `tool-use` `api`
- [API-Bank](https://github.com/AlibabaResearch/DAMO-ConvAI/tree/main/api-bank) — Evaluates tool-augmented LLMs on API selection, calling, and multi-step tool use.
  `benchmark` `tool-use` `api`
- [WebShop](https://webshop-pnlp.github.io/) — Tests agents on web shopping tasks with search, comparison, and purchase-goal reasoning.
  `benchmark` `browser-agent` `commerce`
- [Mind2Web](https://osu-nlp-group.github.io/Mind2Web/) — Provides real website interaction traces for learning and evaluating web navigation agents.
  `benchmark` `browser-agent` `web-navigation`
- [MiniWoB++](https://github.com/Farama-Foundation/miniwob-plusplus) — Provides compact synthetic browser tasks useful for controlled web-agent experimentation.
  `benchmark` `browser-agent` `synthetic`

## Evaluation Frameworks

- [Inspect AI](https://inspect.aisi.org.uk/) — Offers a model-evaluation framework with tool calling, sandboxes, scorers, logs, and web-based result inspection.
  `framework` `evals` `safety`
- [Inspect Evals](https://github.com/UKGovernmentBEIS/inspect_evals) — Collects community eval implementations for Inspect, including agent, coding, and safety tasks.
  `framework` `benchmark-registry` `safety`
- [OpenAI Evals](https://github.com/openai/evals) — Supports custom evals, model-graded checks, and reusable registries for LLM systems.
  `framework` `llm-evaluation` `regression`
- [DeepEval](https://deepeval.com/docs/introduction) — Provides pytest-style LLM and agent evaluation with metrics for tool use, safety, conversation, and regression testing.
  `framework` `testing` `agent-eval`
- [promptfoo](https://github.com/promptfoo/promptfoo) — Runs prompt, model, and agent regression tests with assertions, red teaming, and CI-friendly reports.
  `framework` `regression` `ci`
- [Ragas](https://docs.ragas.io/en/stable/) — Provides evaluation metrics for RAG, tool use, and agentic workflows.
  `framework` `metrics` `rag`
- [LangSmith](https://docs.langchain.com/langsmith/home) — Supports tracing, datasets, experiments, human review, online evaluators, and agent trajectory evaluation.
  `platform` `observability` `agent-eval`
- [LangChain AgentEvals](https://github.com/langchain-ai/agentevals) — Provides prebuilt evaluators for comparing agent trajectories and tool-call behavior.
  `framework` `agent-trajectory` `tool-use`
- [Arize Phoenix](https://arize.com/docs/phoenix) — Offers open-source tracing, dataset experiments, and LLM evaluators for debugging AI applications.
  `platform` `observability` `evaluation`
- [Langfuse](https://langfuse.com/docs) — Tracks traces, prompts, evaluations, cost, latency, and production health for LLM applications.
  `platform` `observability` `production`
- [Braintrust](https://www.braintrust.dev/docs) — Provides datasets, experiments, evaluators, tracing, and prompt iteration for AI product evaluation.
  `platform` `experiments` `regression`
- [Giskard](https://github.com/Giskard-AI/giskard) — Tests AI systems for quality, bias, hallucination, and security issues with automated checks.
  `framework` `quality` `safety`
- [TruLens](https://www.trulens.org/) — Provides instrumentation and feedback functions for evaluating LLM application behavior.
  `framework` `observability` `feedback`
- [OpenTelemetry GenAI Semantic Conventions](https://opentelemetry.io/docs/specs/semconv/gen-ai/) — Standardizes trace and metric attributes for GenAI calls and agent observability.
  `standard` `observability` `telemetry`
- [OpenInference](https://github.com/Arize-ai/openinference) — Defines open instrumentation conventions for tracing LLM, RAG, and agent applications.
  `standard` `observability` `tracing`

## Coding Agent Evaluation

- [SWE-bench](https://www.swebench.com/SWE-bench/) — The default benchmark family for measuring issue-to-patch software engineering ability.
  `benchmark` `coding-agent` `github-issues`
- [SWE-agent](https://github.com/SWE-agent/SWE-agent) — Provides an open coding agent and evaluation harness built around SWE-bench-style tasks.
  `agent` `coding-agent` `swe-bench`
- [OpenHands](https://github.com/All-Hands-AI/OpenHands) — Open-source software development agent useful for evaluating end-to-end coding workflows.
  `agent` `coding-agent` `open-source`
- [Aider](https://github.com/Aider-AI/aider) — Terminal pair-programming agent that can be evaluated on repository editing and regression tasks.
  `agent` `coding-agent` `terminal`
- [BigCodeBench](https://github.com/bigcode-project/bigcodebench) — Evaluates practical code generation with richer function-level tasks and execution tests.
  `benchmark` `code-generation` `execution`
- [RepoBench](https://github.com/Leolty/repobench) — Measures repository-level code completion and retrieval, useful for agent context evaluation.
  `benchmark` `coding-agent` `repository-context`
- [HumanEval](https://github.com/openai/human-eval) — Classic execution-based code-generation benchmark that can serve as a baseline before agentic coding tasks.
  `benchmark` `code-generation` `baseline`
- [EvalPlus](https://github.com/evalplus/evalplus) — Strengthens HumanEval and MBPP with additional tests for more reliable code-generation evaluation.
  `benchmark` `code-generation` `execution`
- [LiveCodeBench](https://livecodebench.github.io/) — Evaluates coding ability on newer contest-style problems to reduce contamination risk.
  `benchmark` `code-generation` `live`

## Browser / Web Agent Evaluation

- [WebArena](https://webarena.dev/) — Self-hosted realistic web tasks for measuring whether an agent changes website state correctly.
  `benchmark` `browser-agent` `self-hosted`
- [WorkArena](https://servicenow.github.io/WorkArena/) — Enterprise browser benchmark for common knowledge-work tasks in ServiceNow.
  `benchmark` `browser-agent` `enterprise`
- [BrowserGym](https://github.com/ServiceNow/BrowserGym) — Provides a Gym-like interface and shared action space for browser-agent benchmarks.
  `framework` `browser-agent` `environment`
- [AgentLab](https://github.com/ServiceNow/AgentLab) — Helps implement, run, and analyze web agents across BrowserGym-compatible benchmarks.
  `framework` `browser-agent` `experiments`
- [Mind2Web](https://osu-nlp-group.github.io/Mind2Web/) — Evaluates real-website navigation from user instructions and observed web pages.
  `benchmark` `browser-agent` `navigation`
- [WebLINX](https://mcgill-nlp.github.io/weblinx/) — Provides real-world browser interaction demonstrations for training and evaluating web agents.
  `dataset` `browser-agent` `demonstrations`
- [VisualWebArena](https://github.com/web-arena-x/visualwebarena) — Tests visual grounding and multimodal reasoning in web-agent tasks.
  `benchmark` `browser-agent` `visual`
- [MiniWoB++](https://github.com/Farama-Foundation/miniwob-plusplus) — Offers small, controlled web UI tasks for rapid agent iteration.
  `benchmark` `browser-agent` `synthetic`
- [browser-use benchmark](https://github.com/browser-use/benchmark) — Curates browser automation tasks across established and custom task families.
  `benchmark` `browser-agent` `automation`

## Tool-Use and Function Calling

- [Berkeley Function Calling Leaderboard](https://gorilla.cs.berkeley.edu/leaderboard.html) — Measures function-calling, relevance detection, executable calls, and multi-turn tool use.
  `benchmark` `function-calling` `tool-use`
- [tau2-bench / tau3-bench](https://github.com/sierra-research/tau2-bench) — Evaluates multi-turn tool-using agents with simulated users, policies, and database-state scoring.
  `benchmark` `tool-use` `customer-service`
- [ToolBench](https://github.com/OpenBMB/ToolBench) — Tests tool-learning and API-use ability over many real-world tools.
  `benchmark` `tool-use` `api`
- [API-Bank](https://github.com/AlibabaResearch/DAMO-ConvAI/tree/main/api-bank) — Evaluates whether models can choose, call, and chain APIs correctly.
  `benchmark` `tool-use` `api`
- [Gorilla](https://github.com/ShishirPatil/gorilla) — Provides datasets and methods for teaching models to call APIs accurately.
  `dataset` `function-calling` `api`
- [ToolSandbox](https://github.com/apple/ToolSandbox) — Evaluates stateful tool-use agents in simulated environments with execution traces.
  `benchmark` `tool-use` `stateful`
- [Ragas Tool Call Metrics](https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/) — Includes tool-call accuracy and agent-goal metrics for application-level evaluation.
  `metrics` `tool-use` `agent-eval`

## Multi-Agent Evaluation

- [AutoGenBench](https://microsoft.github.io/autogen/0.2/blog/2024/01/25/AutoGenBench/) — Benchmarks multi-agent workflows built with AutoGen through repeatable tasks and metrics.
  `benchmark` `multi-agent` `framework`
- [AgentVerse](https://github.com/OpenBMB/AgentVerse) — Provides a framework for simulating and evaluating groups of collaborating agents.
  `framework` `multi-agent` `simulation`
- [MetaGPT](https://github.com/FoundationAgents/MetaGPT) — Implements software-company-style multi-agent workflows that can be evaluated for coordination and output quality.
  `framework` `multi-agent` `software-engineering`
- [ChatDev](https://github.com/OpenBMB/ChatDev) — Explores communicative multi-agent software development and coordination patterns.
  `framework` `multi-agent` `collaboration`
- [CAMEL](https://github.com/camel-ai/camel) — Provides multi-agent role-playing and society simulation infrastructure for agent research.
  `framework` `multi-agent` `simulation`

## Safety & Robustness

- [AgentDojo](https://github.com/ethz-spylab/agentdojo) — Evaluates tool-using agents against indirect prompt-injection attacks and utility-security tradeoffs.
  `benchmark` `safety` `prompt-injection`
- [AgentHarm](https://ukgovernmentbeis.github.io/inspect_evals/evals/safeguards/agentharm/) — Tests whether agents comply with harmful requests across cybercrime, fraud, harassment, and related domains.
  `benchmark` `safety` `agent`
- [b3: Backbone Breaker Benchmark](https://ukgovernmentbeis.github.io/inspect_evals/evals/safeguards/b3/) — Evaluates agentic AI security vulnerabilities such as data exfiltration and system compromise.
  `benchmark` `security` `agent`
- [Purple Llama CyberSecEval](https://github.com/meta-llama/PurpleLlama) — Provides cybersecurity safety evaluations for LLMs and agents.
  `benchmark` `security` `cyber`
- [HarmBench](https://github.com/centerforaisafety/HarmBench) — Evaluates refusal and harmful-behavior robustness across standardized adversarial tasks.
  `benchmark` `safety` `robustness`
- [PromptBench](https://github.com/microsoft/promptbench) — Tests prompt robustness and adversarial prompt sensitivity across NLP and LLM tasks.
  `benchmark` `robustness` `prompts`
- [Garak](https://github.com/NVIDIA/garak) — Scans LLM applications for vulnerabilities such as jailbreaks, prompt injection, and data leakage.
  `tool` `red-teaming` `security`
- [PyRIT](https://github.com/Azure/PyRIT) — Automates AI red teaming workflows for identifying safety and security risks.
  `tool` `red-teaming` `safety`

## Reliability & Failure Recovery

- [Terminal-Bench](https://www.tbench.ai/) — Useful for measuring whether terminal agents can recover from errors while completing system tasks.
  `benchmark` `reliability` `terminal`
- [tau2-bench / tau3-bench](https://github.com/sierra-research/tau2-bench) — Captures policy, conversation, and tool-use failures in realistic customer-support settings.
  `benchmark` `reliability` `tool-use`
- [LangSmith Online Evaluators](https://docs.langchain.com/langsmith/online-evaluations-llm-as-judge) — Scores production traces to detect regressions and quality drift after deployment.
  `platform` `monitoring` `regression`
- [promptfoo Assertions](https://www.promptfoo.dev/docs/configuration/expected-outputs/) — Lets teams express deterministic, model-graded, and custom assertions for regression testing.
  `framework` `regression` `ci`
- [DeepEval Metrics](https://deepeval.com/docs/metrics-introduction) — Provides agent, tool-use, conversational, safety, and custom metrics for automated test suites.
  `framework` `metrics` `regression`
- [Invariant](https://github.com/invariantlabs-ai/invariant) — Helps define guardrails and tests over agent traces, tool calls, and application behavior.
  `framework` `guardrails` `agent-traces`

## Cost, Latency, and Efficiency

- [Langfuse](https://langfuse.com/docs) — Tracks trace-level cost, latency, model usage, prompts, and evaluation scores.
  `platform` `cost` `observability`
- [Helicone](https://github.com/Helicone/helicone) — Provides open-source LLM observability, usage analytics, cost tracking, and request logging.
  `platform` `cost` `monitoring`
- [LiteLLM Proxy](https://docs.litellm.ai/docs/proxy/quick_start) — Adds unified model routing, budgets, logging, and spend controls for LLM applications.
  `tool` `cost` `routing`
- [OpenLLMetry](https://github.com/traceloop/openllmetry) — Instruments LLM applications with OpenTelemetry-compatible traces and metrics.
  `tool` `observability` `telemetry`
- [OpenTelemetry GenAI Semantic Conventions](https://opentelemetry.io/docs/specs/semconv/gen-ai/) — Defines common telemetry fields for GenAI systems, helping normalize cost and latency analysis.
  `standard` `telemetry` `metrics`
- [Phoenix Tracing](https://arize.com/docs/phoenix/tracing) — Captures LLM, retrieval, and tool-use traces for latency analysis and debugging.
  `platform` `latency` `tracing`

## Human Evaluation Rubrics

- [LangSmith Annotation Queues](https://docs.langchain.com/langsmith/annotation-queues) — Routes traces to human reviewers and captures structured feedback for model and agent evaluation.
  `human-eval` `annotation` `platform`
- [Braintrust Human Review](https://www.braintrust.dev/docs/guides/human-review) — Supports human review workflows over experiment results and production traces.
  `human-eval` `annotation` `platform`
- [Phoenix Human Feedback](https://arize.com/docs/phoenix/tracing/concepts-tracing/concepts-annotations) — Supports human labels and annotations alongside automated evaluations.
  `human-eval` `annotation` `observability`
- [OpenAI Evals Model-Graded Templates](https://github.com/openai/evals/blob/main/docs/eval-templates.md) — Provides reusable patterns for rubric-based and model-graded evaluation.
  `rubric` `llm-as-judge` `templates`
- [Langfuse Scores](https://langfuse.com/docs/scores/overview) — Tracks human, heuristic, and model-based scores on traces and observations.
  `human-eval` `scoring` `monitoring`

## Production Monitoring

- [LangSmith](https://docs.langchain.com/langsmith/home) — Combines tracing, datasets, online evaluators, human review, and deployment monitoring for agents.
  `platform` `production` `monitoring`
- [Langfuse](https://langfuse.com/docs) — Provides open-source observability, prompt management, evaluations, and production health tracking.
  `platform` `production` `observability`
- [Arize Phoenix](https://arize.com/docs/phoenix) — Supports tracing, experiments, evaluations, prompt iteration, and self-hosted debugging workflows.
  `platform` `production` `observability`
- [Braintrust](https://www.braintrust.dev/docs) — Connects offline experiments, production logging, scorers, and datasets for continuous AI quality.
  `platform` `production` `evalops`
- [Confident AI](https://docs.confident-ai.com/) — Provides a hosted platform around DeepEval for evaluation reports, monitoring, and quality tracking.
  `platform` `production` `monitoring`
- [Helicone](https://github.com/Helicone/helicone) — Tracks request logs, user analytics, cost, latency, and model provider behavior.
  `platform` `monitoring` `cost`
- [WhyLabs LangKit](https://github.com/whylabs/langkit) — Provides text-quality, prompt-injection, toxicity, and drift signals for LLM monitoring.
  `tool` `monitoring` `quality`
- [TruLens](https://www.trulens.org/) — Provides feedback-based monitoring and evaluation for LLM applications.
  `platform` `monitoring` `feedback`

## Papers

- [SWE-bench: Can Language Models Resolve Real-World GitHub Issues?](https://arxiv.org/abs/2310.06770) — Introduces issue-to-patch evaluation over real GitHub repositories.
  `paper` `coding-agent` `benchmark`
- [AgentBench: Evaluating LLMs as Agents](https://arxiv.org/abs/2308.03688) — Defines a multi-environment benchmark for interactive LLM agents.
  `paper` `general-agent` `benchmark`
- [GAIA: A Benchmark for General AI Assistants](https://arxiv.org/abs/2311.12983) — Introduces challenging assistant tasks requiring reasoning, tools, and multimodal resources.
  `paper` `general-agent` `benchmark`
- [OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments](https://arxiv.org/abs/2404.07972) — Introduces execution-based desktop task evaluation for computer-use agents.
  `paper` `computer-use` `benchmark`
- [WebArena: A Realistic Web Environment for Building Autonomous Agents](https://arxiv.org/abs/2307.13854) — Introduces self-hosted realistic websites for functional web-agent evaluation.
  `paper` `browser-agent` `benchmark`
- [VisualWebArena: Evaluating Multimodal Agents on Realistic Visual Web Tasks](https://arxiv.org/abs/2401.13649) — Extends WebArena with visual grounding requirements.
  `paper` `browser-agent` `multimodal`
- [WorkArena: How Capable Are Web Agents at Solving Common Knowledge Work Tasks?](https://arxiv.org/abs/2403.07718) — Evaluates browser agents on enterprise knowledge-work tasks.
  `paper` `browser-agent` `enterprise`
- [The BrowserGym Ecosystem for Web Agent Research](https://arxiv.org/abs/2412.05467) — Describes a shared browser-agent environment and benchmark ecosystem.
  `paper` `browser-agent` `framework`
- [tau-bench: A Benchmark for Tool-Agent-User Interaction in Real-World Domains](https://arxiv.org/abs/2406.12045) — Evaluates agents in multi-turn conversations with tools, policies, and simulated users.
  `paper` `tool-use` `multi-turn`
- [Berkeley Function-Calling Leaderboard](https://gorilla.cs.berkeley.edu/blogs/8_berkeley_function_calling_leaderboard.html) — Explains executable function-calling evaluation and the BFCL benchmark family.
  `paper` `function-calling` `tool-use`
- [ToolLLM: Facilitating Large Language Models to Master 16000+ Real-world APIs](https://arxiv.org/abs/2307.16789) — Introduces ToolBench and methods for API-using LLM agents.
  `paper` `tool-use` `api`
- [API-Bank: A Comprehensive Benchmark for Tool-Augmented LLMs](https://arxiv.org/abs/2304.08244) — Studies API-augmented LLM evaluation and training.
  `paper` `tool-use` `api`
- [AgentDojo: A Dynamic Environment to Evaluate Prompt Injection Attacks and Defenses for LLM Agents](https://arxiv.org/abs/2406.13352) — Introduces utility-security evaluation for tool-using agents.
  `paper` `safety` `prompt-injection`
- [AgentHarm: A Benchmark for Measuring Harmfulness of LLM Agents](https://arxiv.org/abs/2410.09024) — Evaluates harmful agent behavior under malicious instructions.
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

- [SWE-bench Leaderboard](https://www.swebench.com/) — Tracks submitted systems and coding-agent performance across SWE-bench variants.
  `leaderboard` `coding-agent` `benchmark`
- [GAIA Leaderboard](https://huggingface.co/spaces/gaia-benchmark/leaderboard) — Tracks general AI assistant benchmark submissions and results.
  `leaderboard` `general-agent` `benchmark`
- [OSWorld Leaderboard](https://os-world.github.io/) — Reports computer-use agent results on real desktop task suites.
  `leaderboard` `computer-use` `benchmark`
- [Terminal-Bench Leaderboard](https://www.tbench.ai/) — Tracks terminal-agent task-resolution performance and benchmark releases.
  `leaderboard` `terminal-agent` `benchmark`
- [BFCL Leaderboard](https://gorilla.cs.berkeley.edu/leaderboard.html) — Tracks function-calling benchmark performance across model providers.
  `leaderboard` `function-calling` `tool-use`
- [Inspect Evals Documentation](https://ukgovernmentbeis.github.io/inspect_evals/) — Documents runnable eval implementations for safety, coding, agent, and reasoning tasks.
  `docs` `benchmark-registry` `safety`

## Related Awesome Lists

- [Awesome-LLM-Eval](https://github.com/onejune2018/awesome-llm-eval) — Curates LLM evaluation methods, datasets, tools, and leaderboards.
  `awesome-list` `llm-evaluation` `related`
- [awesome-llm-agents](https://github.com/kaushikb11/awesome-llm-agents) — Collects LLM agent papers, projects, frameworks, and resources.
  `awesome-list` `llm-agents` `related`
- [awesome-ai-agents](https://github.com/e2b-dev/awesome-ai-agents) — Lists AI agent frameworks, tools, and examples across the ecosystem.
  `awesome-list` `ai-agents` `related`
- [awesome-production-machine-learning](https://github.com/EthicalML/awesome-production-machine-learning) — Useful for connecting agent evaluation to production ML monitoring and operations.
  `awesome-list` `production` `monitoring`

## Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a PR.

## License

This project is released under [CC0-1.0](LICENSE).
