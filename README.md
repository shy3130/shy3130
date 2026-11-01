<picture>
  <source media="(max-width: 600px) and (prefers-color-scheme: dark)" srcset="assets/profile-mobile-dark.svg">
  <source media="(max-width: 600px)" srcset="assets/profile-mobile-light.svg">
  <source media="(prefers-color-scheme: dark)" srcset="assets/profile-dark.svg">
  <img src="assets/profile-light.svg" width="100%" alt="wshy — 把想法写成工具。量化研究与 AI 编程工具。">
</picture>

# 你好，我是 wshy

我做 **A 股量化研究工具**，也为 **AI 编程工作流**写插件。喜欢把日常遇到的问题，做成可以自己部署、继续扩展的开源项目。

[TSP 工作台](#user-content-tick-stock-panel) / [Codex 用量](#user-content-codex-token-monitor) / [DSH 额度](#user-content-dsh-quota) / [更多工具](#user-content-更多工具) / [支持](#user-content-支持与交流)

## 量化工作台

### [tick-stock-panel](https://github.com/shy3130/tick-stock-panel)

**把策略、回测、监控与复盘，放进同一个研究工作台。**

支持自定义策略、因子挖掘、实时监控与 AI 助手；通过 Open API 和 MCP 连接自己的工具。Docker 单容器部署，数据保存在本地，数据源可按需扩展。

<a href="https://github.com/shy3130/tick-stock-panel">
  <img src="https://raw.githubusercontent.com/shy3130/tick-stock-panel/main/screenshots/%E7%9C%8B%E6%9D%BF.png" width="100%" alt="tick-stock-panel 实际界面：市场概览、情绪雷达、板块热度与监控信号。截图为历史界面，不是实时行情。">
</a>

[项目与部署指南](https://github.com/shy3130/tick-stock-panel#readme) · [官方网站](https://tsp.shy313.com) · [更多界面](https://github.com/shy3130/tick-stock-panel/blob/main/screenshots/README.md)

<sub>仅供学习研究，不作为投资或看盘软件；不提供 AI 荐股或涨停预测。</sub>

## 新插件

围绕 AI 编程时最常问的两件事：**用了多少，剩下多少。**

### [Codex Token Monitor](https://github.com/shy3130/codex-token-monitor)

**看清本机 Codex 的 Token 用量、模型速度和参考费用。**

按今日、7 日、30 日查看消耗，比较各模型的 Token、平均 TPS 和 API 参考费用，也能回看单次请求。使用 Python 标准库与本地 SQLite，支持浏览器面板和 MCP 接入。

<a href="https://github.com/shy3130/codex-token-monitor">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/shy3130/codex-token-monitor/main/docs/screenshots/models-v1.6.1-dark.png">
    <img src="https://raw.githubusercontent.com/shy3130/codex-token-monitor/main/docs/screenshots/models-v1.6.1-light.png" width="640" alt="Codex Token Monitor 模型明细：并排比较 Token 总量、API 参考费用与平均 TPS。图中使用虚构演示数据。">
  </picture>
</a>

<sub>实际界面，使用虚构演示数据。费用为 API 标准价格估算，不代表实际账单或剩余额度。</sub>

[查看项目](https://github.com/shy3130/codex-token-monitor) · [安装与 MCP 接入](https://github.com/shy3130/codex-token-monitor/blob/main/docs/getting-started.md) · [English](https://github.com/shy3130/codex-token-monitor/blob/main/README.en.md)

### [dsh-quota](https://github.com/shy3130/dsh-quota)

**在 DeepSeek Harness 输入框旁，随时查看额度与消耗。**

跟随当前模型切换厂商，点击状态栏即可查看剩余额度、重置倒计时和 Token 用量。支持 **智谱 GLM、OpenCode Go、Kimi For Coding、小米 Token 套餐与 DeepSeek 官方**。

<a href="https://github.com/shy3130/dsh-quota">
  <img src="https://raw.githubusercontent.com/shy3130/dsh-quota/main/docs/images/hero.png" width="100%" alt="dsh-quota 实际界面：GLM、OpenCode Go 的额度窗口，以及 DeepSeek 余额与消耗。截图数值为当时状态，不是实时额度。">
</a>

<sub>项目公开截图，数值为截图时的状态。支持桌面与窄屏布局。</sub>

[查看项目](https://github.com/shy3130/dsh-quota) · [安装与配置](https://github.com/shy3130/dsh-quota#安装) · [版本记录](https://github.com/shy3130/dsh-quota/releases)

## 更多工具

**[zcode-tps-monitor](https://github.com/shy3130/zcode-tps-monitor)**<br>
ZCode 会话级 Token 速率监控。读取 usage 数据库，在调用工具的回复末尾展示本轮 tok/s；提供多会话大屏、`/tps` 命令和 MCP 工具。

**[stealth-browser-skill](https://github.com/shy3130/stealth-browser-skill)**<br>
面向 AI Agent 的反检测浏览器自动化技能。

## 平时在用

**构建**　Python / TypeScript / JavaScript / React / FastAPI<br>
**数据**　Polars / DuckDB / SQLite / Parquet<br>
**连接**　Open API / MCP / Docker / GitHub Actions

## 支持与交流

项目的问题和想法，欢迎到对应仓库提 Issue。觉得有用，也可以留一个 Star，或通过 [爱发电](https://afdian.com/a/shy3130) 支持后续开发。

感谢 **[RunningHub](https://www.runninghub.ai/zh-cn/call-api?source=github&inviteCode=edt5wh7c)** 对开源项目的支持。

[了解 RunningHub API](https://www.runninghub.ai/zh-cn/call-api?source=github&inviteCode=edt5wh7c)

<details>
<summary>GitHub 贡献记录</summary>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/shy3130/shy3130/output/github-snake-dark.svg">
  <img src="https://raw.githubusercontent.com/shy3130/shy3130/output/github-snake.svg" width="100%" alt="shy3130 的 GitHub 贡献记录动画">
</picture>

[查看完整贡献记录](https://github.com/shy3130?tab=overview)

</details>
