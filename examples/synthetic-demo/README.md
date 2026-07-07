# Synthetic Demo

This demo is intentionally fictional. It shows how the skill should reason from paper evidence to a Chinese WeChat article without using a copyrighted PDF or figure.

## Input Prompt

```text
Use $wechat-literature-article to write a Chinese WeChat public-account article from this paper PDF.

Audience: graduate students and research-group WeChat readers.
Length: standard research-reader version.
Requirements:
- include paper metadata at the beginning;
- explain datasets, methods, uncertainty, and validation;
- select the core result figure and one method figure;
- audit key numbers internally;
- output a Word-ready Chinese article.
```

## Fictional Paper Metadata

```text
Title: Fire Size Controls Postfire Surface Warming in Temperate Forests
Journal: Example Journal of Earth Systems
Publication date: 2026-06-15
DOI: 10.0000/example.2026.001
Study region: temperate forests in a fictional Northern Hemisphere dataset
Study period: 2001-2020
```

## Source Intake Example

The skill should first extract the evidence base:

| Evidence type | Fictional source detail | How it will be used |
| --- | --- | --- |
| Dataset | 500 m annual burned-area map, 2001-2020 | Define fire size and event boundaries |
| Temperature | 1 km land-surface temperature anomaly product | Estimate postfire warming |
| Vegetation | 30 m canopy-cover product resampled to 500 m | Control for prefire forest structure |
| Validation | 120 field plots from three regions | Check whether satellite-derived severity is plausible |
| Main figure | Figure 2: warming response by fire-size class | Support the main result |
| Method figure | Figure 1: event selection and matching workflow | Explain the analysis pipeline |

## Internal Numeric Audit Example

This table should stay internal unless the user asks for it.

| Claim candidate | Source | Unit | Check | Final use |
| --- | --- | --- | --- | --- |
| Large fires show stronger warming than small fires | Figure 2b | degrees C | Confirm class definitions and baseline | Main result paragraph |
| Mean warming persists for 5 years | Results paragraph | years | Confirm postfire window | Discussion |
| 120 field plots used for validation | Methods | plots | Confirm sample count | Methods section |
| Highest uncertainty occurs in sparse-canopy areas | Supplementary Fig. S3 | qualitative | Keep limitation | Discussion |

## Terminology Example

| English term | Preferred Chinese term | Note |
| --- | --- | --- |
| postfire surface warming | 火后地表增温 | Use consistently |
| fire-size class | 火烧面积等级 | Define when first used |
| land-surface temperature anomaly | 地表温度异常 | Keep distinct from air temperature |
| matched control pixels | 匹配对照像元 | Explain matching logic |

## Draft Excerpt Example

```text
标题：火烧面积越大，森林火后的地表增温越强吗？

文章名称：Fire Size Controls Postfire Surface Warming in Temperate Forests
期刊：Example Journal of Earth Systems
发表时间：2026-06-15
DOI：10.0000/example.2026.001

摘要
该研究利用2001-2020年火烧面积、地表温度异常和森林冠层覆盖度数据，评估不同火烧面积等级下森林火后地表增温的持续时间和强度。研究通过匹配未燃烧对照像元控制区域气候背景和植被结构差异，并结合样地数据验证卫星反演的火烧强度指标。结果表明，较大火烧斑块不仅产生更强的火后地表增温，其影响也更可能持续多年，但这种关系在低冠层覆盖区域具有更高不确定性。

数据与方法
研究首先基于500 m年度火烧面积产品识别2001-2020年的森林火烧事件，并按火烧斑块面积划分等级。随后，研究将每个火烧像元与气候背景、海拔和火前冠层覆盖相近的未燃烧像元进行匹配，以估算相对于对照区域的地表温度异常。为避免把空气温度变化误读为地表过程，文中所有增温结果均指地表温度异常，而非近地面气温。
```

## Figure Explanation Example

```text
图1展示了研究的事件筛选和匹配流程：研究先识别森林火烧斑块，再剔除火前冠层覆盖不足和云污染严重的像元，最后为每个火烧像元寻找具有相似背景条件的未燃烧对照像元。这个流程决定了后续增温估计是否能够尽量排除区域气候差异的影响。

图2比较了不同火烧面积等级下的火后地表温度异常。横轴为火后年份，纵轴为相对于匹配对照像元的地表温度异常。该图支持文章的核心结论：火烧面积越大，火后地表增温越强，且持续时间越长。
```

## Final QA Gate

Before publishing, check:

- metadata are not fictional in real use;
- every key number has source location, unit, and denominator;
- "地表温度" is not mixed with "气温";
- figure captions explain what the reader should learn;
- Word output contains publishable text only;
- internal audit and terminology tables are excluded from the public article.

This is the kind of evidence chain that should make the final article more trustworthy than a generic AI summary.
