# Governance Baseline (yao-meta-skill · Library mode)

> 快照:2026-06-20 · axiom v21.1.0。本文件是 yao gate 的可见证据(governance.md Rule 5:drift must be observable)。

## Gate 结果

| Gate | 结果 | 关键数字 |
|------|------|---------|
| `validate_skill` | ✓ pass | 结构完整,含 agents/interface.yaml |
| `context_sizer` | ✓ 在预算内 | initial load 1293 tokens(library 预算 1300) |
| `resource_boundary_check` | ✓ pass | quality_density 54,无 unused dirs |
| `governance_check` | ✓ score 达 library 档 | 见下,band 由 draft→reusable→达标 |
| `trigger_eval` | 基线 | precision 1.0 / recall 0.5 |

## Trigger eval 明细

- should_trigger:3/6 命中(axiom 关键词 + 多信号案例)
- should_not_trigger:5/5 全拒(无误激活)
- near_neighbor:4/4 全拒
- 已知漏触发:单信号的「架构评审 / SDM 复杂开发 / 安全评估」请求得分低于 0.33 阈值——概念权重归一化后单概念得分被压平,单信号案例先天难过阈值。

## 已知缺口 / 下一步迭代方向(yao Phase 8)

1. **Trigger recall 硬化**:跑 `optimize_description.py`,把 cases 拆 train/dev/holdout,补 blind/adversarial holdout(yao Phase 9 promotion gate)。当前是单集合基线,未做泛化验证。
2. **多平台包装**:仅在需要多客户端分发时跑 `cross_packager.py`(axiom 当前 Claude-only)。
3. **回归节奏**:每次版本 bump 重跑本基线,漂移记录进 `evals/history/`。

## Library 模式产物清单

- `agents/interface.yaml` + `manifest.json`(治理元数据:owner / lifecycle=library / maturity=library / review_cadence=semiannual / context_budget_tier=library)
- `evals/`:trigger_cases.json、semantic_config.json、current_description.txt、history/
- `references/`:mental-models / expression-dna / delivery / operating-modes / cognitive-core / agentic-protocol + research/ + extraction-notes
- `reports/`:本文件
