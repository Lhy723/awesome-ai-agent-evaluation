# 贡献指南

感谢你帮助完善 Awesome AI Agent Evaluation。

语言：[English](CONTRIBUTING.md) | 中文

请把它当成一个有人维护的阅读清单，而不是链接仓库。如果一个链接不能帮助别人评测 Agent，它大概率不该放进来。

## 收录范围

我们接受和 AI Agent 评测直接相关的资源，包括：

- Benchmark 和排行榜
- 评测框架和测试 harness
- 数据集和任务集
- 论文和技术报告
- Agent 可靠性、回归测试和监控实践
- 安全、鲁棒性、红队测试和 prompt injection 评测
- 人工评审 rubric 和生产质量流程

## 不收录什么？

请避免提交以下内容：

- 没有 Agent 评测重点的泛 LLM 工具
- 低质量博客或内容很薄的 SEO 页面
- 没有技术实质的营销页
- 没有历史价值的死亡项目或长期无人维护项目
- 同一分类里已经收录的重复资源
- 只有 prompt、但没有评测方法的 prompt 集合

## 条目格式

请使用下面的条目格式：

```md
- [Name](https://example.com) — Short explanation of what it evaluates and why it matters.
  `tag-one` `tag-two`
```

好的描述至少应该回答下面一个问题：

- 它评测了 Agent 的什么行为？
- 它覆盖了什么任务、环境或失败模式？
- 实践者为什么会用它？

请避免只复述项目 tagline。真正有用的是判断：这个资源适合评什么、放在哪个场景里。

## 质量门槛

只有当资源能帮助读者更清楚地评测 Agent 时，才应该收录。

<table>
  <tr>
    <th>优先收录</th>
    <th>尽量避免</th>
  </tr>
  <tr>
    <td>官方文档、论文、仓库、数据集或排行榜</td>
    <td>没有技术增量的二手总结</td>
  </tr>
  <tr>
    <td>任务、指标或评测流程清楚的资源</td>
    <td>不说明如何评测的泛 Agent 工具</td>
  </tr>
  <tr>
    <td>能说明“测了什么”的简短描述</td>
    <td>营销话术和模糊判断</td>
  </tr>
</table>

提交前请检查：

- URL 是官方、稳定、可访问的链接。
- 资源和 AI Agent 评测直接相关。
- 描述简短、中立、有帮助。
- 条目放在最有用的分类里。
- 资源没有被重复收录。

## 推荐标签

请使用 2-4 个轻量标签：

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

## Pull Request

小 PR 更容易 review。如果一次性增加很多资源，请按分类整理，并尽量保持每条说明的长度和语气一致。
