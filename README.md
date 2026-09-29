# 情绪周期（laogu-sentiment）

市场测温——7 维公开指标判定市场处于 5 个情绪阶段中的哪一段，叠加贪婪-恐惧钟摆解读。测温不预测拐点、不预测涨跌，只回答现在市场是什么温度。

## 功能速览

- 7 维打分：涨跌家数比、涨跌停家数比、连板高度、炸板率、两市成交额分位、全A平均换手率、北向成交占比
- 5 阶段判定：冰点期 / 情绪修复期 / 情绪升温期 / 情绪高涨期 / 过热分歧期
- 温度计三档强制结论：过热 / 中性 / 冰冷（附"这意味着什么 / 不意味着什么"）
- 霍华德·马克斯贪婪-恐惧钟摆解读：只描述位置，不预测拐点
- 每维写清"怎么算、阈值怎么定、取不到怎么办"；数据不足（已核验维度 <5）时不强行判定

## 一键安装

```bash
# 方式一：克隆仓库
git clone https://github.com/laogu-caibao/laogu-sentiment.git

# 方式二：下载 ZIP
# https://github.com/laogu-caibao/laogu-sentiment/archive/refs/heads/main.zip

# 方式三：npx 一键安装
npx skills add laogu-caibao/laogu-sentiment
```

- Claude Code：放到 `~/.claude/skills/laogu-sentiment/`
- 扣子：扣子编程 → 技能面板 → 创建技能 → 本地上传（仓库根目录已有 SKILL.md，直接压缩仓库文件夹即可）；页面要求 `.skill` 后缀时由扣子导入后自动生成，**不要只改 zip 扩展名**
- Trae：设置 → 技能 → 上传技能（同上 zip）；或手动放到 `~/.trae/skills/laogu-sentiment/`（TRAE Work 国区版路径为 `~/.trae-cn/skills/`）
- MCP 一次装全：`uvx laogu-mcp`（16+ 个工具，含本 skill 对应的测温数据接口）

## 合规声明

本 skill 不输出任何买卖建议，阶段判定仅为情绪描述。全文禁用"见底/见顶/抄底/逃顶/加仓/减仓"等暗示操作的用语。

---

## English

**laogu-sentiment — Market sentiment gauge.** Seven indicators, five phases of the sentiment cycle — a temperature reading of the A-share market, explicitly not a turning-point predictor. Install: `npx skills add laogu-caibao/laogu-sentiment`.

## FAQ

**Q：laogu-sentiment 有什么用？**
适合的场景：想知道现在市场情绪处于贪婪还是恐惧、在情绪周期五阶段里走到哪一步（测温，不预测拐点）。

**Q：数据可靠吗？会荐股吗？**
数字必须来自可核验的公开来源（上市公司公告、交易所公开数据、公开网页），取不到就标「未核验」，绝不编造；只做结构化整理与解读，不构成投资建议。

**Q：怎么安装？支持哪些 AI 平台？**
```bash
npx skills add laogu-caibao/laogu-sentiment
```
平台中立 Markdown，Claude Code、Codex、豆包智能体、Workbuddy、扣子 Coze、Trae 等环境均可用；数据能力可用 [laogu-mcp](https://github.com/laogu-caibao/laogu-mcp)（`uvx laogu-mcp`）一次装齐。更多 skill 见[老谷拆财报组织主页](https://github.com/laogu-caibao)。
---

## 出品：老谷拆财报

以数据为刃，剖市场真相。

- 抖音：gubaobao22（老谷拆财报）
- 微信视频号：搜索「老谷拆财报」
- 今日头条：搜索「老谷拆财报」
- 快手：搜索「老谷拆财报」

财经科普、财报解读。个人观点，仅供参考，不构成投资建议。
