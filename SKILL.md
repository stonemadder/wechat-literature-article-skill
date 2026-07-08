---
name: wechat-literature-article
description: Use when drafting, revising, or packaging a Chinese WeChat public-account literature article from an academic paper PDF, DOI, URL, extracted text, notes, or existing draft. Focuses on accurate paper metadata, evidence mapping, concise abstract translation, concrete methods and data explanation, numeric audit, terminology consistency, figure explanation, Chinese academic style, clean typography, and Word/WeChat-ready article output. Do not use for presentation or slide-deck creation.
---

# WeChat Literature Article

Use this skill to turn an academic paper into a Chinese 微信公众号文献推文, or to revise an existing draft into a publishable research-oriented WeChat article.

## Core Mandate

- Write for research-aware Chinese readers: academic, clear, and suitable for WeChat publishing.
- Preserve scientific accuracy over narrative smoothness.
- Build an evidence chain from source material to final prose: metadata -> source intake -> terminology list -> numeric audit -> figure selection -> article -> Word/WeChat QA.
- Keep final deliverables publishable: remove process notes, internal comments, unnecessary English source text, and draft-only explanations.
- Treat presentation and slide-deck creation as out of scope. If the user asks for slides, route to a presentation-focused workflow instead.

## Input Modes

Handle sources according to what the user provides:

- **Full PDF**: extract metadata, abstract, methods, figures, tables, captions, key numbers, limitations, and supplementary references when available.
- **DOI or publisher URL**: use available metadata and article text; ask for the PDF or extracted text if full methods, figures, or key results are not accessible.
- **Extracted text or notes**: draft only from supplied content; mark missing figures, tables, methods, or uncertainty details as unavailable rather than inventing them.
- **Existing Chinese draft**: preserve useful structure, then revise for accuracy, terminology, methods depth, numeric support, figure explanation, and WeChat-ready style.
- **Scanned/image PDF**: use OCR if available; if extraction quality is poor, state the limitation and ask for selectable text, official PDF, or key sections.
- **Insufficient source**: do not draft a fact-rich article from title/abstract alone unless the user explicitly accepts a limited abstract-based version.

## Missing Information and Uncertainty

When facts are missing, ambiguous, or not extractable:

- do not invent metadata, sample sizes, datasets, equations, uncertainty ranges, or figure interpretations;
- prefer the paper front page, DOI page, publisher page, official PDF, and then supplementary materials, in that order;
- explicitly track unresolved items in working notes;
- qualify the final prose when a claim is supported only by abstract-level or partial information;
- ask for the missing source only when it is necessary for a reliable article.

Use cautious wording such as “文中报告”, “结果提示”, “在该研究设定下”, and “基于作者提供的数据” when uncertainty or scope limits remain.

## Deliverable Contract

Separate publishable output from working materials.

If creating files, prefer this structure:

- `final_article.docx`: publishable WeChat article only.
- `working_notes.md`: source intake, terminology list, numeric audit, unresolved metadata, and QA notes.
- `figure_notes.md`: selected figures, crop notes, source panels, and Chinese figure explanations.
- `qa_report.md`: final checklist results and remaining caveats.

If the user asks for only chat output, keep internal audit concise and do not expose large working tables unless requested.

The final article must not contain internal checklists, extraction notes, “I checked” process language, unresolved TODOs, or hidden assumptions.

## Evidence Mapping

Every major result claim should map to at least one source location:

- paper text section or paragraph;
- figure number and panel;
- table number;
- supplementary figure/table;
- equation or methods step;
- DOI/publisher metadata page for bibliographic facts.

For each key number, internally track:

- value and unit;
- denominator, baseline, sample size, or comparison group;
- uncertainty, confidence interval, or error range when reported;
- source figure/table/text location;
- how the number is used in the article;
- whether the number was cross-checked.

Do not present figure-estimated values as exact values unless the paper itself reports them exactly.

## Audience and Length

Choose or infer the target depth. If the user does not specify, use the standard research-reader version.

