# 评测框架

把一次性检查变成可重复的实验或回归测试。

## 开源评测框架

适合搭本地 eval 或 CI 流程。

- [Inspect AI](https://inspect.aisi.org.uk/) — 带工具、sandbox、scorer 和日志查看器的 eval 框架。
  `framework` `evals` `safety`
- [Inspect Evals](https://github.com/UKGovernmentBEIS/inspect_evals) — Inspect 生态里的现成 eval 集合。
  `framework` `benchmark-registry` `safety`
- [OpenAI Evals](https://github.com/openai/evals) — 可参考其 eval 组织方式和 registry 设计。
  `framework` `llm-evaluation` `regression`
- [DeepEval](https://deepeval.com/docs/introduction) — 类 pytest 的 LLM 和 Agent 评测框架。
  `framework` `testing` `agent-eval`
- [promptfoo](https://github.com/promptfoo/promptfoo) — 适合放进 CI 的 prompt、模型和 Agent 回归测试。
  `framework` `regression` `ci`
- [Ragas](https://docs.ragas.io/en/stable/) — RAG、工具调用和 agentic workflow 相关指标。
  `framework` `metrics` `rag`

## 平台和可观测性

适合管理 trace、dataset、线上样本和人工反馈。

- [LangSmith](https://docs.langchain.com/langsmith/home) — tracing、dataset、实验、人工评审和在线评测。
  `platform` `observability` `agent-eval`
- [Arize Phoenix](https://arize.com/docs/phoenix) — 开源 tracing、实验和评测工作流。
  `platform` `observability` `evaluation`
- [Langfuse](https://langfuse.com/docs) — 开源 trace、prompt、eval、成本和延迟监控。
  `platform` `observability` `production`
- [Braintrust](https://www.braintrust.dev/docs) — 实验、scorer、dataset、trace 和 prompt 迭代。
  `platform` `experiments` `regression`

## 标准

适合统一 trace 和 telemetry 字段。

- [OpenTelemetry GenAI Semantic Conventions](https://opentelemetry.io/docs/specs/semconv/gen-ai/) — GenAI 调用的标准 telemetry 字段。
  `standard` `observability` `telemetry`
- [OpenInference](https://github.com/Arize-ai/openinference) — LLM、RAG 和 Agent trace 的 instrumentation 约定。
  `standard` `observability` `tracing`
