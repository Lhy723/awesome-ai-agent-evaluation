# 贡献指南

感谢你帮助完善 Awesome AI Agent Evaluation。

语言：[English](CONTRIBUTING.md) | 中文

这是有人维护的阅读清单，不是链接仓库。

## 收录范围

可以收这些：

- Benchmark 和排行榜
- 评测框架和测试 harness
- 数据集和任务集
- 论文和技术报告
- Agent 可靠性、回归测试和监控实践
- 安全、鲁棒性、红队测试和 prompt injection 评测
- 人工评审 rubric 和生产质量流程

## 不收录什么？

这些先别放：

- 没有 Agent 评测重点的泛 LLM 工具
- 低质量博客或内容很薄的 SEO 页面
- 没有技术实质的营销页
- 没有历史价值的死亡项目或长期无人维护项目
- 同一分类里已经收录的重复资源
- 只有 prompt、但没有评测方法的 prompt 集合

## 条目格式

条目统一用这个格式：

```md
- [Name](https://example.com) — Short explanation of what it evaluates and why it matters.
  `tag-one` `tag-two`
```

描述至少回答一个问题：

- 它评测了 Agent 的什么行为？
- 它覆盖了什么任务、环境或失败模式？
- 实践者为什么会用它？

不要只复述项目 tagline。说明它适合评什么、放在哪个场景里。

## 质量门槛

只收能帮读者评测 Agent 的资源。

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
    <td>任务、指标或流程清楚的资源</td>
    <td>不说明如何评测的泛 Agent 工具</td>
  </tr>
  <tr>
    <td>能说明“测了什么”的简短描述</td>
    <td>营销话术和模糊判断</td>
  </tr>
</table>

提交前检查一下：

- URL 是官方、稳定、可访问的链接。
- 资源和 AI Agent 评测直接相关。
- 描述简短、中立、有帮助。
- 条目放在最有用的分类里。
- 没有重复收录。

## 推荐标签

使用 2-4 个轻量标签：

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
