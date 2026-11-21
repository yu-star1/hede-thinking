# Hede Thinking / 合德语思考 (hede-thinking · v2.1)

> 🌐 Language / 语言: **English** | [中文](#中文版)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![Live Demo](https://img.shields.io/badge/Demo-Live-blue.svg)](https://yu-star1.github.io/hede-thinking/) [![Version](https://img.shields.io/badge/version-v2.1-purple.svg)](https://github.com/yu-star1/hede-thinking)

---

## English

> Make your AI think logically and close with a plain-language version — one file, drop it into any AI.

> **Naming note**: Hede Language is the formal name of this language specification; `hede-thinking` is this skill's identifier — it is Hede Language's **thinking-domain application** (teaches machines how to think), hence the name "Hede Thinking".

### What is it (in 3 sentences)

1. **Hede Language** is a thinking and expression specification written for AI: when thinking, the AI first shows its cards (📌 assertion / 🔍 to-verify / 📚 memorize / ⚡ action), every conclusion must carry a verifiable anchor, and failures must be reported honestly without rhetorical packaging.
2. It cures AI's four chronic ailments: **vagueness** (you can't tell which line is a guess), **fabrication** ("I verified it" with no follow-through), **derailment** (the longer the conversation, the more it copies wrong), **forgetfulness** (what you taught it resets to zero next session).
3. This upgrade adds **/eli5 plain-language version**: even the most obscure documents, papers, and technical conclusions get a one-sentence plain-language counterpart — the technical verdict gives you a table you can decide from, while the plain-language version makes you understand in seconds.

### What's in the package

| File | Purpose |
|---|---|
| `SKILL.md` | **Main body**: complete specification of the Hede Thinking skill (v2.1, including verdict table + eli5 + HEDE-MEMO memory format), self-contained with zero dependencies |
| `hede-bench.html` | A single page for human readers: beginner-friendly diagrams + real-world test scorecard, with EN/中文 language toggle (viewable on open, can be hosted on a website) |
| `poster.jpg` | The finished promotional poster image |
| `README.md` | This file (bilingual: English + 中文) |

### Getting started in three minutes

**Route A · Paste the prompt (5 minutes, works with any AI)**

1. Open `SKILL.md` and find **§9 Minimal onboarding package**;
2. Copy the entire section and paste it into your AI's "custom instructions / system prompt / System Prompt";
3. Save. It takes effect in new conversations — see whether your AI's thinking starts showing 📌🔍📚⚡.

**Route B · Install the skill file (tools that support a skills mechanism)**

1. Put `SKILL.md` into the tool's skills directory, e.g. `.zcode/skills/hede-thinking/SKILL.md` (Claude Code / ZCode etc. follow their own conventions);
2. Restart with a new session;
3. Say "**Hede Thinking**" to the AI to invoke it; say "**plain-language version**" or "**$eli5**" to get the plain-language version.

**Verify it's installed**

Toss any small task at the AI and watch its thinking process:
- ✅ Every section starts with a 📌/🔍/📚/⚡ tag;
- ✅ Conclusions are followed by a reading/file path/number (anchor);
- ✅ The task ends with a "closing reconciliation" (four lines: anchor count / closure / memorize / backfill).
- Missing any one? It means the host didn't load it successfully — switch to Route A and try again.

### FAQ

**Q: Does it still work with a different model?**
Works. The specification is written at the prompt layer and is model-agnostic. Real-world note: different models vary widely in "self-compliance rate" (we measured a compliance rate of 41.88% without the specification loaded and 94.40% with it loaded) — so after switching models, we recommend running a self-check per `SKILL.md` §10 J5.

**Q: Will it burn a lot of tokens?**
No noticeable increase (about +3 tokens/line, <5% overall). What it saves isn't tokens — it's trust cost: you no longer have to repeatedly probe "is this line a guess or verified?"

