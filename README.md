# MOTX / Moxt AI Research Log

这个仓库用于持续沉淀关于 MOTX/Moxt 产品、软件研发 AI 同事、AI 原生工作空间与新研发作业范式的研究结果。

## 仓库结构

```text
README.md
SUMMARY.md
docs/
  full-design.md
  ai-teammates.md
  workspace-architecture.md
  workflow.md
  metrics.md
  risks.md
logs/
  YYYY-MM-DD/
    HH-mm.md
```

## 文件职责

| 文件 | 作用 |
|---|---|
| `SUMMARY.md` | 研究索引、阶段性摘要、最新结论导航 |
| `logs/YYYY-MM-DD/HH-mm.md` | 每次定时任务的原始增量研究记录 |
| `docs/full-design.md` | 当前累计沉淀出的全量设计方案 |
| `docs/ai-teammates.md` | AI 同事角色、职责、权限、协作边界、评价指标 |
| `docs/workspace-architecture.md` | AI 原生工作空间对象模型与架构 |
| `docs/workflow.md` | 软件研发新作业范式与流程 |
| `docs/metrics.md` | 效率与评估指标体系 |
| `docs/risks.md` | 权限、安全、治理边界 |

## 研究主题

研究 MOTX/Moxt 产品，持续推理和研究：在软件研发领域应该如何设置 AI 同事，每个 AI 同事如何定位、配置职责、工具权限、协作边界和评价指标，以及如何利用 AI 原生工作空间构建软件研发新作业范式、提高研发效率。

## 当前阶段性结论

Moxt 在软件研发领域的最佳切入点不是做“又一个代码编辑器”，而是做“AI 研发组织的工作空间”。核心价值是让多个 AI 同事在共享上下文、受控权限和可审计产物中协作，把研发流程从人类手工串行推进，升级为 AI 持续并行推进、人类重点审查决策。
