---
name: product-manager-workflow
description: End-to-end product manager workflow for turning ideas, problems, requests, or opportunities into validated PM deliverables. Use when the user asks to clarify a product idea, define a problem, write or review a PRD, create user stories and acceptance criteria, design metrics, plan a roadmap, structure A/B tests or validation, plan delivery, run product reviews, analyze competitors, or prepare launch retrospectives.
---

# Product Manager Workflow

Use this skill to run a complete product manager workflow from discovery interview to structured deliverables. Default to an interview-first process: ask one question at a time, do not invent missing facts, check information completeness, then produce only the deliverables that are sufficiently supported by confirmed information.

## Core Rules

- Follow the user's language. If the user writes in Chinese, respond in Chinese; if English, respond in English. Keep common product and technical terms in their usual form when helpful.
- Ask one question at a time during discovery.
- Show the current interview stage and progress when asking. In Chinese, use a format such as `当前阶段：1/9 背景与触发原因`.
- Do not repeat back every user answer by default. Only restate for confirmation when the answer is ambiguous, contradictory, or important enough to affect later work.
- When an answer is too broad, provide 2-4 concrete options to help the user choose, without deciding for them.
- Do not make assumptions or fill gaps with industry guesses. If information is missing, ask for it or mark the item as not ready.
- Require evidence sources for user needs or problem claims. If no evidence exists, mark the need as unverified.
- Before final deliverables, run an information completeness check and ask the user whether to continue discovery or generate the supported outputs.
- Preserve `待确认` and `未验证` markers in formal outputs. Do not hide missing or unsupported information.
- Do not browse the web unless the user explicitly asks. For external facts such as competitor state, pricing, regulations, platform policies, or API capabilities, mark facts as unverified when not checked.
- Use the minimum process needed for the request, but keep the workflow auditable: every output should trace to confirmed user input, cited evidence, or an explicit user decision.
- Include non-goals only when the request is complex, cross-functional, high-risk, likely to expand in scope, or the user asks for them.
- Do not suggest or launch subagents by default. Use the multi-role review checklist instead.
- Default to standard detail: complete enough for collaboration, but not exhaustive unless the user asks for a detailed version.

## Discovery Interview

Ask through these stages in order. Ask only one question per message, and stay in the current stage until the answer is clear enough to continue.

1. Background and trigger
2. Goal and business outcome
3. Users and use scenarios
4. Current problem and evidence
5. Success metrics
6. Scope boundaries and non-goals when needed
7. Constraints, dependencies, and risks
8. Priority and milestones
9. Launch validation and retrospective approach

Prefer concrete questions over generic prompts. Examples:

- "What triggered this request now?"
- "Which user segment is most affected?"
- "What evidence shows this problem exists?"
- "What outcome would make this work successful?"
- "What constraint is least flexible: time, scope, quality, compliance, or resources?"

## Completeness Check

Before creating formal deliverables, summarize:

- Confirmed information
- Missing information
- Unverified claims or evidence gaps
- Whether there is enough information for each requested deliverable
- Recommended next step: continue interviewing, narrow scope, or generate supported outputs

Ask for user confirmation before proceeding from the completeness check to final deliverables.

Use this output shape:

- Confirmed information
- Missing information, why it matters, and the suggested follow-up question
- Unverified information, current claim, and needed evidence
- Which deliverables can be generated, and why
- Recommended next step: continue interviewing, narrow scope, or generate supported outputs

## Deliverable Priority

When the user asks for full-process output, produce deliverables in this default order:

1. Requirement clarification summary
2. Full engineering-collaboration PRD
3. User stories and acceptance criteria
4. Metrics system and success criteria
5. Roadmap and milestones
6. A/B test or validation plan
7. Project delivery plan
8. Review checklist
9. Launch retrospective template

Generate only deliverables with enough confirmed information. If a deliverable is not ready, explain why in the completeness check instead of forcing a partial document. When generating multiple deliverables, start with an output table of contents, then write each deliverable in order.

Add competitor analysis when the user asks for competitor research, competitive review, market comparison, positioning, or benchmark analysis.

Load `references/templates.md` when writing these deliverables or when the user asks for a template.

## PRD Standard

Default to a full engineering-collaboration PRD. Cover the material needed by product, design, engineering, QA, data, and operations:

- Context and problem
- Goals and business outcomes
- Target users and scenarios
- Evidence and source quality
- Scope, functional requirements, and non-functional requirements
- User stories and acceptance criteria
- States, edge cases, permissions, errors, and boundary conditions
- Page and interaction notes, prototype links, and flow diagram locations
- Metrics, event tracking, and validation plan
- Dependencies, risks, rollout, and rollback
- Milestones and owners

