# Benchmark

本页整理最适合比较 AI Agent 能力的 benchmark 家族。

## 编程 Agent

编程 Agent benchmark 关注真实代码仓库、issue 修复、测试通过和代码编辑能力。

- [SWE-bench](https://www.swebench.com/SWE-bench/) — 评测 coding agent 解决真实 GitHub issue 的能力。
  `benchmark` `coding-agent` `real-world-tasks`
- [SWE-bench Live](https://swe-bench-live.github.io/) — 使用更新的软件工程任务降低数据污染风险。
  `benchmark` `coding-agent` `live`
- [LiveCodeBench](https://livecodebench.github.io/) — 提供更新的代码生成任务，用作模型和 Agent 基线。
  `benchmark` `code-generation` `live`

## 浏览器和 Computer Use

浏览器和 computer-use benchmark 关注网页、桌面或移动环境中的真实交互任务。

- [WebArena](https://webarena.dev/) — 用自托管真实网站评测浏览器 Agent 的任务完成能力。
  `benchmark` `browser-agent` `web`
- [WorkArena](https://servicenow.github.io/WorkArena/) — 评测浏览器 Agent 在企业知识工作场景中的表现。
  `benchmark` `browser-agent` `enterprise`
- [OSWorld](https://os-world.github.io/) — 评测多模态 computer-use Agent 完成真实桌面任务的能力。
  `benchmark` `computer-use` `desktop-agent`
- [AndroidWorld](https://github.com/google-research/android_world) — 用 Android app 交互任务评测移动 Agent。
  `benchmark` `mobile-agent` `computer-use`

## 工具调用

工具调用 benchmark 关注 API 选择、参数构造、多轮调用和执行结果正确性。

- [Berkeley Function Calling Leaderboard](https://gorilla.cs.berkeley.edu/leaderboard.html) — 比较模型在函数调用、API、多轮调用和可执行性上的能力。
  `benchmark` `function-calling` `tool-use`
- [tau2-bench / tau3-bench](https://github.com/sierra-research/tau2-bench) — 在客服任务中评测多轮对话、策略遵循和工具调用。
  `benchmark` `tool-use` `multi-turn`
- [ToolBench](https://github.com/OpenBMB/ToolBench) — 面向 API 使用的工具调用 benchmark。
  `benchmark` `tool-use` `api`

## 通用 Agent

通用 Agent benchmark 关注跨工具、跨环境、跨任务类型的综合能力。

- [GAIA](https://huggingface.co/gaia-benchmark) — 评测需要推理、工具和外部资源的通用助手任务。
  `benchmark` `general-agent` `tool-use`
- [AgentBench](https://github.com/THUDM/AgentBench) — 多环境交互式 LLM Agent benchmark。
  `benchmark` `general-agent` `interactive`
- [Terminal-Bench](https://www.tbench.ai/) — 评测使用 shell 的终端 Agent 完成任务的能力。
  `benchmark` `terminal-agent` `tool-use`
