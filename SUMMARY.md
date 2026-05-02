# MOTX / Moxt AI Research Log Summary

## 文档导航

### 全量设计文档

- [全量设计方案 V2（含 Mermaid 架构图）](docs/full-design.md)
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
- [11:28 - Moxt 公开定位更新：从 AI Team OS 到软件研发 Delegation & Verification Workspace](logs/2026-05-02/11-28.md)
- [12:28 - Moxt 进化为 AI Workflow Runtime 与研发控制面](logs/2026-05-02/12-28.md)
- [13:27 - Moxt 进入多 Agent 调度与解空间搜索阶段](logs/2026-05-02/13-27.md)
- [14:28 - Moxt 进入可学习编排系统阶段（Learning Orchestrator）](logs/2026-05-02/14-28.md)
- [15:27 - 证据优先的 AI Engineering Control Workspace](logs/2026-05-02/15-27.md)
- [16:27 - Evidence-Gated Agentic Development 与 AI 变更控制系统](logs/2026-05-02/16-27.md)
- [17:27 - Agent Identity Boundary 与非人类身份治理](logs/2026-05-02/17-27.md)
- [18:27 - Agent Sandbox 与执行隔离层](logs/2026-05-02/18-27.md)
- [19:27 - Verification Pipeline DSL 与验证编排层](logs/2026-05-02/19-27.md)
- [20:27 - Decision Engine 与可解释发布决策系统](logs/2026-05-02/20-27.md)
- [21:27 - Control Contract System 与行为约束协议层](logs/2026-05-02/21-27.md)
- [22:27 - Stateful Learning Loop 与系统级自进化机制](logs/2026-05-02/22-27.md)

## 当前阶段性结论

Moxt 在软件研发领域的最佳切入点不是做“又一个代码编辑器”，而是做“AI 研发组织的工作空间”。核心价值是让多个 AI 同事在共享上下文、受控权限和可审计产物中协作，把研发流程从人类手工串行推进，升级为 AI 持续并行推进、人类重点审查决策。

进一步确认：Moxt 更适合作为研发组织的 agent operating layer，站在 Cursor、Claude Code、GitHub、Slack、文档系统之上，承担团队 AI 同事编排、共享记忆、规则治理、工具权限和研发对象图谱维护。

最新综合结论：Moxt 的核心正在从 Agent 管理演进为 Task + Agent + Constraint 三位一体系统，并进一步演进为可执行、可验证、可收敛、可优化、可对齐、可解释、可隔离、可学习的 AI 工程组织操作系统。

最新推进：Moxt 的核心不只是管理 agent，而是把软件研发转化为一个可控的搜索、执行、验证、决策与学习系统。TaskGraph 不应只是任务列表，而应成为 DAG + Runtime State + Budget + Risk + Agent Binding 的调度运行时。

最新收敛：Moxt 应成为 AI Engineering Delegation & Verification Workspace，通过 DelegationSpec 把任务委派给外部 / 内部 coding agent，并用 DeliveryContract、RiskBudget、Agent Reputation 和人类审批完成可控收敛。

最新升级：Moxt 更接近 AI Workflow Runtime + Delegation OS + Memory System + Governance Layer。软件研发的核心不只是让 AI 写代码，而是约束、调度、验证和治理 AI 行为，把 AI 的不确定性限制在可验证边界内。

最新范式：Moxt 应从“任务中心”进一步升级为“证据中心”。核心链路是 Intent → Spec → Delivery Contract → Change Set → Evidence Pack → Release Decision → Outcome Memory；完成状态不由执行 AI 自己声明，而由证据协议判定。

最新定位：Moxt 应成为 AI 生成软件变更的“控制塔”和“证据门禁”。产品核心应围绕 Evidence-Gated Agentic Development：IntentSpec、ChangePlan、Delegation Control、Agent Sandbox、EvidencePack、RiskProfile、ReleaseDecision、OutcomeMemory。

最新闭环：Moxt 的控制面已经形成 Identity → Permission → Sandbox → ExecutionTrace → Evidence → Decision 的基础闭环，并进一步演化为 Contract → Identity → Permission → Sandbox → Execution → Verification → Evidence → Decision → Outcome → Learning → Evolution。

最新本质：Moxt 不只是 AI 变更控制系统，而是 AI 工程身份 + 权限 + 隔离执行 + 验证编排 + 可解释决策 + 系统级学习的统一控制面。最终定位可表述为：Self-Evolving AI Software Engineering Control Plane。

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

### 证据优先责任链压缩版

1. Spec Steward / 需求与约束管理员
2. Change Producer / 变更生产者
3. Evidence Reviewer / 证据审查员
4. Release Governor / 发布治理员

### 变更控制责任链 MVP

1. Intent Clarifier / 意图澄清 AI
2. Change Planner / 变更规划 AI
3. Implementation Worker / 实现 AI
4. Evidence Builder / 证据构建 AI
5. Risk & Security Sentinel / 风险安全 AI
6. Release Governor / 发布治理 AI

### 系统级控制角色

1. Agent Identity Steward / AI 身份管理员
2. Sandbox Orchestrator / 执行隔离调度器
3. Verification Architect / 验证架构师
4. Decision Engine / 发布决策引擎
5. Control Contract Designer / 行为约束设计 AI
6. Outcome Analyst / 结果分析 AI
7. Evolution Engine / 策略进化引擎

补充：Agent Adapter 不是独立 AI 同事，而是连接 Copilot、Codex、Claude Code、Cursor、内部 agent 的外部 agent 适配层。

