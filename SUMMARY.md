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
- [20:27 - MOTX/Moxt 软件研发范式研究增量记录：角色自治等级与研发对象协议](logs/2026-05-01/20-27.md)
- [21:28 - MOTX/Moxt 软件研发范式研究增量记录：Risk Control Plane 与 ActionIntent](logs/2026-05-01/21-28.md)
- [22:27 - MOTX/Moxt 软件研发范式研究增量记录：Agent Adapter、AgentSession 与 RiskBudget](logs/2026-05-01/22-27.md)
- [23:27 - MOTX/Moxt 软件研发范式研究增量记录：Lifecycle Control Plane](logs/2026-05-01/23-27.md)

#### 2026-05-02

- [00:28 - MOTX/Moxt 软件研发范式研究增量记录：Task Structuring Engine 与 Semantic Permission](logs/2026-05-02/00-28.md)

## 当前阶段性结论

Moxt 在软件研发领域的最佳切入点不是做“又一个代码编辑器”，而是做“AI 研发组织的工作空间”。核心价值是让多个 AI 同事在共享上下文、受控权限和可审计产物中协作，把研发流程从人类手工串行推进，升级为 AI 持续并行推进、人类重点审查决策。

进一步确认：Moxt 更适合作为研发组织的 agent operating layer，站在 Cursor、Claude Code、GitHub、Slack、文档系统之上，承担团队 AI 同事编排、共享记忆、规则治理、工具权限和研发对象图谱维护。

最新设计判断：Moxt/MOTX 在软件研发里的关键产品形态不是 AI coding IDE，而是 AI-native engineering workspace。它应承担研发上下文总线、AI 同事运行环境、研发对象状态机和治理控制面四个角色。

最新综合结论：Moxt 的核心正在从 Agent 管理演进为 Task + Agent + Constraint 三位一体系统。成功率 = Task 质量 × Agent 能力 × 约束强度；其中 Task 质量与约束强度都可由 Moxt 控制。

## 当前推荐 AI 同事组合

1. Product Analyst / 需求研究 AI
2. Tech Lead / 架构拆解 AI
3. Implementation Engineer / 编码实现 AI
4. Reviewer / 代码审查 AI
5. QA / Release Guardian AI
6. Knowledge Steward / 知识管家 AI
7. Coordinator / 研发协调 AI
8. Security & Compliance Sentinel / 安全合规 AI
9. Lifecycle Manager / 生命周期管理 AI
10. Task Architect / 任务架构师

补充：Agent Adapter 不是第 11 个 AI 同事，而是连接 Copilot、Codex、Claude Code、Cursor、内部 agent 的外部 agent 适配层。

## 当前核心设计判断

- AI 同事不是功能菜单，而是具备稳定身份、职责边界、工具权限、协作规则和评价指标的数字研发成员。
- AI 原生工作空间的核心对象不只是文档，而是需求、任务、分支、PR、测试、发布、事故、记忆、规则和指标组成的研发对象图谱。
- 人类应从执行者转为目标设定者、边界控制者和关键决策者。
- 所有高风险操作必须最小权限、可审计、可回滚、有人类审批。
- 评价 AI 研发系统不能只看编码 benchmark，而要看真实研发效率、质量、成本和风险。
- 多 AI 并行需要 Coordinator 负责任务锁、交接、冲突检测和升级机制。
- 软件研发场景需要单独的 Security & Compliance Sentinel，而不是把安全职责完全分散给 Reviewer。
- AI 同事设计应采用角色 × 自治等级：角色决定职责边界，自治等级决定工具权限，对象状态决定下一步行动，风险等级决定是否需要人类审批。
- Moxt 工作空间应采用统一研发对象协议，为 Goal、Requirement、Design、Task、PR、Test、Release、Incident、Memory、Rule、Skill 设置来源、置信度、风险等级、审批要求和关联对象。
- 所有高风险工具调用都应先结构化为 ActionIntent，再经过风险分级、dry-run、影响范围分析、回滚计划和审批。
- 外部 coding agent 应被视为可插拔 worker，并通过 Agent Adapter 接入 Moxt 的对象协议、权限系统和审计链路。
- 长生命周期 agent 必须纳入 Lifecycle Control Plane，支持 TTL、健康检查、kill fast、资源回收和幽灵任务清理。
- Moxt 应增加 Task Structuring Engine，将模糊需求转为 TaskGraph、SemanticScope、验收标准、依赖关系和风险标签。
- 文件级权限不足，需要 Semantic Permission Layer 识别 auth、billing、migration、permission 等语义风险。

## 后续研究重点

1. 设计 Task Graph 自动生成算法（从 PR / issue 学习）。
2. 设计 Semantic Permission taxonomy（语义权限分类体系）。
3. 设计 reward hacking 检测机制。
4. 建立“Task → Failure → 修正”的闭环系统。
5. 研究如何将 Task Architect 半自动化（human-in-the-loop）。
6. 设计 Agent Reputation System 与组织内 benchmark。
7. 继续细化 Agent Adapter、ActionIntent、RiskBudget、AgentLifecycle、PRRiskProfile 等对象规范。
