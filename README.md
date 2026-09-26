# thesis-spss-results

一个供 Claude Code 使用的论文统计分析 Skill。它以已经整理好的研究数据为起点，引导 Claude 确认研究目标、选择和核查统计方法，并交付可直接用于论文的图表和 SPSS 可打开的 `.sav` 数据。

## 使用

将仓库目录放在 `~/.claude/skills/thesis-spss-results/`，或放在项目的 `.claude/skills/thesis-spss-results/`。在 Claude Code 中输入 `/thesis-spss-results`，并提供数据文件及研究问题。Claude Code 的[技能文档](https://code.claude.com/docs/en/skills)说明了个人和项目两种安装位置。

建议同时说明受试者 ID、组别、时间点、变量含义、量表计分规则，以及期望的论文图表或统计表。影响结论但未说明的设计选择需要在分析前确认。

## 分析基础与范围

Skill 优先使用 jamovi 官方的 [jmv](https://github.com/jamovi/jmv) R 包执行其支持的统计分析，并要求记录实际使用的软件和版本。它本身是工作流说明，不包含统计引擎，也不会自行生成分析结果。运行需要本机具备适用的 R 环境和数据处理、`.sav` 导出工具；具体依赖按任务确定。

`.sav` 是默认的数据交付格式。`.sps` 仅在对应 SPSS/PSPP 流程已经编写并核验时交付；`.spv` 仅在实际使用 IBM SPSS 生成后交付。论文图表和统计表应与分析数据一致。

仓库只包含 Skill 和说明，不包含研究数据。使用者应自行确认数据使用权限和论文报告要求。

## 许可

本仓库的 Skill 文本按 [MIT License](LICENSE) 发布。`jmv` 是独立的第三方项目，按其自身许可证发布；本仓库未包含其源代码。

