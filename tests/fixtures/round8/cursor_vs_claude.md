调研记录（2026-10 内部整理）

来源与口径：Cursor 官网 cursor.com/pricing（2026-09-28 读取）；Claude Code 文档 docs.claude.com（2026-10-02 读取）。以下价格为当月官网展示价，年付折扣未纳入。

Cursor：Pro 每用户每月 20 美元，含一定额度，超量按用量计费；Team 每用户每月 40 美元，含集中计费、SSO；Enterprise 需联系销售，官网未公布价格。官网称"多数 Pro 用户月内可用完额度"，但没有给超额用户的比例。

Claude Code：包含在 Claude Pro（20 美元/月）和 Max（100/200 美元/月）订阅中，也可通过 API 按 token 付费。按 token 计费的单价取决于所用模型（Sonnet/Opus 不同），本次未逐项记录。API 与订阅的使用条款不同，团队批量使用需看商业条款（未展开）。

功能对比（公开材料）：
- 代码补全：Cursor 有 Tab 补全；Claude Code 无内联补全，靠命令行对话。
- 多文件修改：两者都支持；Cursor 通过 Composer/Agent 模式，Claude Code 通过执行命令和编辑文件。
- 终端操作：Cursor 有终端并可让 Agent 在其中执行；Claude Code 本身就在终端里工作。
- IDE 集成：Cursor 是独立编辑器（VS Code 分支）；Claude Code 可装在 VS Code / JetBrains 插件里，也可纯终端。
- MCP 支持：两者都支持。
- 本地模型：Cursor 支持部分自定义 API；Claude Code 只能连 Anthropic 协议兼容端点（可通过代理）。

团队与隐私：Cursor 有 Privacy Mode，并宣称代码可在本地索引、不上传；具体企业合规资质（SOC2 等）本次未核实。Claude Code 的数据政策按 Anthropic 商业条款，具体是否训练模型本次未核实。

试用反馈（3 人小组，两周，均为前端为主）：
- 2 人觉得 Cursor 的补全和可视化 diff 更顺手；
- 3 人认为 Claude Code 在"改一个跨越十几个文件的逻辑"时更少改错；
- 1 人提到 Cursor 长会话后期变慢；
- 大文件（>5000 行）两者都有超时，Claude Code 需要先定位再改。
这是小样本主观反馈，不能当作评测结论。

外部数据：2026 年上半年开发者调查（非官方，样本 N=1200，自行招募）中，Cursor 使用率 38%，Claude Code 使用率 21%；同一调查中受访者表示"两个都用的"占 14%。该调查方法未公开，仅作参考。

结论线索（待业务判断）：
- 个人用：订阅价差不大，选补全还是命令行取决于习惯。
- 团队用：Cursor Team 有集中计费和管理，Claude Code 需要走 API 并自行管理成本，这一点可能影响采购决策，但差异有多大没有数据。
- 两者可同时使用。
