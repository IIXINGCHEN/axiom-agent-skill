# 认知核心机制（深度参考）

> 承接 SKILL.md 的 Ultrathink 4 阶段方法。

## Ultrathink 深度分析

触发条件：核心架构变更 / 高不确定性 / 用户手动激活。

4 阶段强制思维链：
1. **系统思维**：解构问题，分析全局上下文影响
2. **辩证与创新思维**：生成 ≥2 个方案，辩证分析优劣
3. **批判思维**：压力测试首选方案，识别盲点
4. **决策制定**：最终选择 + 明确理由 + 已知风险

---

## Ultrathink × cc-thinking-skills 技法映射（可选增强）

> 若已安装 [cc-thinking-skills](https://github.com/tjboudreaux/cc-thinking-skills) 插件，Ultrathink 每阶段可挂载具体推理技法。**不确定用哪个时先走 `thinking-model-router`；若没有任何模型明显适用，直接推理、不要硬套**（与 axiom 反仪式原则一致）。

| Ultrathink 阶段 | 推荐 cc 技能（按需选 1-2） | 触发场景 |
|----------------|---------------------------|---------|
| 系统思维 | `thinking-systems` / `thinking-feedback-loops` / `thinking-leverage-points` / `thinking-theory-of-constraints` | 跨服务调试、性能瓶颈、一处修复引发他处问题 |
| 辩证与创新 | `thinking-steel-manning` / `thinking-second-order` / `thinking-inversion` / `thinking-triz` | 方案对比、技术矛盾化解、反向思考 |
| 批判 | `thinking-pre-mortem` / `thinking-red-team` / `thinking-debiasing` / `thinking-kepner-tregoe` / `thinking-five-whys-plus` | 上线前风险、安全评审、根因、偏见检查 |
| 决策 | `thinking-bayesian` / `thinking-reversibility` / `thinking-opportunity-cost` / `thinking-occams-razor` | 不确定性下抉择、可逆性分级、资源取舍 |

> 直达示例：找瓶颈 → `thinking-theory-of-constraints`；攻击自测 → `thinking-red-team`；跨服务 bug → `thinking-systems`。
