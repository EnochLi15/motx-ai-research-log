# AI 原生工作空间架构

## 1. 定位

AI 原生工作空间不是传统文档库，也不是单个聊天窗口，而是人类与 AI 同事共同工作的研发控制塔。

它需要同时承载：

- 组织记忆
- 项目上下文
- 研发对象
- 工具权限
- 任务编排
- 审计记录
- 评价指标

## 2. 分层架构

```text
┌──────────────────────────────┐
│ 人类 Owner / Reviewer / PM    │
├──────────────────────────────┤
│ AI 同事层                     │
│ Product / Tech Lead / Dev / QA │
├──────────────────────────────┤
│ Moxt Workspace                │
│ Files / Memory / Skills / Rules│
├──────────────────────────────┤
│ 工具集成层                    │
│ GitHub / Slack / CI / Docs     │
├──────────────────────────────┤
│ 研发资产层                    │
│ Code / Issues / PR / Tests     │
└──────────────────────────────┘
```

## 3. 核心对象模型

### Project

字段建议：

- id
- name
- repo
- owner
- business_goal
- tech_stack
- architecture_constraints
- risk_level
- active_ai_teammates

### Requirement

字段建议：

- id
- title
- source
- user_value
- acceptance_criteria
- open_questions
- priority
- status
- linked_tasks
- linked_prs

### Task

字段建议：

- id
- requirement_id
- type
- owner_type: human | ai
- assignee
- context_package
- allowed_files
- forbidden_files
- test_requirements
- escalation_rules
- status

### Pull Request

字段建议：

- id
- branch
- requirement_id
- task_id
- author_type
- change_summary
- risk_level
- test_evidence
- review_status
- human_approval_required

### Memory

字段建议：

- id
- scope: personal | team | project | audit
- content
- source
- confidence
- expires_at
- owner

### Rule

字段建议：

- id
- name
- condition
- action
- severity
- owner
- version
- enabled

### Skill

字段建议：

- id
- name
- role
- prompt
- tool_requirements
- output_schema
- evaluation_method

## 4. 记忆分层

| 记忆类型 | 内容 | 示例 |
|---|---|---|
| Personal Memory | 个人偏好 | 某工程师喜欢简洁 PR 摘要 |
| Team Memory | 团队规范 | 所有 API 变更必须更新 OpenAPI |
| Project Memory | 项目上下文 | 当前系统采用事件驱动架构 |
| Audit Memory | 决策记录 | 某次架构取舍和批准人 |

## 5. 工具集成

| 工具 | 在工作空间中的角色 |
|---|---|
| GitHub | 代码、Issue、PR、CI、审计执行层 |
| Slack / 飞书 | 沟通输入、通知、异步协作 |
| 文档系统 | PRD、方案、ADR、runbook |
| CI/CD | 验证、构建、发布证据 |
| 监控系统 | 运行反馈、告警、事故输入 |
| 测试平台 | 测试用例、回归、覆盖率 |

## 6. 文件化要求

所有关键产出必须落盘：

- 需求分析：Markdown
- 技术方案：Markdown / ADR
- 任务拆分：Issue / Task
- 代码实现：Branch / PR
- 审查结果：PR Comment / Review Report
- 测试结果：Test Report
- 发布检查：Release Checklist
- 事故复盘：Postmortem
- 长期规则：Rules / Skills

## 7. 审计要求

每个 AI 动作都应记录：

- 谁触发
- 哪个 AI 执行
- 读取了什么上下文
- 使用了什么工具
- 修改了什么对象
- 产出了什么文件
- 是否经过人类确认
- 是否影响生产

## 8. 总结

AI 原生工作空间的关键不是“让 AI 能聊天”，而是让 AI 产出的每一步都进入组织可追踪、可验证、可复用的研发资产链路。
