# Benchmark

常用 Agent benchmark。

## 编程 Agent

看仓库理解、补丁生成和测试结果。

- [SWE-bench](https://www.swebench.com/SWE-bench/) — 把真实 GitHub issue 做成补丁任务。
  `benchmark` `coding-agent` `real-world-tasks`
- [SWE-bench Live](https://swe-bench-live.github.io/) — 更新的 issue 修复任务，适合担心数据污染时看。
  `benchmark` `coding-agent` `live`
- [LiveCodeBench](https://livecodebench.github.io/) — 较新的代码题，可以作为 coding 能力基线。
  `benchmark` `code-generation` `live`

## 浏览器和 Computer Use

看交互过程和状态变化。

- [WebArena](https://webarena.dev/) — 自托管网站任务，看浏览器 Agent 是否真的完成了状态变更。
  `benchmark` `browser-agent` `web`
- [WorkArena](https://servicenow.github.io/WorkArena/) — ServiceNow 场景里的企业知识工作任务。
  `benchmark` `browser-agent` `enterprise`
- [OSWorld](https://os-world.github.io/) — 真实桌面任务，结果用执行状态判断。
  `benchmark` `computer-use` `desktop-agent`
- [AndroidWorld](https://github.com/google-research/android_world) — Android app 交互任务，适合看移动端 Agent。
  `benchmark` `mobile-agent` `computer-use`

## 工具调用

看 API 选择、参数、调用顺序和执行结果。

- [Berkeley Function Calling Leaderboard](https://gorilla.cs.berkeley.edu/leaderboard.html) — 函数调用、参数、可执行性和多轮调用的综合测试。
  `benchmark` `function-calling` `tool-use`
- [tau2-bench / tau3-bench](https://github.com/sierra-research/tau2-bench) — 客服式多轮任务，带策略约束和数据库状态评分。
  `benchmark` `tool-use` `multi-turn`
- [ToolBench](https://github.com/OpenBMB/ToolBench) — 面向 API 使用的工具调用 benchmark。
  `benchmark` `tool-use` `api`

## 通用 Agent

混合推理、检索、文件、网页和工具调用。

- [GAIA](https://huggingface.co/gaia-benchmark) — 通用助手任务，经常需要工具、网页、文件和多步推理。
  `benchmark` `general-agent` `tool-use`
- [AgentBench](https://github.com/THUDM/AgentBench) — 多环境交互式 LLM Agent benchmark。
  `benchmark` `general-agent` `interactive`
- [Terminal-Bench](https://www.tbench.ai/) — 终端任务，适合看 shell 使用和调试能力。
  `benchmark` `terminal-agent` `tool-use`