## 当前核心设计判断

- AI 同事不是功能菜单，而是具备稳定身份、职责边界、工具权限、协作规则和评价指标的数字研发成员。
- AI 原生工作空间的核心对象不只是文档，而是需求、任务、分支、PR、测试、发布、事故、记忆、规则、指标和决策图谱组成的研发对象系统。
- 人类应从执行者转为目标设定者、边界控制者、关键决策者、监督者和干预者。
- 所有高风险操作必须最小权限、可审计、可回滚、有人类审批。
- 评价 AI 研发系统不能只看编码 benchmark，而要看真实研发效率、质量、成本、风险、可解释性和长期稳定性。
- 多 AI 并行需要 Coordinator / Orchestrator 负责任务锁、交接、冲突检测、候选方案生成、早停和升级机制。
- 软件研发场景需要单独的 Security & Compliance Sentinel，而不是把安全职责完全分散给 Reviewer。
- AI 同事设计应采用角色 × 自治等级：角色决定职责边界，自治等级决定工具权限，对象状态决定下一步行动，风险等级决定是否需要人类审批。
- Moxt 工作空间应采用统一研发对象协议，为 Goal、Requirement、Design、Task、PR、Test、Release、Incident、Memory、Rule、Skill、AgentSession、ActionIntent、DeliveryContract、DecisionGraph、DelegationSpec、ControlContract、SolutionSet、StrategyMemory、ExperienceRecord、EvidencePack、IntentSpec、ChangePlan、RiskProfile、ReleaseDecision、AgentPerformanceRecord、AgentIdentity、PermissionGrant、DelegationChain、AgentSandbox、ToolProxy、ExecutionTrace、VerificationPipeline、VerificationResult、DecisionPolicy、DecisionTrace、BehaviorTrace、OutcomeRecord、LearningSignal、EvolutionAction 设置来源、置信度、风险等级、审批要求和关联对象。
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
- ControlContract 是约束 AI 行为的关键对象：它定义 allowed_actions、forbidden_actions、required_verifications、risk_budget、escalation_rules，并与 VerificationPipeline 对齐。
- Moxt 不应默认选择“第一个完成的 agent”，而应根据 DeliveryContract、风险、成本、可维护性、测试信心和 Agent Reputation 综合选择候选结果。
- SolutionSet / SolutionGraph 把研发从单路径执行转为多候选解搜索；SelectionPolicy 决定如何在质量、成本、延迟和风险之间权衡。
- Learning Controller 与 StrategyMemory 使 Moxt 从编排系统进化为可学习系统：Execution → Result → Evaluation → Strategy Update → Next Execution。
- Evidence Pack 和 Release Decision 是证据优先范式的关键：把 AI 审查、测试、静态分析、风险说明和发布门禁标准化。
- Evidence-Gated Agentic Development 是当前最可落地的软件研发作业范式：AI 不是提交完成结果，而是提交候选变更；系统通过 EvidencePack、RiskProfile 和 ReleaseDecision 决定是否接受。
- Moxt 应围绕 Change Acceptance 而不是 Code Generation 设计产品：关键不是哪个 agent 最会写代码，而是在什么任务、风险、上下文、验证证据下，哪个 agent 的哪个变更可以被接受。
- AgentIdentity / PermissionGrant / DelegationChain 解决“哪个 AI 身份在什么授权边界内完成了什么变更”的问题。
- AgentSandbox / ToolProxy / ExecutionTrace 解决“agent 在哪里执行、如何调用工具、做了什么”的问题。
- VerificationPipeline / VerificationResult / EvidenceSchema 解决“证据如何被生产出来”的问题。
- DecisionEngine / DecisionPolicy / DecisionTrace 解决“如何基于证据做出可解释接受决策”的问题。
- OutcomeRecord / LearningSignal / EvolutionAction 解决“系统如何从真实结果中持续进化”的问题。

## 后续研究重点

1. 设计 AgentIdentity schema 与 agent registry。
2. 设计 PermissionGrant 的语义权限模型，区分 file scope、tool scope、data scope、runtime scope。
3. 设计 DelegationChain 可视化：从 human intent 到 release decision 的完整责任链。
4. 设计 Sandbox Runtime 架构选择：container vs microVM vs WASM，不同风险等级映射。
5. 设计 Tool Proxy DSL：声明 tool 权限、参数级控制、审计规则。
6. 设计 ExecutionTrace → EvidencePack 映射规则。
7. 设计 Verification Pipeline DSL：YAML vs code-based、可组合性、模板系统。
8. 设计 Verification cost model：时间 vs 覆盖率 vs 风险。
9. 设计 Decision Engine scoring model：融合 risk、quality、cost、confidence、agent reputation。
10. 设计 DecisionPolicy DSL 与 human override 机制。
11. 设计 Control Contract DSL：可组合规则、可继承模板、轻量/严格策略。
12. 设计 Contract × Verification 对齐机制。
13. 设计 Learning Signal 标注体系与 Policy 更新安全机制，避免误学习。
14. 设计 Evolution 审批流程与 Explainable Evolution。
15. 设计 Memory Safety 机制：哪些内容可以进入长期记忆，哪些必须标记为 tentative / expired / human-verified。
16. 设计 `.moxt/` 仓库规范：handoff、taskgraph、delivery-contract、risk-budget、decision-log、memory、delegation-spec、control-contract、evidence-pack、strategy-memory、release-decision、agent-identity、permission-grant、verification-pipeline、decision-policy、learning-signal。
