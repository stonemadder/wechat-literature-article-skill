# Demo Workflow

This demo shows the expected shape of a `wechat-literature-article` run. It does not include a real paper PDF or copyrighted figures. Use it as a pattern for testing the skill with an open-access paper or your own manuscript draft.

## 1. Input

Typical input:

```text
Use $wechat-literature-article to write a Chinese WeChat public-account article from this paper PDF.

Please use the standard research-reader length, include paper metadata, explain the data and methods carefully, select the most important figures, and output a Word document suitable for WeChat publishing.
```

Optional user preferences:

```text
Audience: graduate students and early-career researchers.
Length: about 3000 Chinese characters.
Figures: include the main result figure and one method figure if they are readable.
Tone: academic, clear, not promotional.
```

## 2. Source Intake

Before drafting, the skill should extract or confirm:

- paper title, journal, publication date, DOI, and article type;
- research question and claimed contribution;
- study area, period, samples, or experimental system;
- datasets, instruments, models, variables, and spatial or temporal resolution;
- method workflow, equations, thresholds, and validation approach;
- main figures, extended figures, tables, captions, and supplementary materials;
- key numbers with units, denominators, uncertainty, and source locations;
- limitations and assumptions stated by the paper.

If metadata are inconsistent, the paper front page, DOI page, publisher page, or official PDF should be preferred. The skill should not invent missing facts.

## 3. Internal Working Notes

The final article should not expose internal notes, but the working process should maintain them. A compact internal audit table can look like this:

| Item | Source | Use in article | Check |
| --- | --- | --- | --- |
| DOI | Paper front page | Metadata block | Confirmed |
| Main dataset | Methods section | Data and methods | Confirmed |
| Key effect size | Figure 2 and Results | Main result paragraph | Unit and denominator checked |
| Uncertainty range | Table 1 | Main result paragraph | Confidence interval checked |
| Limitation | Discussion | Discussion section | Kept with qualification |

A terminology list can look like this:

| English term | Chinese term | First-use note |
| --- | --- | --- |
| Aboveground carbon | 地上生物量碳 | Define abbreviation if the paper uses AGC |
| Disturbance | 扰动 | Keep distinct from land-use conversion |
| Recovery trajectory | 恢复轨迹 | Use consistently across results and discussion |

## 4. Article Shape

A publication-ready article should usually contain:

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

The exact headings can be adjusted for the paper, but the article should explain the scientific argument rather than simply follow the original figure order.

## 5. Figure Handling

Selected figures should satisfy these conditions:

- axes, legends, color bars, panel labels, and key annotations remain visible;
- surrounding article body text from the PDF is cropped out;
- each figure has a short Chinese explanation;
- each inserted figure is referenced near the relevant result;
- no figure is inserted only for decoration.

For Word output, inspect the rendered document when possible. Fix oversized figures, blurred labels, tables that exceed margins, and awkward page breaks before delivery.

## 6. Final Output

The final Word document should contain only publishable content:

- no internal terminology tables unless the user asks for them;
- no numeric audit table unless the user asks for it;
- no process notes such as "I checked this";
- no unverified bibliographic facts;
- no untranslated English headings unless requested.

Use [quality-rubric.md](quality-rubric.md) as the final review checklist before sharing or publishing the article.