**Q: Will the tags box the AI in and make it mechanical?**
No. The specification hard-codes two safeguards: core reasoning always uses natural language and is never templated; high-risk operation segments (actual code edits / deletions / outbound sends) can switch back to pure Chinese thinking. Tags are behavioral markers, not content compression (we ran four rounds of experiments on the content-compression approach and all disproved it — don't try it).

**Q: My AI has no memory feature — is "📚 memorize" still useful?**
Yes. §7 designs three levels of adaptation: if it has a memory tool, use the tool (Level A); if it has a file system, write to the `hede_memos/` directory (Level B); if it's pure conversation, output a standard MEMO code block at closing, which you copy and save yourself and paste back next time (Level C). All three levels share a unified format, so you can upgrade anytime without losing data.

**Q: How is this different from format constraints like "make the AI output JSON/tables"?**
Those constrain how output looks; Hede Language constrains **thinking behavior**: every assertion must be verifiable, every question must be resolved, every piece of experience must be accumulable — it manages the AI's thinking ledger, not just formatting.

**Q: What's the relationship between Hede Language and hede-thinking?**
Hede Language is the proper name of the language specification; `hede-thinking` is this skill's directory identifier — it is Hede Language's thinking-domain application (the part that teaches machines how to think), hence "Hede Thinking". Use the name hede-thinking when installing; when introducing it externally, just say "Hede Language".

### Version

- **v2.1** (2026-11-20): Closing-output layer upgrade — verdict table (multi-step tasks must produce a comparison table at closing) + eli5 plain-language version (trigger words `$eli5` / `plain-language version`).
- v2.0 (2026-11-01): Skill whitepaper finalized + HEDE-MEMO three-level memory adaptation.
- Data source: All readings come from real-world tests using pre-registered criteria sets (success criteria are fixed in writing before the run to prevent retrofitting), see `SKILL.md` §5 and §10 for details.

---

## 中文版

> 让你的 AI 按逻辑思考、讲人话收口——一个文件，装进任意 AI。

> **命名说明**：合德语（**Hede Language**）是这套语言规范的正式名称；`hede-thinking` 是本 skill 的标识——它是合德语的**思考域应用**（教机器怎么思考），故名"合德语思考"。

### 这是什么（3 句话）

1. **合德语**是一套写给 AI 的思考与表达规范：AI 思考时先亮牌（📌 断言 / 🔍 待查 / 📚 要记 / ⚡ 行动），每句结论必带可查证的锚，失败如实报告不许话术包装。
2. 它治 AI 的四大老毛病：**含糊**（哪句是猜的听不出）、**编造**（"我验证过了"没下文）、**翻车**（长对话越抄越错）、**健忘**（教过的下个会话清零）。
3. 本次升级加入 **/eli5 讲人话**：再晦涩的文档、论文、技术结论，一句话翻成大白话对照——技术判定给你可拍板的表，人话版让你秒懂。

### 包里有什么

| 文件 | 用途 |
|---|---|
| `SKILL.md` | **主体**：合德语思考 skill 完整规范（v2.1，含定论表 + eli5 + HEDE-MEMO 记忆格式），自包含零依赖 |
| `hede-bench.html` | 给人看的单页：小白图解 + 实测成绩单，支持中英语言切换（打开即看，可挂官网） |
| `poster.jpg` | 成品宣传海报图 |
| `README.md` | 本文件（中英双语） |

### 三分钟上手

**路线 A · 贴提示词（5 分钟，任何 AI 都行）**

1. 打开 `SKILL.md`，找到 **§九 最小接入包**；
2. 整段复制，贴进你的 AI 的"自定义指令 / 系统提示 / System Prompt"；
3. 保存。新对话生效——看 AI 思考是不是开始挂 📌🔍📚⚡ 了。

**路线 B · 装 skill 文件（支持 skills 机制的工具）**

1. 把 `SKILL.md` 放进工具的 skills 目录，如 `.zcode/skills/hede-thinking/SKILL.md`（Claude Code / ZCode 等按各自约定）；
2. 重开新会话；
3. 对 AI 说"**合德语思考**"即可唤起；说"**讲人话**"或"**$eli5**"出大白话版。

**验证装好了没**

随便丢给 AI 一个小任务，看它的思考过程：
- ✅ 每段开头有 📌/🔍/📚/⚡ 标签；
- ✅ 结论后面跟着读数/文件路径/编号（锚）；
- ✅ 任务结尾有一段"收口对账"（锚数/闭环/落库/回填四行）。
- 缺一样？说明宿主没加载成功，换路线 A 重试。

### 常见问题（FAQ）

**Q：换一个模型还管用吗？**
管用。规范是写在提示词层的，与模型无关。实测提醒：不同模型"自觉遵守率"差异很大（我们测到未加载规范时合规率 41.88%，加载后 94.40%）——所以换模型后建议按 `SKILL.md` §十 J5 做一次自检。

**Q：会不会很费 token？**
不会明显增加（约 +3 token/行，整体 <5%）。它省的不是 token，是信任成本——你不用反复试探"这话是猜的还是验过的"。

**Q：AI 会不会被标签框死，变得机械？**
不会。规范里写死两条保险：核心推理永远用自然语言不模板化；高风险操作段（编码实改/删除/外发）可切回纯中文思考。标签是行为标记，不是内容压缩（内容压缩路线我们实验四轮，全部证伪，别试）。

**Q：我的 AI 没有记忆功能，"📚 落库"还有用吗？**
有。§七设计了三级适配：有记忆工具走工具（A 级）、有文件系统写 `hede_memos/` 目录（B 级）、纯对话就在收口时输出标准 MEMO 代码块，你自己复制保存、下次贴回去即可（C 级）。三级格式统一，随时升级不丢数据。

**Q：和"让 AI 输出 JSON/表格"这类格式约束有什么区别？**
那些约束输出长相，合德语约束**思考行为**：每句断言必须可查证、每个疑问必须有着落、每条经验必须可积累——它管的是 AI 想问题的账，不止排版。

**Q：合德语和 hede-thinking 是什么关系？**
合德语（**Hede Language**）是语言规范的正名；`hede-thinking` 是本 skill 的目录标识——它是合德语的思考域应用（教机器怎么思考的那部分），所以叫"合德语思考"。装的时候用 hede-thinking 这个名字，对外介绍时说"合德语"即可。

### 版本

- **v2.1**（2026-11-20）：收口输出层升级——定论表（多步任务收口必出对照表）+ eli5 讲人话（触发词 `$eli5`/`讲人话`）。
- v2.0（2026-11-01）：技能白皮书定稿 + HEDE-MEMO 三级记忆适配。
- 数据出处：全部读数出自预注册判据卷实测（跑前先写死成功标准，防事后找补），详见 `SKILL.md` §五、§十。

---

## License / 许可证

Released under the **MIT License** — see [LICENSE](LICENSE). 本项目采用 **MIT 许可证**，详见 [LICENSE](LICENSE)。

You are free to **use, copy, modify, merge, publish, distribute, sublicense, and/or sell** copies of this project, for personal or commercial purposes. The only requirement is to keep the copyright notice and this permission notice in any copy or substantial portion. No warranty is provided.

你可以自由**使用、复制、修改、合并、发布、分发、再授权，乃至出售**本项目副本，可用于个人或商业用途。唯一要求是在任何副本或实质部分中保留版权声明与许可声明。不提供任何担保。

In plain terms / 大白话：拿去用、随便改、尽管分享，拿去做产品赚钱也行——只要留着署名那一行。

## Contributing / 贡献

Issues and pull requests are welcome. If you find a wording issue in the translation, have an idea for a new section, or want to add a language edition, open an issue or submit a PR. 欢迎提 Issue 和 Pull Request——发现译文问题、想加新章节、或想新增语言版本，都可以开 issue 或提交 PR。

## Star this repo / 点个星

If this project helped you, a ⭐ star is the easiest way to support it and help others discover it. 如果这个项目帮到了你，点个 ⭐ 是最简单的支持方式，也能帮更多人发现它。
