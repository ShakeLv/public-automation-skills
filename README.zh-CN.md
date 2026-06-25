# Public Automation Skills

[English](README.md) / [中文](README.zh-CN.md)

这是一个公开安全版 Codex skills 仓库，整理了四类可复用的自动化工作流：内容生产、GitHub outreach、数据管理和内部日报。

这个仓库**不是**生产环境自动化仓库。它只包含可公开阅读的 agent 操作说明和安全边界，不包含生产脚本、账号配置或私有数据。

目标很简单：别人复制一个 skill 文件夹，提供公开信息或脱敏数据，就可以得到有用的输出，而且不需要知道原始的私有环境。

## Workflows

### Content Production Pipeline

把公开 SEO / AI 趋势信号转成可以发布的内容资产。

Skills：`trend-signal-tracker`，`wix-blog-pipeline`

安全输入：公开趋势链接、脱敏选题快照、文章大纲、公开参考链接。

输出：排序后的选题、内容角度、SEO 元信息，以及 Wix-ready 发布包。

### GitHub Outreach

寻找 GitHub-first 的分发机会，并准备可公开提交的材料。

Skill：`github-outreach-ops`

安全输入：公开 GitHub 仓库链接、公开产品介绍、awesome-list 规则、提交规范。

输出：筛选后的目标列表、推荐提交路径、PR 或 listing 文案、进度追踪表。

### Data Management

在不连接生产系统的前提下，分析获客、收入和订阅数据。

Skills：`ads-health-monitor`，`stripe-ops-review`，`growth-data-analysis`

安全输入：脱敏 Google Ads 导出、脱敏 Stripe 导出、聚合增长数据表、人工整理的指标摘要。

输出：指标快照、异常点、可能原因、数据质量备注和待执行动作队列。

### Internal Daily Brief

把每天的市场、广告、收入、内容和 outreach 变化整理成 Slack-ready 日报。

Skill：`daily-growth-brief`

安全输入：脱敏日报素材、公开市场信号、聚合 Ads / Stripe 变化、内容进度、outreach 进度。

输出：Slack-ready 日报、值得关注的数据、待办动作、阻塞项和数据质量备注。

## Quick Start

先选工作流，再加载对应的 skill 文件夹。

```text
Use trend-signal-tracker to review these public AI/SEO trend candidates and pick five article angles.
```

```text
Use github-outreach-ops to qualify these GitHub awesome-list repositories and prepare safe PR copy.
```

```text
Use ads-health-monitor and stripe-ops-review to review these sanitized exports and prepare today's action queue.
```

```text
Use daily-growth-brief to turn today's market, Ads, Stripe, content, and outreach snapshots into a Slack-ready report.
```

## Skills

| Skill | 用途 |
| --- | --- |
| `trend-signal-tracker` | 监控公开 SEO / AI 趋势信号，去重、评分，并产出内容计划。 |
| `wix-blog-pipeline` | 把内容想法整理成 Wix-ready 发布包。 |
| `ads-health-monitor` | 基于脱敏 Google Ads 数据做账户健康检查和动作建议。 |
| `stripe-ops-review` | 分析脱敏 Stripe 收入、订阅、流失和 cohort 数据。 |
| `growth-data-analysis` | 把脱敏增长数据转成结论和下一步实验。 |
| `github-outreach-ops` | 查找、筛选并追踪 GitHub-first outreach 机会。 |
| `daily-growth-brief` | 把脱敏市场、广告、收入和增长信息整理成 Slack-ready 日报。 |

## Safety Model

这些 skills 面向公开使用和作品展示。

它们不包含：

- API key、token、cookie、OAuth secret 或任何凭证
- 生产账号 ID、客户 ID、账单 ID 或后台链接
- 私有数据库 schema、内部 endpoint、服务器路径或本地路径
- 客户 PII、邮箱、支付信息、原始事件日志或用户级标识符
- 可以直接修改生产系统的脚本

每个 skill 默认只接受三类安全输入：

1. 公开网页信息
2. 用户提供的脱敏导出
3. 手动粘贴、且已移除敏感字段的摘要

## Repository Structure

```text
skills/
  ads-health-monitor/
  github-outreach-ops/
  growth-data-analysis/
  stripe-ops-review/
  trend-signal-tracker/
  wix-blog-pipeline/
  daily-growth-brief/
```

每个 skill 文件夹包含：

- `SKILL.md`：agent-facing 操作说明
- `agents/openai.yaml`：展示名称、短描述和默认提示词

## Usage

把任意 `skills/` 目录下的文件夹复制到你的 Codex skills 目录，或者在对话里直接引用对应 skill 文件夹。

示例：

```text
Use growth-data-analysis to inspect this sanitized acquisition export and summarize the top three findings.
```

## Publication Note

这个仓库默认公开。如果你要把这些 skills 改造成私有生产工作流，请把生产 connector、凭证、账号 ID 和任何 live mutation 步骤放在私有仓库里。
