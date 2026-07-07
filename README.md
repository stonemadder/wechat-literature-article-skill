# WeChat Literature Article Skill

[![Release](https://img.shields.io/github/v/release/Keyao-Wen/wechat-literature-article-skill?label=release)](https://github.com/Keyao-Wen/wechat-literature-article-skill/releases)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Codex Skill](https://img.shields.io/badge/Codex-skill-2F7D4A)](SKILL.md)

Turn academic papers into rigorous Chinese WeChat public-account literature articles.

`wechat-literature-article` is a Codex skill for research-oriented Chinese WeChat writing. It helps turn an academic paper, especially a Nature/Science-style paper, into a publishable article with accurate metadata, concrete methods, audited numbers, explained figures, clean Chinese typography, and Word-ready formatting.

还在为导师布置的公众号文献介绍发愁？读完论文已经很累了，还要想标题、翻译摘要、讲清方法、裁主图、调 Word 格式、顺手把中文排版里的奇怪空格一个个揪出来？

你可能需要 `wechat-literature-article`。

## Why This Exists

Most paper summaries fail in predictable ways: they sound fluent but skip methods, blur uncertainty, drop units, overuse English terms, or insert figures without explaining what they prove.

This skill is designed around a stricter idea: **a scientific WeChat article should be readable, but also auditable**.

It asks Codex to preserve the evidence chain from paper source to public article:

```text
paper metadata -> source intake -> terminology list -> numeric audit -> figure selection -> Chinese article -> Word/WeChat QA
```

## 30-Second Demo

Prompt:

```text
Use $wechat-literature-article to write a Chinese WeChat public-account article from this paper PDF.
Use the standard research-reader length, explain the data and methods carefully, include the core figures, and output a Word document suitable for WeChat publishing.
```

Expected output shape:

```text
Title

文章名称:
期刊:
发表时间:
DOI:

摘要
核心发现
研究背景
数据与方法
主要结果
讨论
结论与启示
```

Quality checks performed internally:

- bibliographic metadata are checked against the paper or DOI page;
- repeated technical terms are translated consistently;
- key numbers keep units, uncertainty, denominators, and source locations;
- figures are cropped with axes, legends, labels, and color bars visible;
- every figure is explained near the result it supports;
- internal audit notes stay out of the publishable Word document.

See [examples/synthetic-demo/README.md](examples/synthetic-demo/README.md) for a copyright-safe demo based on a fictional mini-paper.

## What Makes It Different

| Common prompt | This skill |
| --- | --- |
| "Summarize this paper in Chinese" | Builds a publishable WeChat article with metadata, methods, results, discussion, and conclusion |
| Often skips methods | Requires datasets, variables, model logic, validation, and uncertainty |
| May copy numbers loosely | Maintains an internal numeric audit table |
| Treats figures as decoration | Selects figures as evidence and checks figure-text correspondence |
| Leaves mixed English/Chinese style | Enforces consistent terminology and clean Chinese typography |
| Produces a draft only | Targets Word/WeChat-ready delivery |

## Best For / Not For

| Best for | Not for |
| --- | --- |
| Research-group WeChat paper introductions | One-click viral science news |
| Graduate students preparing literature posts | Casual popular-science rewriting with loose accuracy |
| Nature/Science-style research papers | Papers where you do not have access rights to figures or PDF content |
| Method-heavy papers that need careful explanation | Replacing domain expert review before public release |
| Draft revision, figure explanation, and Word cleanup | Inventing missing metadata, numbers, or claims |

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

More prompt templates are in [examples/prompts.md](examples/prompts.md).

## Repository Contents

- `SKILL.md`: the main Codex skill workflow and quality requirements.
- `examples/prompts.md`: ready-to-use prompts for article drafting, draft revision, and journal-club PPT preparation.
- `examples/synthetic-demo/README.md`: a fictional, copyright-safe example showing the expected evidence chain.
- `agents/openai.yaml`: app-facing metadata and default prompt for implicit invocation.
- `docs/demo.md`: a compact walkthrough of the expected input, workflow, and output shape.
- `docs/quality-rubric.md`: a practical checklist for judging whether an output is ready for publication.
- `ROADMAP.md`: planned improvements.
- `CHANGELOG.md`: release history.

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

## Scope

This skill contains workflow instructions only. It does not include paper PDFs, copyrighted figures, article drafts, or generated Word/PPT files.

When using copyrighted papers or figures, make sure you have the right to use or reproduce them in your publication context.

## Contributing

Good contributions include:

- better prompts for specific paper types;
- realistic demo cases based on open-access papers;
- stronger QA checklists for figures, tables, and Word layout;
- examples of common failure modes and how to fix them.

Please see [CONTRIBUTING.md](CONTRIBUTING.md) before opening an issue or pull request.

## License

MIT License. See [LICENSE](LICENSE).
