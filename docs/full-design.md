# MOTX / Moxt 软件研发 AI 原生工作空间全量设计

## 1. 设计目标

构建一个面向软件研发团队的 AI 原生工作空间，让多个 AI 同事在共享上下文、受控权限、可审计产物和可度量指标中协作，覆盖从需求、方案、实现、审查、测试、发布到知识沉淀的完整研发链路。

目标不是简单让 AI 写代码，而是改变研发组织的作业方式：

```text
人类设目标、控边界、做关键判断
AI 负责搜索、分析、拆解、执行、检查、总结、沉淀
```

## 2. 产品定位

Moxt 更适合作为“AI 研发组织的工作空间”，而不是单点编码工具。

它应承担三层职责：

1. **组织记忆层**：沉淀项目背景、架构约束、历史决策、团队规则。
2. **流程编排层**：让不同 AI 同事围绕研发对象协作。
3. **证据沉淀层**：把 AI 产出落到文件、Issue、PR、测试报告、发布记录和复盘中。

## 3. 核心原则

- AI 同事必须有稳定身份、职责边界和工具权限。
- 所有关键产出必须文件化、可追溯、可审计。
- 高风险操作必须人类审批。
- 每轮研究、每次任务、每个 PR 都应沉淀为组织资产。
- AI 的错误要进入反馈闭环，转化为规则、Skills 或评估指标。

## 4. 推荐 AI 同事组合

第一阶段建议配置 6 类 AI 同事：

1. Product Analyst / 需求研究 AI
2. Tech Lead / 架构拆解 AI
3. Implementation Engineer / 编码实现 AI
4. Reviewer / 代码审查 AI
5. QA / Release Guardian AI
6. Knowledge Steward / 知识管家 AI

这些角色覆盖软件研发闭环：

```text
需求 → 方案 → 实现 → 审查 → 测试发布 → 知识沉淀
```

## 5. 工作空间核心对象

AI 原生工作空间不应只管理文档，而应管理研发对象：

- Project
- Requirement
- Acceptance Criteria
- Task
- Architecture Decision Record
- Branch
- Pull Request
- Test Plan
- Release
- Incident
- Runbook
- Memory
- Rule
- Skill
- Metric

对象之间需要形成图谱关系。例如：

```text
Requirement
  ├── Acceptance Criteria
  ├── Technical Design
  ├── Task
  ├── Branch
  ├── Pull Request
  ├── Test Plan
  ├── Release
  └── Retrospective
```

## 6. 新研发作业范式

传统研发流程：

```text
人写需求 → 人开会 → 人拆任务 → 人写代码 → 人 Review → 人测试 → 人发布 → 人复盘
```

AI 原生研发流程：

```text
人提出目标
→ 需求研究 AI 补齐背景和验收标准
→ 架构拆解 AI 生成方案和任务图
→ 编码实现 AI 在隔离分支完成子任务
→ Reviewer AI 做第一轮审查
→ QA AI 生成测试和发布证据
→ 人类 owner 做关键判断和批准
→ Knowledge Steward AI 沉淀文档、规则和复盘
```

## 7. 权限边界

权限必须采用最小权限原则：

| 级别 | 权限 | 默认策略 |
|---|---|---|
| L0 | 只读文档、代码、Issue | 默认开放 |
| L1 | 写分析、草稿、评论 | 默认开放 |
| L2 | 创建分支、提交代码 | 任务授权 |
| L3 | 运行测试、CI、诊断命令 | 白名单 |
| L4 | 改配置、发布、迁移 | 人类审批 |
| L5 | 删除数据、删除备份、强推主干 | 默认禁止 |

## 8. 评价体系

不能只看 AI 是否会写代码，应看完整研发效率和质量：

- 需求澄清轮次
- 任务拆分准确率
- PR 首次 CI 通过率
- PR 合并率
- Review 修改轮次
- 人类修改比例
- 缺陷逃逸率
- 发布阻断准确率
- 文档沉淀率
- 新人 onboarding 时间
- 每个已交付任务的 AI 成本

## 9. 阶段性结论

Moxt 在软件研发中的核心机会，是把 AI 从“临时聊天助手”升级为“长期参与研发流程的组织成员”。真正的效率提升来自：

1. 上下文不再丢失。
2. 低风险研发任务可以并行推进。
3. Review、测试、发布证据可以自动化准备。
4. 组织经验可以沉淀为 Memory、Rules、Skills。
5. 人类从执行者转向目标设定者、风险控制者和关键决策者。
