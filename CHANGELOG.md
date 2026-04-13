# Changelog

## [21.0.1] - 2026-04-13

### Fixed

- **INSTALL.md**: 统一所有 URL 为一致拼写（修复双 `s` / 单 `s` 混用和 Kiro 占位符）
- **INSTALL.md**: 符号链接路径与 git clone URL 保持一致
- **README.md**: 术语表 "12项不可妥协的交付要求" 改为准确描述 "12项交付标准（10项刚性+2项推荐）"
- **README.md**: 外部依赖表新增"获取方式"列和使用注意事项
- **SKILL.md**: description 添加英文激活关键词，提升非中文请求匹配率
- **04-external-views.md**: "11项A-K" 更新为 "12项A-L"（反映 v20.2 新增的 L 标准）
- **06-timeline.md**: "11项交付标准" 更新为 "12项交付标准" 并标注 v20.2 来源

### Added

- **.gitignore**: 排除 `.claude/settings.local.json` 和 `.agents/` 运行时目录
- **CHANGELOG.md**: 本文件

---

## [21.0.0] - 2026-04-13

### Added

- 基于 29 个核心规范的深度蒸馏版 SKILL.md
- 6 个核心心智模型（通过三重验证）
- 14 条决策启发式（含来源证据）
- 量化表达 DNA（确定性 5.7:1，结构化 54%）
- Agentic Protocol（3 步回答工作流：先研究再回答）
- 5 对显式保留的内在矛盾
- 8 条诚实边界（每条有证据）
- 12 项生产级交付标准（含 v20.2 新增的 L 标准）
- 6 路并行调研文档（`references/research/01-06.md`）
- 三重验证过程记录（`references/extraction-notes.md`）
- 多平台安装指南（Claude Code / Codex CLI / Kiro IDE）
- 示例对话（7 场景 + Agentic Protocol 演示）
