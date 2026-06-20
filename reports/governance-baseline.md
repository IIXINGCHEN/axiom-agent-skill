# Governance Baseline (yao-meta-skill · Library mode)

> 快照:2026-06-20 · axiom v21.1.0。本文件是 yao gate 的可见证据(governance.md Rule 5:drift must be observable)。

## Gate 结果

| Gate | 结果 | 关键数字 |
|------|------|---------|
| `validate_skill` | ✓ pass | 结构完整,含 agents/interface.yaml |
| `context_sizer` | ✓ 在预算内 | initial load 1293 tokens(library 预算 1300) |
| `resource_boundary_check` | ✓ pass | quality_density 54,无 unused dirs |
| `governance_check` | ✓ score 达 library 档 | 见下,band 由 draft→reusable→达标 |
| `trigger_eval` | ✓ recall 已硬化 | precision 1.0 / recall 1.0(threshold,跨 dev/holdout/blind/adversarial) |

## Trigger eval 明细(recall 已硬化,2026-06-20)

- 根因:评分器归一化 positive 权重,5 个过细概念单概念得分 <0.33。修法:合并为 2 强概念(axiom_keyword 0.45 + engineering_cognitive 0.55)+ 加「根因/复盘/事故」短语 + 加 do_not_directive exclusive 负向。
- `optimize_description.py` 跨 4 拆分集(dev/holdout/blind/adversarial,全新案例):threshold 层 dev 0 / holdout 0 / blind 0 / adversarial 0 错,adversarial risk_band=healthy,precision 1.0 / recall 1.0。候选 6 个,当前 description 胜出。
- 泛化保证:holdout/blind/adversarial 是未参与调参的新案例(反过拟合)。
- 残留:judge_blind(独立 rubric 评审)仍标 2 个诊断类措辞为边界(threshold 层已正确处理);属 description 清晰度残余,受 1300 预算约束。
- 注:yao `promotion_checker`/suite-runner 绑定 yao 自身 root+example 技能(要 `targets` suite),对外部技能 axiom 不直接适用;`optimize_description` 跨拆分集零错即为实质晋升证据。

## 已知缺口 / 下一步迭代方向

1. ~~Trigger recall 硬化~~ ✓ 已完成(threshold 层 recall 1.0)。残余:judge_blind 2 例边界(description 清晰度,预算约束)。
2. **多平台包装**:仅在需要多客户端分发时跑 `cross_packager.py`(axiom 当前 Claude-only)。
3. **回归节奏**:每次版本 bump 重跑本基线,漂移记录进 `evals/history/`。

## Library 模式产物清单

- `agents/interface.yaml` + `manifest.json`(治理元数据:owner / lifecycle=library / maturity=library / review_cadence=semiannual / context_budget_tier=library)
- `evals/`:trigger_cases.json、semantic_config.json、current_description.txt、history/
- `references/`:mental-models / expression-dna / delivery / operating-modes / cognitive-core / agentic-protocol + research/ + extraction-notes
- `reports/`:本文件
