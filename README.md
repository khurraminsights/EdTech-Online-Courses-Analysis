<div align="center">

# EdTech Online Courses Analysis
### Power BI Portfolio Project | Course Catalog, Languages & Learner Engagement

<img width="2244" height="701" alt="EdTech Courses Analysis Banner" src="https://github.com/user-attachments/assets/8ca739b5-dbb5-4d86-950f-1b5bc6ab2051" />


![Power BI](https://img.shields.io/badge/Power_BI-Data_Visualization-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Analytics](https://img.shields.io/badge/Analytics-Course_Performance-722B8E?style=for-the-badge)
![Data](https://img.shields.io/badge/Insights-Education_Data-D94189?style=for-the-badge)

**An interactive Power BI report exploring course formats, teaching languages, average views, subtitles, duration, instructor ratings and skills across an online-course catalog.**

[Dashboard](#dashboard-preview) · [Questions](#business-questions) · [Findings](#findings-visible-in-the-report) · [Method](#power-bi-report--methodology) · [Limitations](#data-interpretation--quality-checks)

</div>

> **Independent project:** This is an educational data analytics portfolio project. Findings below describe the attached Power BI report and should not be interpreted as verified platform-wide performance. The banner is a design illustration; the dashboard screenshot is from the uploaded project PDF.

## Executive Summary

Online education platforms contain courses across many subjects, formats, teaching languages and skill levels. Understanding that catalog requires more than counting courses: analysts also need to compare potential learner interest, instructor ratings and engagement-related attributes.

I developed an **EdTech Online Courses Analysis** report in Power BI to explore these relationships through interactive category and sub-category filters, charts and summary tables. The report helps frame questions about **course supply, language availability, views, subtitle support, course length and skills coverage**.

| Project detail | Description |
|---|---|
| **Role** | Data Analyst — portfolio case study |
| **Primary tool** | Power BI Desktop |
| **Source artifacts** | `.pbix` report and PDF dashboard export |
| **Report pages inspected** | 1 |
| **Main dataset references** | `Online_Courses`, `Instructors` (visible in PBIX report metadata) |
| **Main interactive filters** | Category, Sub-Category |
| **Analysis areas** | Course type, language, average views, subtitles, duration, ratings, skills |

## Dashboard Preview

<img width="1448" height="1086" alt="EdTech Online Courses Dashboard" src="https://github.com/user-attachments/assets/9ef5d9de-c2ac-400d-ad68-da255d58b78e" />

*Actual screenshot rendered from the provided Power BI dashboard PDF. This is the evidence-backed reference for values and charts.*

## Business Questions

The report investigates these nine questions:

1. **Course formats:** Which formats (Course, Specialization, Project, Professional Certificate) are most common?
2. **Category performance:** How do views vary by category and sub-category?
3. **Skills:** How many skills are associated with different course categories?
4. **Language availability:** Which teaching languages are represented in the catalog?
5. **Subtitles:** How does average viewership vary with the number of subtitle languages?
6. **Instructors:** Which displayed instructors have the highest ratings?
7. **Duration:** How does course duration relate to the average number of views?
8. **Sub-category comparison:** How do subject areas differ in course attributes and engagement?
9. **Catalog positioning:** Which underrepresented formats or language segments might merit further research?

## Findings Visible in the Report

| Finding | What the dashboard shows | Interpretation / caveat |
|---|---|---|
| **Courses dominate the format mix** | **746** entries labeled `Course` versus **132** `Specialization` entries | These are catalog counts, not enrollment or revenue measures. |
| **English is the dominant teaching language** | Pie chart shows **845 (95.91%)** for the leading language and **23 (2.61%)** for the next displayed slice | The chart legend indicates English is dominant; remaining slices and denominators should be checked before claiming a complete language breakdown. |
| **Average views vary by language** | The table includes approximately **2,092** for Portuguese (Brazilian), **1,637** for Spanish and **102** for Chinese (Simplified) | These are report values for the selected context, not evidence that language alone causes engagement. |
| **Some highly rated instructors cluster near the ceiling** | Several displayed instructor ratings read **4.9** | A rating chart alone does not establish statistical significance or course quality. |
| **Subtitle-language count and views are plotted together** | The chart increases sharply at some higher subtitle counts, with a point labeled around **38K** | Outliers and sample sizes need review; this is not proof that adding subtitles causes more views. |
| **Duration and viewership vary nonlinearly** | The scatter/line display covers courses with durations up to roughly **800 hours** | Check long-course outliers and metric aggregation before making a duration recommendation. |
| **Skills coverage varies by sub-category** | Business table shows an average count of **3.76** skills provided in its total row | The table is filtered to Business in the displayed view; do not generalize this figure to every category. |

These observations come from the uploaded PDF. The dashboard screenshot contains some ambiguous labels and partially truncated category names, so conclusions should remain limited to what can be read and reproduced.

## Power BI Report & Methodology

The `.pbix` report metadata shows **one page with 12 visual containers**, including a category slicer, sub-category slicer, course-type bar chart, language/sub-category column chart, language pie chart, category ranking matrix, subtitle-count line chart, instructor-rating column chart, duration-versus-views line chart and skills/duration matrix.

### Analytical workflow

```text
Online course & instructor records
           |
    Power BI data model
           |
     Category filters
           |
  +--------+---------+---------+
  |        |         |         |
Formats Languages  Viewership  Instructors
  |        |         |         |
  +--------+---------+---------+
           |
   Interactive dashboard
           |
    Questions & insights
```

### Measures and aggregations

The report visual metadata references aggregations such as `COUNT` of course identifiers, `SUM` or averages of views, and instructor-rating measures. Before treating the results as production KPIs, the specific measure definitions and filter contexts should be documented in the `.pbix` file.

## Business Recommendations

| Opportunity | Recommended investigation | Success criterion |
|---|---|---|
| **Course portfolio mix** | Compare completion, enrollment and profitability across formats instead of counting supply alone | Enrollment and completion by course type |
| **Language localization** | Examine underserved language segments and course demand | Qualified demand and engagement by language |
| **Subtitle accessibility** | Test whether expanded subtitle support improves access after controlling for course popularity | Controlled engagement and completion measures |
| **Instructor experience** | Pair instructor ratings with review counts and course-level outcomes | Rating reliability and learner outcomes |
| **Course length** | Separate short and extended courses; investigate outliers | Completion and watch time by duration band |
| **Skills coverage** | Compare skills offered against measured learner demand | Skill relevance and enrollment conversion |

*These are proposed analyses, not measured improvements from the current report.*

## Data Interpretation & Quality Checks

The following checks would improve reproducibility before external publication:

- [ ] Confirm total number of course records and de-duplicate course IDs.
- [ ] Inspect the category slicer for the `(Blank)` value and determine its source.
- [ ] Verify whether reported `Number of viewers` represents unique viewers, total views or an imported numeric field.
- [ ] Validate chart titles: count, average and sum are different metrics.
- [ ] Inspect the unusually long-duration records and high subtitle-count outliers.
- [ ] Reconcile language counts with the pie chart's percentages and total denominator.
- [ ] Check instructor-rating sample sizes.
- [ ] Document the source dataset, refresh date and Power Query transformations.
- [ ] Add verified measure definitions and validated screenshots from Power BI Desktop.

## Visual Design

The supplied report uses a dark maroon and light-pink theme. A refreshed visual direction can use **navy, plum, rose and white** with clearer hierarchy, more room for category labels, fewer decorative elements and explicit metric units.

**Important:** AI-rendered mockups are *design concepts only*. They must not replace the original dashboard as quantitative evidence unless values and labels are rebuilt from the actual model.

## Repository Files

```text
EdTech-Online-Courses-Analysis/
├── README.md
├── assets/
│   ├── edtech-banner.png
│   └── original-dashboard.png
├── EdTech Online Courses Analysis.pbix   # add original file if desired
└── Power BI Project Dashboard.pdf        # add original export if desired
```

The last two entries are suggested filenames; keep the real filenames when uploading the source files. GitHub's normal preview cannot interact with `.pbix` reports, so include screenshots and clear reproduction notes.

## About the Analyst

**Khurram Naveed** — Data Analyst | Power BI | SQL Server | Excel

[![GitHub](https://img.shields.io/badge/GitHub-khurraminsights-181717?style=for-the-badge&logo=github)](https://github.com/khurraminsights)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/khurram-naveed-0083851aa/)

---

<div align="center"><strong>Better questions. Clearer analysis. More useful learning insights.</strong></div>

