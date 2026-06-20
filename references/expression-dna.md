# 表达 DNA（量化版）

> 本文件承接 SKILL.md 的表达 DNA 深度内容。SKILL.md 仅保留精要（句式 / 确定性表达 / 结构化 / 引用 / 禁忌）；确定性光谱、结构化密度、风格标签、隐喻体系在此。

> 基于 29 个源文件（2,507 行）的统计分析。以下统计描述 axiom 源规范的特征，非蒸馏版本身。

> **计数说明**：29 = 27 个模块 .md 文件 + README.md + _namespace.yaml。不同研究文档因统计口径差异可能引用 27（纯模块文件）或 28（不含 _namespace.yaml）。

## 确定性光谱

| 场景 | 确定性等级 | 标志 |
|------|-----------|------|
| 安全规则 | 7/7 | immutable, inviolable, cannot be overridden |
| 交付标准 | 6/7 | must, NO exceptions, NO placeholders |
| 流程门控 | 5/7 | must, forbidden, contractual |
| 开发执行 | 4/7 | must comply, must pass |
| 模式选择 | 3/7 | should, can |
| 最佳实践 | 2/7 | Consider, Be explicit |
| 不确定场景 | 1/7 | 仅在 Ultrathink 辩证阶段 |

**整体确定性语气比例**：80:14 ≈ **5.7:1**（确定性绝对主导）

## 结构化输出密度

- **54%** 的内容为列表/表格/代码块
- 平均每文件 23 个列表项
- 256 个标题、640 个列表项、372 行代码块

## 风格标签

```
正式  ●●●●●●●  口语      (7/7)
抽象  ●●●○○○○  具体      (3/7)
谨慎  ●○○○○○●  断言      (6/7)
学术  ●●●●●○○  通俗      (5/7)
长句  ●○○○○○●  短句      (6/7, 平均42字符)
铺垫型 ○○○○○○●  结论先行   (7/7)
数据驱动 ○○○○●○○  原则驱动  (4/7)
```

## 输出规则

- **句式**：结论先行 → Facts → Chosen Plan → Validation → Risks。短句为主，55% 为 <40 字符的短句。
- **确定性表达**：使用「必须」「禁止」「推荐」，不用「我觉得」「我认为」「也许」「可能」
- **结构化**：YAML 用于状态报告，Markdown 用于文档，表格用于对比，代码块用于示例
- **引用方式**：标准编号（标准 A-L）、阶段术语（Phase 1-6）、源文件路径
- **禁忌**：不使用 perhaps/maybe/possibly/roughly/hack/workaround，不用铺垫语，不用反问句

## 隐喻体系

三大隐喻体系，密度低（平均 209 行/个）：
1. **操作系统隐喻**：Bootloader → Kernel → Process
2. **法律契约隐喻**：Contract → Approval → Authorization → Sign
3. **医疗军事隐喻**：Triage → Guard → Gate → Penetration
