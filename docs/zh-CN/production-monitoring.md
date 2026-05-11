# 生产监控

上线后的问题：成本、延迟、工具调用、质量回退。

## 可观测性平台

先留 trace，再做评分、回归和人工 review。

- [LangSmith](https://docs.langchain.com/langsmith/home) — tracing、dataset、在线评测、annotation queue 和部署监控。
  `platform` `production` `monitoring`
- [Langfuse](https://langfuse.com/docs) — 开源 trace、prompt、eval、成本和延迟追踪。
  `platform` `production` `observability`
- [Arize Phoenix](https://arize.com/docs/phoenix) — 自托管 tracing、实验和评测工作流。
  `platform` `production` `observability`
- [Braintrust](https://www.braintrust.dev/docs) — 用 dataset 和 scorer 连接离线实验与生产日志。
  `platform` `production` `evalops`
- [Helicone](https://github.com/Helicone/helicone) — 请求日志、用户分析、模型用量、成本和延迟。
  `platform` `monitoring` `cost`

## 回归测试和在线评测

先发现“昨天能做，今天坏了”的问题。

- [LangSmith Online Evaluators](https://docs.langchain.com/langsmith/online-evaluations-llm-as-judge) — 对线上 trace 打分，监控质量和回归。
  `platform` `online-evals` `regression`
- [Langfuse Scores](https://langfuse.com/docs/scores/overview) — 在 trace 上记录人工、启发式和模型评分。
  `platform` `scores` `monitoring`
- [promptfoo Assertions](https://www.promptfoo.dev/docs/configuration/expected-outputs/) — 用断言写 CI 回归测试，可以是确定性规则，也可以是模型评分。
  `framework` `regression` `ci`

## 成本和 Telemetry

成本和延迟最好一开始就记。

- [LiteLLM Proxy](https://docs.litellm.ai/docs/proxy/quick_start) — 统一模型路由、预算、成本控制和日志。
  `tool` `cost` `routing`
- [OpenLLMetry](https://github.com/traceloop/openllmetry) — 面向 LLM 应用的 OpenTelemetry instrumentation。
  `tool` `observability` `telemetry`
- [OpenTelemetry GenAI Semantic Conventions](https://opentelemetry.io/docs/specs/semconv/gen-ai/) — 模型请求和 GenAI 操作的通用 telemetry 字段。
  `standard` `telemetry` `metrics`
