# WeChat Literature Article Skill

还在为导师布置的公众号文献介绍发愁？读完论文已经很累了，还要想标题、翻译摘要、讲清方法、裁主图、调 Word 格式、顺手把中文排版里的奇怪空格一个个揪出来？

你可能需要 `wechat-literature-article`。

这是一个面向中文科研公众号写作的 Codex skill，目标很朴素：把一篇英文学术论文，尤其是 Nature/Science 风格的研究论文，整理成一篇**能发、能读、方法讲得清楚、图也看得懂**的中文公众号文献推文。它不会把文章写成空泛的新闻稿，也不会只堆图和数字，而是会按照“论文信息、摘要、背景、数据与方法、结果、讨论、结论”的逻辑，把论文真正讲明白。

它特别适合这些场景：

- 导师或课题组要求写公众号文献介绍
- 想把英文论文整理成中文推文初稿
- 已经有草稿，但语言太口语、英文词太多、方法太空
- 需要把论文主图和附图裁好并配上中文说明
- 想顺便做一版组会文献分享 PPT

`wechat-literature-article` is a Codex skill for turning academic papers into Chinese WeChat public-account literature articles. It is designed for research-oriented summaries of Nature/Science-style papers, where accuracy, method detail, figure selection, and WeChat-ready formatting matter.

## What It Helps With

- Drafting a Chinese WeChat article from a paper PDF
- Revising a draft into a more academic, publishable style
- Explaining data, methods, calculations, results, and limitations in concrete terms
- Selecting and checking figures for article use
- Creating a rigorous but eye-catching WeChat title
- Cleaning Chinese typography and enforcing consistent Word fonts
- Controlling audience depth and article length
- Keeping terminology consistent and auditing key numbers
- Checking that every figure is referenced and explained
- Preparing a related journal-club PPT outline or deck

## Quickstart

Clone this repository into your Codex skills directory with the folder name expected by the skill:

```text
git clone https://github.com/Keyao-Wen/wechat-literature-article-skill.git ~/.codex/skills/wechat-literature-article
```

On Windows PowerShell:

```text
git clone https://github.com/Keyao-Wen/wechat-literature-article-skill.git "$env:USERPROFILE\.codex\skills\wechat-literature-article"
```

Restart Codex or start a new conversation if needed.

Then invoke the skill with:

```text
Use $wechat-literature-article to write a Chinese WeChat public-account article from this paper PDF.
```

## Repository Contents

- `SKILL.md`: the main Codex skill workflow and quality requirements.
- `examples/prompts.md`: ready-to-use prompts for article drafting, draft revision, and journal-club PPT preparation.
- `agents/openai.yaml`: app-facing metadata and default prompt for implicit invocation.
- `docs/demo.md`: a compact walkthrough of the expected input, workflow, and output shape.
- `docs/quality-rubric.md`: a practical checklist for judging whether an output is ready for publication.

## Quality Expectations

A good output from this skill should be more than a fluent Chinese summary. It should:

- preserve bibliographic facts, DOI, dates, units, and key numbers;
- explain data sources, methods, calculations, validation, and uncertainty in concrete terms;
- use consistent Chinese terminology for repeated technical concepts;
- select figures for evidence, not decoration;
- explain every inserted figure near the relevant result;
- keep internal audit notes out of the publishable Word document;
- render cleanly enough to copy into a WeChat public-account editor.

For a more detailed scoring guide, see [docs/quality-rubric.md](docs/quality-rubric.md).

## Example Prompts

The examples below are intentionally detailed. They tell Codex not only what to draft, but also how to audit numbers, handle figures, and keep working notes out of the final article.

```text
Use $wechat-literature-article to write a Chinese WeChat public-account article from this paper PDF. Please include a rigorous but eye-catching title, paper metadata, a concise abstract translation, detailed methods, main results, explained figures, discussion, and conclusion. Output as Word with clean Chinese typography.
```

```text
Use $wechat-literature-article to revise this draft. Make the language more academic, reduce English terms, improve the methods and conclusion sections, explain each selected figure, clean Chinese typography, standardize Word fonts, and check whether the figures are suitable for WeChat publishing.
```

```text
Use $wechat-literature-article to prepare an English journal-club PPT for this paper. Keep one claim per slide and include the core figures.
```

More examples are in [examples/prompts.md](examples/prompts.md).

## Scope

This skill contains workflow instructions only. It does not include paper PDFs, copyrighted figures, article drafts, or generated Word/PPT files.

When using copyrighted papers or figures, make sure you have the right to use or reproduce them in your publication context.

## License

MIT License. See [LICENSE](LICENSE).