## Product Principles

Use these principles during interviews, reviews, and output checks:

- Define the problem before proposing solutions.
- Identify specific users and scenarios.
- Require success metrics.
- State non-goals when complexity or scope risk requires it.
- Cover boundary conditions and exception paths.
- Include tracking and validation plans.
- Identify dependencies, risks, and launch strategy.

## Method Defaults

- Metrics: use North Star metric, input metrics, and guardrail metrics.
- Prioritization: choose the method by context, such as RICE, MoSCoW, value-cost matrix, Kano, or impact-effort. Explain why the method fits.
- Requirement priority labels: follow the user's team convention. If no convention is provided, use `P0 / P1 / P2`.
- Competitor analysis: default to structured analysis covering target users, core flows, feature matrix, pricing or business model, strengths, weaknesses, and opportunity points.
- Delivery plan: define deliverables, owners, milestones, dependencies, completion criteria, and risks.
- Launch retrospective: cover goal review, actual results versus expectation, metric performance, user feedback, issues or incidents, decision review, lessons learned, and follow-up actions.

## Review Checklist

Use this checklist for PM review or before handoff:

- Problem is clear and evidence-backed.
- Target user and scenario are specific.
- Outcome and success metrics are measurable.
- Scope is clear enough for design and engineering.
- Non-goals are present when needed.
- Requirements include edge cases, errors, states, and permissions.
- Acceptance criteria are testable.
- Metrics and event tracking support validation.
- Dependencies and risks have owners or mitigation.
- Rollout, rollback, and post-launch review are defined.

---

# 产品经理工作流模板

仅在完成访谈和信息完整度检查后使用这些模板。删除没有已确认信息支撑的部分，或标记为“待确认 / 未验证”。默认输出标准版：足够协作，但不写成过度冗长的文档。

## 输出目录

一次生成多个输出物时先输出目录：

```markdown
# 本次输出目录

1. 需求澄清摘要
2. PRD
3. 用户故事与验收标准
4. 指标体系与成功标准
5. Roadmap 与里程碑
6. A/B 测试或验证方案
7. 项目推进计划
8. 产品评审 Checklist
9. 上线复盘
```

## 信息完整度检查

```markdown
# 信息完整度检查

## 1. 已确认信息

| 信息项 | 已确认内容 | 来源 |
| --- | --- | --- |

## 2. 缺失信息

| 信息项 | 为什么重要 | 建议追问 |
| --- | --- | --- |

## 3. 未验证信息

| 信息项 | 当前说法 | 需要的证据 |
| --- | --- | --- |

## 4. 可生成的输出物

| 输出物 | 是否可生成 | 原因 |
| --- | --- | --- |

## 5. 建议下一步

- 继续追问 / 缩小范围 / 生成已支持的输出物
```

## 1. 需求澄清摘要

```markdown
# 需求澄清摘要

## 1. 背景

## 2. 触发原因

## 3. 目标用户

## 4. 使用场景

## 5. 问题陈述

## 6. 证据来源

## 7. 目标

## 8. 成功指标

## 9. 范围

## 10. 约束

## 11. 风险

## 12. 待确认问题
```

## 2. 完整研发协作型 PRD

```markdown
# PRD：<产品 / 功能名称>

## 1. 文档信息

- 版本：
- 作者：
- 更新时间：
- 相关链接：
- 状态：草稿 / 评审中 / 已确认 / 开发中 / 已上线

## 2. 背景与上下文

## 3. 问题陈述

## 4. 证据与来源质量

- 证据来源：
- 证据类型：
- 可信度：
- 是否仍需验证：

## 5. 目标与业务结果

- 产品目标：
- 用户目标：
- 业务目标：

## 6. 目标用户与场景

- 用户角色：
- 用户场景：
- 当前路径：
- 目标路径：

## 7. 页面 / 交互说明

### 7.1 页面清单

| 页面 / 模块 | 说明 | 入口 | 相关状态 |
| --- | --- | --- | --- |

### 7.2 关键交互

| 交互点 | 触发条件 | 系统反馈 | 备注 |
| --- | --- | --- | --- |

### 7.3 原型链接

- Figma / 蓝湖 / Pixso / 墨刀 / 其他：

### 7.4 流程图位置

- 用户流程图：
- 业务流程图：
- 状态流转图：
- 时序图 / 数据流图：

## 8. 范围

### 8.1 本次范围

### 8.2 非目标 / 暂不做

## 9. 功能需求

| ID | 功能点 | 用户价值 | 优先级 | 说明 |
| --- | --- | --- | --- | --- |

## 10. 详细规则 / 业务逻辑

## 11. 用户故事与验收标准

| 用户故事 | 验收标准 | 优先级 |
| --- | --- | --- |

## 12. 边界情况与异常路径

- 空状态：
- 错误状态：
- 权限不足：
- 网络 / 系统失败：
- 数据异常：
- 重复提交：
- 取消 / 回退 / 撤销：

## 13. 非功能需求

- 性能：
- 安全：
- 隐私：
- 可用性：
- 兼容性：
- 可访问性：
- 合规：

## 14. 埋点与数据需求

| 事件名 | 触发时机 | 属性 | 用途 |
| --- | --- | --- | --- |

## 15. 指标与验证方式

- 北极星指标：
- 输入指标：
- 护栏指标：
- 验证方式：

## 16. 依赖

- 设计依赖：
- 技术依赖：
- 数据依赖：
- 运营依赖：
- 法务 / 合规依赖：

## 17. 风险与应对

| 风险 | 影响 | 概率 | 应对方案 |
| --- | --- | --- | --- |

## 18. 发布策略

- 灰度范围：
- 上线步骤：
- 回滚方案：
- 通知对象：

## 19. 里程碑与 Owner

| 阶段 | 交付物 | Owner | 时间节点 | 完成标准 |
| --- | --- | --- | --- | --- |

## 20. 待确认问题
```

