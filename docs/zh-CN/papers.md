# 论文

先看任务定义和评分方式，再看榜单。

## 通用和工具型 Agent

推理、工具调用、多轮交互和外部资源。

- [AgentBench: Evaluating LLMs as Agents](https://arxiv.org/abs/2308.03688) — 多环境交互式 LLM Agent benchmark。
  `paper` `general-agent` `benchmark`
- [GAIA: A Benchmark for General AI Assistants](https://arxiv.org/abs/2311.12983) — 高难度助手任务，常需要工具、网页和文件。
  `paper` `general-agent` `tool-use`
- [tau-bench: A Benchmark for Tool-Agent-User Interaction in Real-World Domains](https://arxiv.org/abs/2406.12045) — 客服式多轮场景，带工具、策略和用户模拟。
  `paper` `tool-use` `multi-turn`
- [API-Bank: A Comprehensive Benchmark for Tool-Augmented LLMs](https://arxiv.org/abs/2304.08244) — API 增强 LLM 的评测和训练。
  `paper` `tool-use` `api`

## 编程 Agent

仓库上下文、补丁生成和测试验证。

- [SWE-bench: Can Language Models Resolve Real-World GitHub Issues?](https://arxiv.org/abs/2310.06770) — 仓库级 issue-to-patch 评测的代表性工作。
  `paper` `coding-agent` `benchmark`

## 浏览器和 Computer-use Agent

网页、桌面、截图、状态变化和执行结果。

- [WebArena: A Realistic Web Environment for Building Autonomous Agents](https://arxiv.org/abs/2307.13854) — 自托管真实网站环境，适合看浏览器 Agent。
  `paper` `browser-agent` `benchmark`
- [VisualWebArena: Evaluating Multimodal Agents on Realistic Visual Web Tasks](https://arxiv.org/abs/2401.13649) — 在 web-agent 任务里加入视觉 grounding。
  `paper` `browser-agent` `multimodal`
- [WorkArena: How Capable Are Web Agents at Solving Common Knowledge Work Tasks?](https://arxiv.org/abs/2403.07718) — 企业知识工作场景里的 web-agent 评测。
  `paper` `browser-agent` `enterprise`
- [OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments](https://arxiv.org/abs/2404.07972) — 真实桌面任务，用执行结果评分。
  `paper` `computer-use` `benchmark`

## 安全

工具权限、外部内容和多步执行带来的安全问题。

- [AgentDojo: A Dynamic Environment to Evaluate Prompt Injection Attacks and Defenses for LLM Agents](https://arxiv.org/abs/2406.13352) — 工具型 Agent 的 prompt-injection 攻防评测。
  `paper` `safety` `prompt-injection`
- [AgentHarm: A Benchmark for Measuring Harmfulness of LLM Agents](https://arxiv.org/abs/2410.09024) — Agent 场景下的有害行为 benchmark。
  `paper` `safety` `agent`
