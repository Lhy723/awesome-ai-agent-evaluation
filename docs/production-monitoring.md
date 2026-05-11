# Production Monitoring

Production agent evaluation is about continuously tracking quality, cost, latency, safety, and regressions after launch.

## Observability Platforms

- [LangSmith](https://docs.langchain.com/langsmith/home) — Tracing, datasets, online evaluators, annotation queues, and deployment monitoring.
  `platform` `production` `monitoring`
- [Langfuse](https://langfuse.com/docs) — Open-source tracing, prompt management, evaluations, cost, and latency tracking.
  `platform` `production` `observability`
- [Arize Phoenix](https://arize.com/docs/phoenix) — Self-hosted tracing, experiments, and evaluation workflows.
  `platform` `production` `observability`
- [Braintrust](https://www.braintrust.dev/docs) — Connects offline experiments and production logs through datasets and scorers.
  `platform` `production` `evalops`
- [Helicone](https://github.com/Helicone/helicone) — Request logging, user analytics, model usage, cost, and latency tracking.
  `platform` `monitoring` `cost`

## Regression and Online Evaluation

- [LangSmith Online Evaluators](https://docs.langchain.com/langsmith/online-evaluations-llm-as-judge) — Scores live traces to monitor quality and detect regressions.
  `platform` `online-evals` `regression`
- [Langfuse Scores](https://langfuse.com/docs/scores/overview) — Tracks human, heuristic, and model-generated scores over traces.
  `platform` `scores` `monitoring`
- [promptfoo Assertions](https://www.promptfoo.dev/docs/configuration/expected-outputs/) — Expresses deterministic and model-graded assertions for CI regression tests.
  `framework` `regression` `ci`

## Cost and Telemetry

- [LiteLLM Proxy](https://docs.litellm.ai/docs/proxy/quick_start) — Unified routing, budgets, spend controls, and logging for model calls.
  `tool` `cost` `routing`
- [OpenLLMetry](https://github.com/traceloop/openllmetry) — OpenTelemetry instrumentation for LLM applications.
  `tool` `observability` `telemetry`
- [OpenTelemetry GenAI Semantic Conventions](https://opentelemetry.io/docs/specs/semconv/gen-ai/) — Common telemetry fields for model requests and GenAI operations.
  `standard` `telemetry` `metrics`