## 3. 用户故事与验收标准

```markdown
# 用户故事与验收标准

## 1. 用户角色

## 2. 用户故事列表

| ID | 用户角色 | 场景 | 用户故事 | 用户价值 | 优先级 |
| --- | --- | --- | --- | --- | --- |

## 3. 验收标准

| 用户故事 ID | Given 前置条件 | When 用户行为 | Then 预期结果 | 补充说明 |
| --- | --- | --- | --- | --- |

## 4. 边界与异常验收

| 场景 | 前置条件 | 操作 | 预期结果 |
| --- | --- | --- | --- |

## 5. 不通过示例
```

## 4. 指标体系与成功标准

```markdown
# 指标体系与成功标准

## 1. 指标目标

## 2. 北极星指标

| 指标 | 定义 | 计算方式 | 数据来源 | 目标值 | 观察周期 |
| --- | --- | --- | --- | --- | --- |

## 3. 输入指标

| 指标 | 影响路径 | 定义 | 数据来源 | 目标值 | 负责人 |
| --- | --- | --- | --- | --- | --- |

## 4. 护栏指标

| 指标 | 防止的问题 | 阈值 | 触发后动作 |
| --- | --- | --- | --- |

## 5. 埋点需求

| 事件名 | 触发时机 | 属性 | 关联指标 | 说明 |
| --- | --- | --- | --- | --- |

## 6. 分析维度

## 7. 成功标准

## 8. 复盘节奏
```

## 5. Roadmap 与里程碑

```markdown
# Roadmap 与里程碑

## 1. Roadmap 目标

## 2. 阶段规划

| 阶段 | 时间范围 | 阶段目标 | 核心交付物 | 不做什么 |
| --- | --- | --- | --- | --- |

## 3. 里程碑

| 里程碑 | 时间节点 | Owner | 完成标准 | 依赖 |
| --- | --- | --- | --- | --- |

## 4. 优先级依据

## 5. 关键依赖

| 依赖项 | 影响范围 | 负责人 | 截止时间 | 风险 |
| --- | --- | --- | --- | --- |

## 6. 风险与调整机制
```

## 6. A/B 测试或验证方案

```markdown
# A/B 测试或验证方案

## 1. 验证目标

## 2. 核心假设

## 3. 实验对象

- 目标用户：
- 纳入条件：
- 排除条件：

## 4. 实验设计

| 组别 | 方案 | 预期影响 | 说明 |
| --- | --- | --- | --- |
| 对照组 |  |  |  |
| 实验组 |  |  |  |

## 5. 指标

- 主指标：
- 输入指标：
- 护栏指标：

## 6. 样本与周期

- 预计样本量：
- 实验周期：
- 是否需要分层：
- 是否存在季节性或活动影响：

## 7. 决策规则

## 8. 风险与干扰因素

## 9. 复盘计划
```

## 7. 项目推进计划

