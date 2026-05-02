# MOTX / Moxt AI Research Log Summary

## 文档导航

### 全量设计文档

- [全量设计方案 V2](docs/full-design.md)
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
- [01:28 - MOTX/Moxt 软件研发范式研究增量记录：Agent HQ 化与任务交接层](logs/2026-05-02/01-28.md)
- [02:27 - MOTX/Moxt 软件研发范式研究增量记录：Verifiable Delivery Protocol](logs/2026-05-02/02-27.md)
- [03:27 - MOTX/Moxt 软件研发范式研究增量记录：Adaptive Task-Verification Loop](logs/2026-05-02/03-27.md)
- [04:27 - MOTX/Moxt 软件研发范式研究增量记录：Strategy Layer 与全局优化](logs/2026-05-02/04-27.md)
- [05:27 - MOTX/Moxt 软件研发范式研究增量记录：Economic Layer 与资源优化](logs/2026-05-02/05-27.md)
- [06:27 - MOTX/Moxt 软件研发范式研究增量记录：Incentive Layer 与行为对齐](logs/2026-05-02/06-27.md)
- [07:28 - MOTX/Moxt 软件研发范式研究增量记录：Interpretability & Governance Layer](logs/2026-05-02/07-28.md)
- [08:28 - MOTX/Moxt 软件研发范式研究增量记录：AI Engineering Control Plane](logs/2026-05-02/08-28.md)
- [09:28 - MOTX/Moxt 软件研发范式研究增量记录：TaskGraph Runtime 与可控搜索验证系统](logs/2026-05-02/09-28.md)
- [10:27 - MOTX/Moxt 软件研发范式研究增量记录：Delegation Control Plane 与可验证委派层](logs/2026-05-02/10-27.md)

## 当前阶段性结论

Moxt 在软件研发领域的最佳切入点不是做“又一个代码编辑器”，而是做“AI 研发组织的工作空间”。核心价值是让多个 AI 同事在共享上下文、受控权限和可审计产物中协作，把研发流程从人类手工串行推进，升级为 AI 持续并行推进、人类重点审查决策。

进一步确认：Moxt 更适合作为研发组织的 agent operating layer，站在 Cursor、Claude Code、GitHub、Slack、文档系统之上，承担团队 AI 同事编排、共享记忆、规则治理、工具权限和研发对象图谱维护。

最新设计判断：Moxt/MOTX 在软件研发里的关键产品形态不是 AI coding IDE，而是 AI-native engineering workspace。它应承担研发上下文总线、AI 同事运行环境、研发对象状态机和治理控制面四个角色。

最新综合结论：Moxt 的核心正在从 Agent 管理演进为 Task + Agent + Constraint 三位一体系统，并进一步演进为可执行、可验证、可收敛、可优化、可对齐、可解释的 AI 工程组织操作系统。

最新推进：Moxt 的核心不只是管理 agent，而是把软件研发转化为一个可控的搜索与验证系统。TaskGraph 不应只是任务列表，而应成为 DAG + Runtime State + Budget + Risk + Agent Binding 的调度运行时。

最新收敛：Moxt 应成为 AI Engineering Delegation & Verification Workspace，通过 DelegationSpec 把任务委派给外部 / 内部 coding agent，并用 DeliveryContract、RiskBudget、Agent Reputation 和人类审批完成可控收敛。

## 当前推荐 AI 同事组合

### MVP 核心 7 个 AI 同事

1. Product Analyst / 需求研究 AI
2. Tech Lead / 架构拆解 AI
3. Task Architect / 任务架构师
4. Implementation Engineer / 编码实现 AI
5. Reviewer / 代码审查 AI
6. QA / Release Guardian AI
7. Knowledge Steward / 知识管家 AI

### 企业增强型 AI 同事

8. Coordinator / 研发协调 AI
9. Security & Compliance Sentinel / 安全合规 AI
10. Lifecycle Manager / 生命周期管理 AI
11. Delivery Auditor / 交付审计 AI
12. Task Critic / 任务批判 AI
13. Strategy Planner / 策略规划 AI
14. Architecture Governor / 架构治理 AI
15. Resource Allocator / 资源分配 AI
16. Incentive Designer / 激励设计 AI
17. Decision Explainer / 决策解释 AI
18. Governance Auditor / 治理审计 AI