- 简短版：about 1500-2500 Chinese characters, for quick WeChat reading.
- 标准版：about 2500-3500 Chinese characters, for research-aware readers and most public-account posts.
- 专业版：about 3500-5000 Chinese characters, for specialist readers or method-heavy papers.

Keep the article proportional. Method-heavy papers may need more space in “数据与方法”; discovery or mechanism papers may need more space in “主要结果” and “讨论”. Do not pad the article just to meet a length target.

## Article Structure

Choose a WeChat title before the article body. The title should be eye-catching but rigorous: it may highlight the paper's core tension, surprising result, scale, or implication, but must not exaggerate, overclaim, or use clickbait.

Start the article body with bibliographic metadata:

- 文章名称
- 期刊、卷期页码或在线发表信息
- DOI
- 发表时间

Then organize the article by content rather than by figure order:

1. 摘要
2. 引言/研究背景
3. 数据与方法
4. 主要结果
5. 讨论
6. 结论与启示

The abstract section should be a concise Chinese translation and compression of the original abstract, not a loose summary. Add a short “核心发现” section when it helps readers scan the paper.

## Terminology Consistency

Create an internal terminology list before drafting when the paper contains repeated technical terms, variables, datasets, model names, or abbreviations.

Track:

- English source term;
- preferred Chinese translation;
- abbreviation, if any;
- first-use explanation;
- terms that must not be mixed.

For example, do not alternate between “地上碳”, “地上生物量碳”, and “地上碳储量” unless the paper distinguishes those concepts. Use the most accurate term consistently.

## Methods Section

The methods section must be concrete enough for readers to understand what was done. Avoid vague phrases such as “using remote-sensing analysis” without explaining inputs and calculations.

Prefer this order:

1. 数据输入：dataset names, time range, spatial/temporal resolution, variables
2. 研究对象与分类：sample selection, study objects, categories, masks, exclusions
3. 扰动或处理识别：event definition, thresholds, classification rules, grouping
4. 模型或计算方法：statistical model, physical model, equations, fitting logic, parameter estimation
5. 结果计算：how core metrics, changes, losses, gains, risks, or effects were derived
6. 不确定性与验证：validation data, sensitivity analysis, uncertainty propagation, comparison with independent observations

For method-heavy papers, use small subheadings and short explanatory paragraphs instead of wide tables that may overflow in Word or WeChat.

## Domain Adaptation

Adjust the methods explanation to the paper type:

- **Ecology, climate, remote sensing, and Earth system papers**: emphasize study area, period, spatial/temporal resolution, variables, masks, event definitions, baseline choice, validation, and uncertainty propagation.
- **Biomedical and clinical papers**: emphasize cohort or sample definition, inclusion/exclusion criteria, endpoints, intervention or exposure, statistical model, confounder adjustment, effect size, confidence interval, ethics/approval if relevant, and limitations. Do not translate associations into clinical recommendations.
- **AI, computational, and modeling papers**: emphasize task definition, dataset split, baseline models, evaluation metrics, ablations, uncertainty or robustness tests, compute/data limitations, and whether claims are empirical or theoretical.
- **Social science, policy, and economics papers**: emphasize data source, identification strategy, controls, robustness checks, external validity, and causal limitations.
- **Review, perspective, or synthesis papers**: distinguish author interpretation from primary evidence; avoid presenting a narrative claim as a new experimental result.

## Results Section

Each result subsection should contain:

- a clear result claim;
- exact key numbers with units and uncertainty when reported;
- interpretation of what the numbers mean;
- figure or table support when it directly helps explain the result.

Do not merely list numbers. Explain how the numbers support the paper’s argument. When applicable, distinguish gross change, net change, baseline, denominator, sample size, and uncertainty.

## Figures

Figures support the explanation; they should not determine the article structure.

Prioritize:

- core main figures that carry the main results;
- one important methodological extended or supplementary figure when it clarifies the workflow;
- one additional supporting figure only if it helps explain the overall conclusion.

Before inserting a figure:

