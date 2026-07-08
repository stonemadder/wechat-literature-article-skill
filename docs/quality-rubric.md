# Quality Rubric

Use this rubric to judge whether an output from `wechat-literature-article` is ready for a Chinese WeChat public-account post.

Scoring suggestion:

- 3 = publication-ready
- 2 = usable with minor revision
- 1 = needs substantial revision
- 0 = missing or unreliable

## 1. Paper Metadata

Checklist:

- title is correct;
- journal, publication date, volume/pages or online article status are correct when available;
- DOI is correct;
- the article does not invent missing metadata.

Common failure modes:

- DOI copied with extra punctuation;
- publication date confused with online access date;
- journal name shortened inconsistently;
- article type or status overstated.

## 2. Scientific Faithfulness

Checklist:

- the central research question is represented accurately;
- the claimed contribution matches the paper;
- limitations and assumptions are kept;
- causal language is not stronger than the paper supports;
- conclusions are qualified when uncertainty remains.

Common failure modes:

- turning correlation into causation;
- omitting uncertainty because it weakens the story;
- exaggerating regional findings into global conclusions;
- replacing the paper's argument with a generic news-style summary.

## 3. Methods and Data Explanation

Checklist:

- datasets, samples, study period, and spatial or temporal resolution are stated where relevant;
- model inputs, variables, thresholds, and grouping rules are explained;
- calculations or equations are translated into readable Chinese prose;
- validation, sensitivity analysis, and uncertainty treatment are described;
- vague phrases such as "using remote sensing" are expanded into concrete steps.

Common failure modes:

- naming datasets without explaining what they measure;
- skipping denominators, masks, exclusions, or sample sizes;
- describing a model as a black box;
- hiding uncertainty treatment in a single sentence.

## 4. Numeric Audit

Checklist:

- key numbers match the paper's text, figures, tables, or supplementary materials;
- units are preserved;
- uncertainty, confidence intervals, and denominators are included when the paper reports them;
- gross change, net change, baseline, sample size, and percentage change are not mixed;
- rounded values do not change the interpretation.

Common failure modes:

- copying a number but dropping its denominator;
- mixing percentage points and percent change;
- translating units inconsistently;
- using figure-derived values as exact values without qualification.

## 5. Terminology and Chinese Style

Checklist:

- repeated technical terms use consistent Chinese translations;
- abbreviations are defined on first use;
- English terms are kept only when useful;
- Chinese punctuation and spacing are clean;
- the tone is academic and readable, not promotional.

Common failure modes:

- alternating between several Chinese translations for the same concept;
- leaving too many English phrases in otherwise Chinese prose;
- adding casual jokes or clickbait phrasing;
- creating unnatural spaces around Chinese punctuation, numbers, and units.

## 6. Figure Selection and Explanation

Checklist:

- selected figures support the article's argument;
- axes, legends, panel labels, and color bars are visible after cropping;
- each figure has a concise Chinese explanation;
- every inserted figure is referenced near the relevant text;
- every mentioned figure is inserted or intentionally omitted.

Common failure modes:

- using figures as decoration;
- cutting off legends or color bars;
- translating the original caption verbatim without explaining the result;
- leaving orphan figures that are not discussed.

## 7. Word and WeChat Readiness

Checklist:

- body text and headings use consistent font sizes;
- Chinese and Latin fonts are standardized when practical;
- tables and figures stay within page margins;
- the final Word document contains only publishable content;
- internal notes, audit tables, and process checklists are kept out of the public article.

Common failure modes:

- oversized tables that overflow the page;
- image labels too small to read;
- inconsistent heading styles;
- publishing internal notes by accident.

## 8. Source Completeness and Evidence Mapping

Checklist:

- major result claims map to paper text, a figure, a table, a supplement, or a DOI/publisher metadata page;
- missing methods, figures, uncertainty ranges, or metadata are explicitly tracked;
- partial-source drafts are labelled as limited when only an abstract, notes, or extracted text are available;
- unsupported statements are removed or softened;
- working notes remain separate from the final article.

Common failure modes:

- drafting a full article from an abstract while implying the full paper was checked;
- presenting unverified metadata as confirmed;
- using a figure number without checking what the panel actually shows;
- hiding missing source material from the user;
- leaving unresolved TODOs in the final article.

## 9. Scope Control

Checklist:

- the output is a WeChat literature article or article revision;
- the task is not converted into a presentation, slide deck, broad literature review, or unrelated writing assignment;
- presentation requests are routed to a presentation-focused workflow.

## Release Gate

Before publishing, all nine sections should score at least 2. For research-group or public-account release, sections 1, 2, 4, 6, and 8 should score 3.