补充：Agent Adapter 不是独立 AI 同事，而是连接 Copilot、Codex、Claude Code、Cursor、内部 agent 的外部 agent 适配层。

## 当前核心设计判断

- AI 同事不是功能菜单，而是具备稳定身份、职责边界、工具权限、协作规则和评价指标的数字研发成员。
- AI 原生工作空间的核心对象不只是文档，而是需求、任务、分支、PR、测试、发布、事故、记忆、规则、指标和决策图谱组成的研发对象系统。
- 人类应从执行者转为目标设定者、边界控制者、关键决策者、监督者和干预者。
- 所有高风险操作必须最小权限、可审计、可回滚、有人类审批。
- 评价 AI 研发系统不能只看编码 benchmark，而要看真实研发效率、质量、成本、风险、可解释性和长期稳定性。
- 多 AI 并行需要 Coordinator 负责任务锁、交接、冲突检测和升级机制。
- 软件研发场景需要单独的 Security & Compliance Sentinel，而不是把安全职责完全分散给 Reviewer。
- AI 同事设计应采用角色 × 自治等级：角色决定职责边界，自治等级决定工具权限，对象状态决定下一步行动，风险等级决定是否需要人类审批。
- Moxt 工作空间应采用统一研发对象协议，为 Goal、Requirement、Design、Task、PR、Test、Release、Incident、Memory、Rule、Skill、AgentSession、ActionIntent、DeliveryContract、DecisionGraph、DelegationSpec 设置来源、置信度、风险等级、审批要求和关联对象。
- 所有高风险工具调用都应先结构化为 ActionIntent，再经过风险分级、dry-run、影响范围分析、回滚计划和审批。
- 外部 coding agent 应被视为可插拔 worker，并通过 Agent Adapter 接入 Moxt 的对象协议、权限系统和审计链路。
- 长生命周期 agent 必须纳入 Lifecycle Control Plane，支持 TTL、健康检查、kill fast、资源回收和幽灵任务清理。
- Moxt 应增加 Task Structuring Engine，将模糊需求转为 TaskGraph、SemanticScope、验收标准、依赖关系和风险标签。
- 文件级权限不足，需要 Semantic Permission Layer 识别 auth、billing、migration、permission 等语义风险。
- Delivery Contract 与 Delivery Auditor 应成为判断“PR 是否真的完成目标”的核心机制。
- Task Critic 与 Task Evolution Log 应帮助系统区分 task failure、execution failure、verification failure，并推动任务持续收敛。
- Strategy Layer、Economic Layer、Incentive Layer、Interpretability & Governance Layer 分别解决全局最优、资源最优、行为对齐和可信治理问题。
- TaskGraph Runtime 是下一阶段核心突破点：它需要支持动态插入节点、执行中重新拆任务、候选 PR 自动评分、失败后任务演化，以及映射到 GitHub issue / PR / check。
- DelegationSpec 是 Moxt 进入“可验证委派层”的关键对象：它定义任务类型、委派模式、候选 agent、上下文包、权限预算、风险预算、验证契约、超时策略和期望产物。
- Moxt 不应默认选择“第一个完成的 agent”，而应根据 DeliveryContract、风险、成本、可维护性、测试信心和 Agent Reputation 综合选择候选结果。

## 后续研究重点

1. 设计 Agent Reputation System：任务类型画像、成功率、失败模式、上下文敏感性、成本和风险倾向。
2. 设计 TaskGraph Runtime：DAG、Runtime State、Budget、Risk、Agent Binding、动态插入节点。
3. 设计 Candidate PR 评分模型：quality、risk、cost、diff size、test confidence、delivery contract confidence。
4. 设计 GitHub 映射方案：TaskGraph 如何落到 issue、branch、draft PR、check run、review、release。
5. 设计 Governance Policy DSL，定义权限、审计、解释、审批和软/硬治理规则。
6. 设计 AI 同事角色合并与最小化方案，避免角色过度膨胀。
7. 设计 `.moxt/` 仓库规范：handoff、taskgraph、delivery-contract、risk-budget、decision-log、memory、delegation-spec。
8. 继续细化 Agent Adapter、ActionIntent、RiskBudget、AgentLifecycle、PRRiskProfile、DeliveryContract、TaskEvolutionLog、StrategySnapshot、IncentiveProfile、DecisionGraph、DelegationSpec 等对象规范。