```markdown
# 项目推进计划

## 1. 项目目标

## 2. 角色与分工

| 角色 | Owner | 职责 | 备注 |
| --- | --- | --- | --- |
| PM |  |  |  |
| 设计 |  |  |  |
| 研发 |  |  |  |
| 测试 |  |  |  |
| 数据 |  |  |  |
| 运营 |  |  |  |

## 3. 阶段计划

| 阶段 | 时间节点 | 交付物 | Owner | 完成标准 |
| --- | --- | --- | --- | --- |
| 需求澄清 |  |  |  |  |
| 方案设计 |  |  |  |  |
| 技术评审 |  |  |  |  |
| 开发联调 |  |  |  |  |
| 测试验收 |  |  |  |  |
| 灰度上线 |  |  |  |  |
| 正式发布 |  |  |  |  |
| 上线复盘 |  |  |  |  |

## 4. 依赖管理

| 依赖项 | 依赖方 | 影响 | 截止时间 | 状态 |
| --- | --- | --- | --- | --- |

## 5. 风险管理

| 风险 | 影响 | 概率 | 应对方案 | Owner |
| --- | --- | --- | --- | --- |

## 6. 沟通机制

- 固定会议：
- 评审节点：
- 状态同步方式：
- 升级机制：

## 7. 决策记录

| 决策 | 背景 | 决策人 | 时间 | 影响 |
| --- | --- | --- | --- | --- |
```

## 8. 产品评审 Checklist

```markdown
# 产品评审 Checklist

## 1. PM 自查

- [ ] 是否先定义问题，而不是直接给方案
- [ ] 是否明确目标用户和使用场景
- [ ] 是否有证据来源
- [ ] 是否定义成功指标
- [ ] 是否明确范围和必要的非目标
- [ ] 是否识别依赖和风险

## 2. 设计评审

- [ ] 是否覆盖核心用户路径
- [ ] 是否有页面 / 交互说明或原型链接
- [ ] 是否覆盖空状态、错误状态、加载状态
- [ ] 是否考虑可用性和可访问性
- [ ] 是否与现有设计规范一致

## 3. 研发评审

- [ ] 需求是否可拆解、可实现
- [ ] 业务规则是否明确
- [ ] 状态流转是否清楚
- [ ] 权限、数据、接口依赖是否明确
- [ ] 是否有性能、安全、兼容性要求

## 4. QA 评审

- [ ] 验收标准是否可测试
- [ ] 是否覆盖边界情况和异常路径
- [ ] 是否明确不通过示例
- [ ] 是否有回归影响范围
- [ ] 是否有上线前验收标准

## 5. 数据评审

- [ ] 指标定义是否清楚
- [ ] 埋点事件和属性是否完整
- [ ] 是否能支撑主指标、输入指标、护栏指标
- [ ] 是否有实验或上线后复盘口径

## 6. 运营 / GTM 评审

- [ ] 是否需要用户通知、公告或培训
- [ ] 是否需要客服话术或帮助文档
- [ ] 是否有灰度和发布节奏
- [ ] 是否有异常处理预案
```

## 9. 上线复盘

```markdown
# 上线复盘

## 1. 目标回顾

- 原定目标：
- 成功标准：
- 上线范围：
- 实际上线时间：

## 2. 实际结果 vs 预期

| 项目 | 预期 | 实际 | 差异 | 原因 |
| --- | --- | --- | --- | --- |

## 3. 指标表现

| 指标 | 上线前基线 | 目标值 | 实际值 | 结论 |
| --- | --- | --- | --- | --- |

## 4. 用户反馈

- 正向反馈：
- 负向反馈：
- 高频问题：
- 代表性原话 / 案例：

## 5. 问题与事故

| 问题 | 影响范围 | 原因 | 处理过程 | 后续措施 |
| --- | --- | --- | --- | --- |

## 6. 决策复盘

## 7. 经验沉淀

- 做得好的地方：
- 可以改进的地方：
- 下次可复用的方法：

## 8. 后续行动项

| 行动项 | Owner | 截止时间 | 成功标准 |
| --- | --- | --- | --- |
```

## 竞品分析

```markdown
# 竞品分析

## 1. 分析目标

## 2. 竞品范围

| 竞品 | 类型 | 选择原因 | 信息来源 |
| --- | --- | --- | --- |

## 3. 目标用户对比

| 竞品 | 目标用户 | 核心场景 |
| --- | --- | --- |

## 4. 核心流程对比

| 竞品 | 关键流程 | 优点 | 缺点 | 可借鉴点 |
| --- | --- | --- | --- | --- |

## 5. 功能矩阵

| 功能点 | 我们 | 竞品 A | 竞品 B | 竞品 C | 备注 |
| --- | --- | --- | --- | --- | --- |

## 6. 定价 / 商业模式

| 竞品 | 定价方式 | 商业模式 | 备注 |
| --- | --- | --- | --- |

## 7. 优劣势总结

| 竞品 | 优势 | 劣势 |
| --- | --- | --- |

## 8. 机会点

## 9. 未验证信息
```

