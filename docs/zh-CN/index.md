# Awesome AI Agent Evaluation

<p align="center">
  <a href="../../README.zh-CN.md">仓库 README</a> ·
  <a href="../index.md">English</a>
</p>

这是项目的短入口。完整清单在 README；这里适合直接跳到 benchmark、框架、生产监控或论文。

## 快速入口

<table>
  <tr>
    <th>页面</th>
    <th>适合用来找什么</th>
  </tr>
  <tr>
    <td><a href="benchmarks.md">Benchmarks</a></td>
    <td>编程、浏览器、computer-use、tool-use 和通用 Agent benchmark。</td>
  </tr>
  <tr>
    <td><a href="frameworks.md">Frameworks</a></td>
    <td>评测框架、trace 工具和可观测性平台。</td>
  </tr>
  <tr>
    <td><a href="production-monitoring.md">Production Monitoring</a></td>
    <td>质量检查、成本、延迟、回归和在线评测。</td>
  </tr>
  <tr>
    <td><a href="papers.md">Papers</a></td>
    <td>主要 Agent 评测资源背后的方法论文。</td>
  </tr>
</table>

## 评测地图

| 问题 | 从这里开始 |
| --- | --- |
| 这个 Agent 会写代码吗？ | Benchmark 和 coding-agent 资源 |
| 这个 Agent 能正确调用工具吗？ | Function-calling 和 tool-use benchmark |
| 这个 Agent 会浏览网页吗？ | Browser 和 web-agent benchmark |
| 这个 Agent 失败后能恢复吗？ | 可靠性和回归测试资源 |
| 我能在生产环境监控它吗？ | 生产监控资源 |
| 这个 Agent 足够安全吗？ | 安全与鲁棒性 benchmark |

## 仓库

完整资源列表见 [README.zh-CN.md](../../README.zh-CN.md) 和 [README.md](../../README.md)。

## 阅读建议

- 先看任务，不要先看工具。
- 榜单分数只能当线索，不能当结论。
- 优先看任务和评分方式说清楚的资源。
- 做生产评测时，trace 和回归测试通常不比离线分数次要。
