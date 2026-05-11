# Awesome AI Agent Evaluation

![Awesome AI Agent Evaluation social preview](assets/social-preview.png)

<p align="center">
  <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome"></a>
  <a href="README.md">English</a>
</p>

AI Agent 评测资源地图：benchmark、评测框架、论文、数据集、回归测试和生产监控。

Agent 评测现在还很分散。有些资源是学术 benchmark，有些是工程测试框架，有些是可观测性工具，还有一些是只有在真实用户 trace 出来以后才有意义的生产实践。

这个列表把这些东西放到一起，但不追求“大而全”。更看重的是它能不能回答具体工程问题：测了什么、怎么打分、哪里失败、离真实使用还有多远。

<table>
  <tr>
    <th>会收</th>
    <th>不收</th>
  </tr>
  <tr>
    <td>任务和评分方式清楚的 benchmark</td>
    <td>泛泛的 Agent demo</td>
  </tr>
  <tr>
    <td>能跑 eval 或跟踪 eval 的框架</td>
    <td>没有评测方法的 prompt 集合</td>
  </tr>
  <tr>
    <td>方法能复用的论文和报告</td>
    <td>没有技术细节的营销页</td>
  </tr>
</table>

## 从哪里看

<table>
  <tr>
    <th>如果你关心...</th>
    <th>建议先看</th>
  </tr>
  <tr>
    <td>软件工程任务</td>
    <td><a href="README.md#coding-agent-evaluation">Coding Agent Evaluation</a></td>
  </tr>
  <tr>
    <td>网站和 UI 操作</td>
    <td><a href="README.md#browser--web-agent-evaluation">Browser / Web Agent Evaluation</a></td>
  </tr>
  <tr>
    <td>API 和函数调用</td>
    <td><a href="README.md#tool-use-and-function-calling">Tool-Use and Function Calling</a></td>
  </tr>
  <tr>
    <td>回归测试和失败恢复</td>
    <td><a href="README.md#reliability--failure-recovery">Reliability & Failure Recovery</a></td>
  </tr>
  <tr>
    <td>Prompt injection 和有害行为</td>
    <td><a href="README.md#safety--robustness">Safety & Robustness</a></td>
  </tr>
  <tr>
    <td>日志、trace、成本和质量漂移</td>
    <td><a href="README.md#production-monitoring">Production Monitoring</a></td>
  </tr>
</table>

## 分类说明

<details open>
<summary>展开分类</summary>

- [Evaluation Basics](README.md#evaluation-basics) / 评测基础：从产品问题、任务设计、评分方式和 trace 分析角度理解 Agent eval。
- [Benchmarks](README.md#benchmarks) / 基准测试：比较不同模型或系统在真实任务、交互环境和工具调用中的表现。
- [Evaluation Frameworks](README.md#evaluation-frameworks) / 评测框架：把一次性检查变成可复现、可回归、可进入 CI 或生产监控的流程。
- [Coding Agent Evaluation](README.md#coding-agent-evaluation) / 编程 Agent 评测：真实代码仓库、issue 修复、测试通过率、上下文理解和代码编辑质量。
- [Browser / Web Agent Evaluation](README.md#browser--web-agent-evaluation) / 浏览器与 Web Agent 评测：网页导航、视觉理解、表单操作、状态变更和任务完成度。
- [Tool-Use and Function Calling](README.md#tool-use-and-function-calling) / 工具调用与函数调用：API 选择、参数构造、多轮调用、状态更新和执行结果正确性。
- [Multi-Agent Evaluation](README.md#multi-agent-evaluation) / 多 Agent 评测：协作、角色分工、通信成本、任务分解和最终产出质量。
- [Safety & Robustness](README.md#safety--robustness) / 安全与鲁棒性：prompt injection、越权工具调用、有害请求、数据泄露和对抗场景。
- [Reliability & Failure Recovery](README.md#reliability--failure-recovery) / 可靠性与失败恢复：出错后的重试、修正、状态恢复、回归风险和长期稳定性。
- [Cost, Latency, and Efficiency](README.md#cost-latency-and-efficiency) / 成本、延迟与效率：token、模型调用、工具调用、耗时和预算控制。
- [Human Evaluation Rubrics](README.md#human-evaluation-rubrics) / 人工评审标准：给 trace、对话、工具调用和最终结果打分。
- [Production Monitoring](README.md#production-monitoring) / 生产监控：上线后的 trace、质量评分、成本、延迟、失败率、人工反馈和质量漂移。
- [Papers](README.md#papers) / 论文：主要 benchmark 和方法论来源。
- [Datasets](README.md#datasets) / 数据集：可用于训练、评测或复现实验的 Agent 任务数据。
- [Reports & Case Studies](README.md#reports--case-studies) / 报告与案例：榜单结果、实际系统表现和评测实践。
- [Related Awesome Lists](README.md#related-awesome-lists) / 相关 Awesome 列表：LLM eval、Agent 框架和生产机器学习等邻近领域。

</details>

轻量文档站中文入口见 [docs/zh-CN/index.md](docs/zh-CN/index.md)。完整资源清单仍维护在英文 [README.md](README.md)，资源名称和官方链接尽量保持原文，避免翻译造成检索困难。

## 贡献

欢迎提交 PR 或 issue。请先阅读 [CONTRIBUTING.zh-CN.md](CONTRIBUTING.zh-CN.md)，里面有收录范围、条目格式、标签和质量门槛。

优先推荐这些资源：

- 和 AI Agent 评测直接相关
- 官方链接稳定可访问
- 能帮助读者做技术判断
- 有明确 benchmark、数据集、工具、论文、报告或生产实践价值

不建议提交这些资源：

- 泛 LLM 工具，但没有 Agent 评测重点
- 低质量博客或 SEO 页面
- 纯营销页
- 重复资源
- 只有 prompt，没有评测方法

## License

本项目使用 [CC0-1.0](LICENSE) 发布。
