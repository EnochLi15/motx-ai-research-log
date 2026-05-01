# MOTX / Moxt AI Research Log Summary

## 文档导航

### 全量设计文档

- [全量设计方案](docs/full-design.md)
- [AI 同事角色设计](docs/ai-teammates.md)
- [AI 原生工作空间架构](docs/workspace-architecture.md)
- [软件研发 AI 原生作业范式](docs/workflow.md)
- [效率与评价指标体系](docs/metrics.md)
- [权限、安全与治理边界](docs/risks.md)

### 增量研究记录

#### 2026-05-01

- [18:27 - MOTX/Moxt 软件研发范式研究增量记录](logs/2026-05-01/18-27.md)
- [19:00 - MOTX/Moxt 软件研发范式研究增量记录：6+2 AI 同事模型](logs/2026-05-01/19-00.md)

## 当前阶段性结论

Moxt 在软件研发领域的最佳切入点不是做“又一个代码编辑器”，而是做“AI 研发组织的工作空间”。核心价值是让多个 AI 同事在共享上下文、受控权限和可审计产物中协作，把研发流程从人类手工串行推进，升级为 AI 持续并行推进、人类重点审查决策。

本轮进一步确认：Moxt 更适合作为研发组织的 agent operating layer，站在 Cursor、Claude Code、GitHub、Slack、文档系统之上，承担团队 AI 同事编排、共享记忆、规则治理、工具权限和研发对象图谱维护。

## 当前推荐 AI 同事组合

1. Product Analyst / 需求研究 AI
2. Tech Lead / 架构拆解 AI
3. Implementation Engineer / 编码实现 AI
4. Reviewer / 代码审查 AI
5. QA / Release Guardian AI
6. Knowledge Steward / 知识管家 AI
7. Coordinator / 研发协调 AI
8. Security & Compliance Sentinel / 安全合规 AI

## 当前核心设计判断

- AI 同事不是功能菜单，而是具备稳定身份、职责边界、工具权限、协作规则和评价指标的数字研发成员。
- AI 原生工作空间的核心对象不只是文档，而是需求、任务、分支、PR、测试、发布、事故、记忆、规则和指标组成的研发对象图谱。
- 人类应从执行者转为目标设定者、边界控制者和关键决策者。
- 所有高风险操作必须最小权限、可审计、可回滚、有人类审批。
- 评价 AI 研发系统不能只看编码 benchmark，而要看真实研发效率、质量、成本和风险。
- 多 AI 并行需要 Coordinator 负责任务锁、交接、冲突检测和升级机制。
- 软件研发场景需要单独的 Security & Compliance Sentinel，而不是把安全职责完全分散给 Reviewer。

## 后续研究重点

1. 为 8 个 AI 同事分别设计 System Prompt、Skills、Rules 和权限模板。
2. 设计 Moxt × GitHub 的 issue -> branch -> PR -> review -> release 具体对象模型。
3. 建立 AI 生成 PR 的评分表，包括正确性、可维护性、安全性、测试覆盖、需求一致性。
4. 研究 Coordinator 的任务锁、冲突检测、状态机和升级机制。
5. 持续跟踪 Moxt、AI coding agent、SWE-bench Live/Pro、团队级 agent orchestrator 的新进展。