- crop to include axes, legends, color bars, panel letters, and key labels;
- avoid including surrounding body text from the PDF;
- do not cut off axis titles, tick labels, legends, or color scales;
- check figure clarity after insertion into Word;
- write short Chinese captions explaining what the figure supports.

Do not translate long original figure legends verbatim.

Every selected figure must have a short explanatory note in Chinese. The note should be concise but self-contained: readers should understand what the figure shows, which panels or axes matter, and how it supports the adjacent result.

Run a figure-text correspondence check before delivery:

- every inserted figure must be referenced and explained in the nearby text;
- every figure mentioned in the text should be inserted, unless there is a clear reason not to;
- no orphan figures should remain;
- figure order should follow the article logic, not necessarily the paper’s original figure order.

## Language Style

- Use formal academic Chinese.
- Avoid repetitive subjects such as “这篇研究” and “作者发现”. Prefer “本研究”, “结果表明”, “这一结果提示”, or omit the subject.
- Translate most English terms into Chinese. Keep abbreviations only when useful, and define them on first use, for example “地上生物量碳（AGC）”.
- Avoid English headings such as “Highlights” unless the user requests English.
- Avoid promotional wording, exaggerated claims, casual jokes, and news-copy phrasing.
- Conclusions should be detailed and scholarly: state what the result means, under what assumptions, and what limitations remain.
- Clean AI-generated Chinese typography before delivery. Remove unnecessary spaces between Chinese characters and numbers, units, punctuation, or parentheses when standard Chinese layout does not require them.
- Keep spaces only where they improve readability for Latin abbreviations, formulas, English names, DOI/URL strings, or mixed technical expressions.
- Use standard Chinese punctuation in Chinese prose, such as ，。；：？（）. Use English punctuation only when the surrounding phrase is mainly English, a DOI/URL, a formula, or a code-like expression.

## Red Lines

Never:

- invent missing metadata, datasets, sample sizes, values, equations, or figure meanings;
- convert correlation, association, or model comparison into unsupported causation;
- present model outputs as experimental facts unless the paper does so;
- overgeneralize regional, cohort-specific, or simulation-specific findings;
- remove uncertainty because it weakens the story;
- reuse long original figure legends verbatim;
- place internal audit tables or process notes in the final article;
- create presentation or slide-deck deliverables under this skill.

## Word and WeChat Formatting

When creating a Word document:

- use black body text unless the user requests a color style;
- use SimSun/宋体 for Chinese text and Times New Roman for Latin text when practical;
- keep font size consistent within the same hierarchy: all same-level headings should match, and all body paragraphs should match;
- avoid blue-heavy styling;
- avoid wide tables that exceed page margins;
- convert oversized tables into bullets or short paragraphs;
- use paragraph spacing suitable for copying into the WeChat editor;
- keep figures large enough to inspect but within page margins;
- include only publishable content in the final document.

If a Word rendering or page preview workflow is available, inspect the rendered pages and fix overflowing tables, cropped images, unclear figures, or awkward line breaks before delivery.

## Final QA Checklist

Before delivery, verify:

- title, journal, DOI, and publication date are correct or explicitly marked unavailable;
- target audience and approximate length are appropriate for the user’s request;
- terminology is consistent across the article;
- abstract translation is faithful and concise;
- methods explain data and computational logic concretely;
- major claims map to paper locations;
- key numbers match the paper and include correct units;
- internal numeric audit has checked key numbers against paper figures/tables/text;
- results are interpreted, not only listed;
- conclusions are academic and appropriately qualified;
- English terms are not overused;
- the WeChat title is attractive but rigorous and not exaggerated;
- Chinese typography is cleaned;
- figures are cleanly cropped with axes and legends visible;
- every selected figure has a concise Chinese explanation of its meaning;
- every inserted figure is referenced in the text, and every mentioned figure is inserted or intentionally omitted;
- Word fonts use SimSun/宋体 and Times New Roman where practical;
- same-level headings and body paragraphs have consistent font sizes;
- Word layout has no overflowing tables or images;
- final Word is separated from working notes, numeric audit tables, terminology lists, figure notes, and QA notes;
- final output contains no internal notes or process text.
