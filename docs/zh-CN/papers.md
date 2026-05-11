# 论文

这些论文适合理解 Agent benchmark 如何设计、实际测量了什么、以及有哪些局限。

## 通用和工具型 Agent

通用和工具型 Agent 论文关注跨任务推理、工具调用、多轮交互和真实场景约束。

- [AgentBench: Evaluating LLMs as Agents](https://arxiv.org/abs/2308.03688) — 提出多环境交互式 LLM Agent benchmark。
  `paper` `general-agent` `benchmark`
- [GAIA: A Benchmark for General AI Assistants](https://arxiv.org/abs/2311.12983) — 评测需要推理和工具的高难度助手任务。
  `paper` `general-agent` `tool-use`
- [tau-bench: A Benchmark for Tool-Agent-User Interaction in Real-World Domains](https://arxiv.org/abs/2406.12045) — 在策略约束客服对话中评测工具型 Agent。
  `paper` `tool-use` `multi-turn`
- [API-Bank: A Comprehensive Benchmark for Tool-Augmented LLMs](https://arxiv.org/abs/2304.08244) — 研究 API 增强 LLM 的评测和训练。
  `paper` `tool-use` `api`

## 编程 Agent

编程 Agent 论文关注真实仓库 issue、补丁生成、测试执行和软件工程任务完成度。

- [SWE-bench: Can Language Models Resolve Real-World GitHub Issues?](https://arxiv.org/abs/2310.06770) — 提出仓库级 issue 修复评测。
  `paper` `coding-agent` `benchmark`

## 浏览器和 Computer-use Agent

浏览器和 computer-use 论文关注网页、桌面、视觉环境和真实交互任务。

- [WebArena: A Realistic Web Environment for Building Autonomous Agents](https://arxiv.org/abs/2307.13854) — 提出用于浏览器 Agent 评测的自托管真实网站环境。
  `paper` `browser-agent` `benchmark`
- [VisualWebArena: Evaluating Multimodal Agents on Realistic Visual Web Tasks](https://arxiv.org/abs/2401.13649) — 在 web-agent 评测中加入视觉 grounding。
  `paper` `browser-agent` `multimodal`
- [WorkArena: How Capable Are Web Agents at Solving Common Knowledge Work Tasks?](https://arxiv.org/abs/2403.07718) — 评测 web Agent 完成企业任务的能力。
  `paper` `browser-agent` `enterprise`
- [OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments](https://arxiv.org/abs/2404.07972) — 用执行式检查评测桌面 computer-use Agent。
  `paper` `computer-use` `benchmark`

## 安全

安全论文关注 prompt injection、有害请求、越权行为和 Agent 特有攻击面。

- [AgentDojo: A Dynamic Environment to Evaluate Prompt Injection Attacks and Defenses for LLM Agents](https://arxiv.org/abs/2406.13352) — 衡量 prompt-injection 攻击下的 utility-security tradeoff。
  `paper` `safety` `prompt-injection`
- [AgentHarm: A Benchmark for Measuring Harmfulness of LLM Agents](https://arxiv.org/abs/2410.09024) — 测试 agentic 场景中的有害行为。
  `paper` `safety` `agent`
