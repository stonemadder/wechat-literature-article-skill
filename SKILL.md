---
name: wechat-literature-article
description: Use when drafting, revising, or packaging a Chinese WeChat public-account article from an academic paper PDF, especially Nature/Science-style literature summaries. Emphasizes accurate paper metadata, concise abstract translation, detailed data and method logic, main result interpretation, academic Chinese style, publication-ready Word formatting, clean figure cropping, and optional journal-club PPT preparation.
metadata:
  short-description: Chinese WeChat literature article workflow
---

# WeChat Literature Article

Use this skill when the user wants to turn an academic paper into a Chinese 微信公众号文献推文, revise an existing draft for publication quality, or prepare a related journal-club PPT.

## Working Principles

- Write for research-aware Chinese readers: academic, clear, and suitable for WeChat publishing.
- Focus on the paper's question, data, methods, results, mechanisms, implications, and limitations.
- Do not profile researchers, institutions, or lab stories unless the user asks.
- Preserve scientific accuracy over narrative smoothness. Verify uncertain bibliographic facts from the paper or reliable source material.
- Keep the final article publishable: remove process notes, internal comments, unnecessary English source text, and draft-only explanations.

## Source Intake

When a PDF or paper source is available, first extract or confirm:

- title, journal, volume/pages or online publication status, publication date, DOI
- abstract and stated contribution
- study region, study period, objects or samples
- datasets, instruments, model inputs, variables, and resolution
- method workflow, equations or computational logic where available
- main figures, extended figures, supplementary figures, tables, and captions
- key numeric results with units and uncertainty
- limitations, validation data, and sensitivity or uncertainty analysis

If bibliographic metadata are ambiguous, prioritize the paper front page, DOI page, publisher page, or official PDF. Do not invent missing metadata.

## Audience and Length

Before drafting, choose or infer the target depth. If the user does not specify, use the standard research-reader version.

- 简短版：about 1500-2500 Chinese characters, for quick WeChat reading.
- 标准版：about 2500-3500 Chinese characters, for research-aware readers and most public-account posts.
- 专业版：about 3500-5000 Chinese characters, for specialist readers or method-heavy papers.

Keep the article proportional: method-heavy papers may need more space in “数据与方法”, while discovery or mechanism papers may need more space in “主要结果” and “讨论”. Do not pad the article just to meet a length target.

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

Create an internal terminology list before drafting when the paper contains repeated technical terms, variables, datasets, model names, or abbreviations. Use it to keep translations consistent throughout the article.

The terminology list should track:

- English source term
- preferred Chinese translation
- abbreviation, if any
- first-use explanation
- terms that must not be mixed

For example, do not alternate between “地上碳”, “地上生物量碳”, and “地上碳储量” unless the paper distinguishes those concepts. Use the most accurate term consistently.

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

## Methods Section

The methods section must be concrete enough for readers to understand what was done. Avoid vague phrases such as “using remote-sensing analysis” without explaining inputs and calculations.

Prefer this order:

1. 数据输入：dataset names, time range, spatial/temporal resolution, variables
2. 研究对象与分类：sample selection, study objects, categories, masks, exclusions
3. 扰动或处理识别：event definition, thresholds, classification rules, grouping
4. 模型或计算方法：statistical model, physical model, equations, fitting logic, parameter estimation
5. 结果计算：how core metrics, changes, losses, gains, risks, or effects were derived
6. 不确定性与验证：validation data, sensitivity analysis, uncertainty propagation, comparison with independent observations

For method-heavy papers, use small subheadings and short explanatory paragraphs instead of a wide table that may overflow in Word or WeChat.

## Results Section

Each result subsection should contain:

- a clear result claim
- exact key numbers with units and uncertainty
- interpretation of what the numbers mean
- figure support only when it directly helps explain the result

Do not merely list numbers. Explain how the numbers support the paper’s argument. When applicable, distinguish gross change, net change, baseline, denominator, sample size, and uncertainty.

Maintain an internal numeric audit table while drafting. It does not need to appear in the final article unless the user asks. Track:

- key number
- unit
- uncertainty or confidence interval
- source figure/table/paragraph
- how it is used in the article
- whether it has been cross-checked

## Figures

Figures support the explanation; they should not determine the article structure.

Prioritize:

- core main figures that carry the main results
- one important methodological extended or supplementary figure when it clarifies the workflow
- one additional supporting figure only if it helps explain the overall conclusion

Before inserting a figure:

- crop to include axes, legends, color bars, panel letters, and key labels
- avoid including surrounding body text from the PDF
- do not cut off axis titles, tick labels, legends, or color scales
- check figure clarity after insertion into Word or PPT
- write short Chinese captions explaining what the figure supports

Do not translate long original figure legends verbatim.

Every selected figure must have a short explanatory note in Chinese. The note should be concise but self-contained: readers should understand what the figure shows, which panels or axes matter, and how it supports the adjacent result.

Run a figure-text correspondence check before delivery:

- every inserted figure must be referenced and explained in the nearby text
- every figure mentioned in the text should be inserted, unless there is a clear reason not to
- no “orphan figures” should remain
- figure order should follow the article logic, not necessarily the paper’s original figure order

## Word and WeChat Formatting

When creating a Word document:

- use black body text unless the user requests a color style
- use SimSun/宋体 for Chinese text and Times New Roman for Latin text when practical
- keep font size consistent within the same hierarchy: all same-level headings should match, and all body paragraphs should match
- avoid blue-heavy styling
- avoid wide tables that exceed page margins
- convert oversized tables into bullets or short paragraphs
- use paragraph spacing suitable for copying into the WeChat editor
- keep figures large enough to inspect but within page margins
- include only publishable content in the final document

If a Word rendering or page preview workflow is available, inspect the rendered pages and fix overflowing tables, cropped images, unclear figures, or awkward line breaks before delivery.

Separate publishable output from working materials:

- the final Word document should contain only the publishable article
- internal terminology lists, numeric audit tables, figure-cropping notes, and QA notes should stay in a separate working file or scratch area
- do not paste internal checklists into the public article unless the user explicitly requests them

## Final QA Checklist

Before delivery, verify:

- title, journal, DOI, and publication date are correct
- target audience and approximate length are appropriate for the user’s request
- terminology is consistent across the article
- abstract translation is faithful and concise
- methods explain data and computational logic concretely
- key numbers match the paper and include correct units
- internal numeric audit has checked key numbers against paper figures/tables/text
- results are interpreted, not only listed
- conclusions are academic and appropriately qualified
- English terms are not overused
- the WeChat title is attractive but rigorous and not exaggerated
- Chinese typography is cleaned: no unnecessary spaces between Chinese text and numbers, units, punctuation, or parentheses
- figures are cleanly cropped with axes and legends visible
- every selected figure has a concise Chinese explanation of its meaning
- every inserted figure is referenced in the text, and every mentioned figure is inserted or intentionally omitted
- Word fonts use SimSun/宋体 and Times New Roman where practical
- same-level headings and body paragraphs have consistent font sizes
- Word layout has no overflowing tables or images
- final Word is separated from working notes, numeric audit tables, terminology lists, and QA notes
- final output contains no internal notes or process text

## Optional Journal-Club PPT

If the user asks for a journal-club PPT:

- follow the user’s requested language
- structure slides as paper metadata, research problem, data and methods, main results, mechanism, critique/limitations, and discussion questions
- use one clear claim per slide
- include main figures and key extended figures as evidence objects
- make methods slides concrete: data, model, calculation logic, and validation
- render-check the contact sheet and key slides for text overflow, image rendering, and figure cropping
