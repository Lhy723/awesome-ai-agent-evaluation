# Contributing

Thanks for helping improve Awesome AI Agent Evaluation.

Language: English | [Chinese](CONTRIBUTING.zh-CN.md)

Please treat this as a maintained reading list, not a dumping ground. If a link does not help someone evaluate an agent, it probably does not belong here.

## What belongs here?

We accept resources directly related to evaluating AI agents, including:

- Benchmarks and leaderboards
- Evaluation frameworks and test harnesses
- Datasets and task suites
- Papers and technical reports
- Agent reliability, regression, and monitoring practices
- Safety, robustness, red-teaming, and prompt-injection evaluations
- Human review rubrics and production quality workflows

## What does not belong here?

Please avoid:

- Generic LLM tools with no agent evaluation focus
- Low-quality blog posts or thin SEO pages
- Marketing pages without technical substance
- Dead or unmaintained projects with no historical value
- Duplicate resources already listed in the same category
- Pure prompt collections unless they include an evaluation method

## Entry format

Use this format:

```md
- [Name](https://example.com) — Short explanation of what it evaluates and why it matters.
  `tag-one` `tag-two`
```

Good descriptions answer at least one of these questions:

- What agent behavior does this evaluate?
- What task, environment, or failure mode does it cover?
- Why would a practitioner use it?

Avoid descriptions that only repeat the project tagline. The useful part is the judgment: what this resource is good for, and where it fits.

## Quality bar

A resource should be included only if it helps readers evaluate an agent more clearly.

<table>
  <tr>
    <th>Prefer</th>
    <th>Avoid</th>
  </tr>
  <tr>
    <td>Official docs, papers, repositories, datasets, or leaderboards</td>
    <td>Second-hand summaries that add no technical value</td>
  </tr>
  <tr>
    <td>Clear tasks, metrics, or evaluation workflows</td>
    <td>Agent tools that do not say how to evaluate anything</td>
  </tr>
  <tr>
    <td>Concise descriptions of what is being tested</td>
    <td>Marketing copy or vague claims</td>
  </tr>
</table>

Before submitting, please check:

- The URL is official, stable, and working.
- The resource is directly related to AI agent evaluation.
- The description is short, neutral, and helpful.
- The item is placed in the most useful category.
- The resource is not already listed.

## Preferred tags

Use 2-4 lightweight tags:

```text
benchmark
framework
dataset
paper
coding-agent
browser-agent
tool-use
function-calling
computer-use
safety
robustness
monitoring
human-eval
production
open-source
commercial
```

## Pull requests

Small PRs are easier to review. If you are adding many resources, group them by category and keep each description consistent with the existing style.
