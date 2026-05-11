# 评测框架

评测框架帮助团队把一次性检查变成可复现、可回归、可进入 CI 或生产监控的流程。

## 开源评测框架

开源评测框架适合本地运行、CI 集成和自定义任务评测。

- [Inspect AI](https://inspect.aisi.org.uk/) — 支持工具、scorer、sandbox 和日志的模型与 Agent 评测框架。
  `framework` `evals` `safety`
- [Inspect Evals](https://github.com/UKGovernmentBEIS/inspect_evals) — Inspect AI 的社区 benchmark 实现集合。
  `framework` `benchmark-registry` `safety`
- [OpenAI Evals](https://github.com/openai/evals) — 用于评测 LLM 系统的框架和 registry。
  `framework` `llm-evaluation` `regression`
- [DeepEval](https://deepeval.com/docs/introduction) — 类 pytest 的 LLM 和 Agent 评测框架。
  `framework` `testing` `agent-eval`
- [promptfoo](https://github.com/promptfoo/promptfoo) — 适合 CI 的 prompt、模型和 Agent 回归测试工具。
  `framework` `regression` `ci`
- [Ragas](https://docs.ragas.io/en/stable/) — 提供 RAG、工具调用和 agentic workflow 指标。
  `framework` `metrics` `rag`

## 平台和可观测性

平台和可观测性工具适合管理 trace、dataset、实验、人工反馈和线上评估。

- [LangSmith](https://docs.langchain.com/langsmith/home) — 支持 tracing、dataset、实验、人工评审和在线评测。
  `platform` `observability` `agent-eval`
- [Arize Phoenix](https://arize.com/docs/phoenix) — 面向 AI 应用的开源 tracing 和评测工作流。
  `platform` `observability` `evaluation`
- [Langfuse](https://langfuse.com/docs) — 开源可观测性、prompt 管理、评测和生产监控平台。
  `platform` `observability` `production`
- [Braintrust](https://www.braintrust.dev/docs) — 管理实验、scorer、dataset、trace 和 prompt 迭代。
  `platform` `experiments` `regression`

## 标准

标准化 trace 和 telemetry 字段能降低不同工具之间的数据迁移和对比成本。

- [OpenTelemetry GenAI Semantic Conventions](https://opentelemetry.io/docs/specs/semconv/gen-ai/) — GenAI 系统的标准 telemetry 字段。
  `standard` `observability` `telemetry`
- [OpenInference](https://github.com/Arize-ai/openinference) — LLM、RAG 和 Agent trace 的 instrumentation 约定。
  `standard` `observability` `tracing`
