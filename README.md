# Hede Thinking Skill Sharing Package (hede-thinking · v2.1)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![Live Demo](https://img.shields.io/badge/Demo-Live-blue.svg)](https://yu-star1.github.io/hede-thinking/) [![Version](https://img.shields.io/badge/version-v2.1-purple.svg)](https://github.com/yu-star1/hede-thinking)

> Make your AI think logically and close with a plain-language version — one file, drop it into any AI.
>
> **Naming note**: Hede Language is the formal name of this language specification; `hede-thinking` is this skill's identifier — it is Hede Language's **thinking-domain application** (teaches machines how to think), hence the name "Hede Thinking".

## What is it (in 3 sentences)

1. **Hede Language** is a thinking and expression specification written for AI: when thinking, the AI first shows its cards (📌 assertion / 🔍 to-verify / 📚 memorize / ⚡ action), every conclusion must carry a verifiable anchor, and failures must be reported honestly without rhetorical packaging.
2. It cures AI's four chronic ailments: **vagueness** (you can't tell which line is a guess), **fabrication** ("I verified it" with no follow-through), **derailment** (the longer the conversation, the more it copies wrong), **forgetfulness** (what you taught it resets to zero next session).
3. This upgrade adds **/eli5 plain-language version**: even the most obscure documents, papers, and technical conclusions get a one-sentence plain-language counterpart — the technical verdict gives you a table you can decide from, while the plain-language version makes you understand in seconds.

## What's in the package

| File | Purpose |
|---|---|
| `SKILL.md` | **Main body**: complete specification of the Hede Thinking skill (v2.1, including verdict table + eli5 + HEDE-MEMO memory format), self-contained with zero dependencies |
| `hede-bench.html` | A single page for human readers: beginner-friendly diagrams + real-world test scorecard (viewable on open, can be hosted on a website) |
| `poster-prompt.md` | AI image-generation prompts for the promotional poster (base-image prompt + list of copy to overlay) |
| `README.md` | This file |

## Getting started in three minutes

### Route A · Paste the prompt (5 minutes, works with any AI)

1. Open `SKILL.md` and find **§9 Minimal onboarding package**;
2. Copy the entire section and paste it into your AI's "custom instructions / system prompt / System Prompt";
3. Save. It takes effect in new conversations — see whether your AI's thinking starts showing 📌🔍📚⚡.

### Route B · Install the skill file (tools that support a skills mechanism)

1. Put `SKILL.md` into the tool's skills directory, e.g. `.zcode/skills/hede-thinking/SKILL.md` (Claude Code / ZCode etc. follow their own conventions);
2. Restart with a new session;
3. Say "**Hede Thinking**" to the AI to invoke it; say "**plain-language version**" or "**$eli5**" to get the plain-language version.

### Verify it's installed

Toss any small task at the AI and watch its thinking process:
- ✅ Every section starts with a 📌/🔍/📚/⚡ tag;
- ✅ Conclusions are followed by a reading/file path/number (anchor);
- ✅ The task ends with a "closing reconciliation" (four lines: anchor count / closure / memorize / backfill).
- Missing any one? It means the host didn't load it successfully — switch to Route A and try again.

## FAQ

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

## Version

- **v2.1** (2026-11-20): Closing-output layer upgrade — verdict table (multi-step tasks must produce a comparison table at closing) + eli5 plain-language version (trigger words `$eli5` / `plain-language version`).
- v2.0 (2026-11-01): Skill whitepaper finalized + HEDE-MEMO three-level memory adaptation.
- Data source: All readings come from real-world tests using pre-registered criteria sets (success criteria are fixed in writing before the run to prevent retrofitting), see `SKILL.md` §5 and §10 for details.

## License

Released under the **MIT License** — see [LICENSE](LICENSE).

You are free to **use, copy, modify, merge, publish, distribute, sublicense, and/or sell** copies of this project, for personal or commercial purposes. The only requirement is to keep the copyright notice and this permission notice in any copy or substantial portion. No warranty is provided.

In plain terms: take it, use it, change it, share it, even build a product on it — just keep the attribution line.

## Contributing

Issues and pull requests are welcome. If you find a wording issue in the translation, have an idea for a new section, or want to add a language edition, open an issue or submit a PR.

## Star this repo

If this project helped you, a ⭐ star is the easiest way to support it and help others discover it.
