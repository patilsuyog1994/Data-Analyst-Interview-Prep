# 🇬🇧 UK Data Analyst Interview Prep

A free, personalised interview question bank built for UK-based data analyst roles. Filter by experience level, core skills, and industry sector to generate 100 targeted questions — then track your practice progress.

**[▶ Live Demo](https://YOUR-USERNAME.github.io/data-analyst-interview-prep/)**

---

## What It Does

You set three filters, hit **Generate**, and the tool scores and ranks 100 questions tailored to your profile:

- **Experience level** — drag a slider from 1 to 5 years; questions are weighted by suitability for that level
- **Core skills** — pick from SQL, Python, Excel, Power BI, Tableau, R, Statistics, Machine Learning, Data Engineering, Storytelling, A/B Testing, Forecasting
- **Industry sector** — pick from Retail & Ecommerce, Finance & Banking, Healthcare & NHS, Tech & SaaS, Marketing & Media, Logistics & Supply Chain, Consulting, Energy & Utilities

Results are structured into four categories with balanced proportions:

| Category | Questions | What It Covers |
|---|---|---|
| Skill-Based Technical | 35 | SQL, Python, Excel, BI tools, statistics, ML |
| Case Study & Scenario | 30 | Root cause analysis, A/B testing, forecasting, stakeholder scenarios |
| Behavioural & Competency | 25 | STAR-method questions, communication, conflict, ambiguity |
| Industry & Role-Specific | 10 | UK GDPR, ICO, career progression, sector trends |

---

## Features

- **Smart scoring** — each question carries skill, industry, and experience-level metadata; the algorithm ranks all 100 by relevance to your selection
- **Difficulty badges** — every question is tagged Foundational → Senior+ so you can pace your practice
- **Search** — filter results by keyword across questions and assessment hints
- **Progress tracker** — mark questions as done; a progress bar shows how far through you are
- **Fully offline** — single HTML file, zero dependencies, works in any browser without internet

---

## UK-Specific Content

This tool is built with the UK job market in mind:

- Questions reference **UK GDPR**, the **ICO**, and post-Brexit data regulations
- Industry scenarios are grounded in UK sectors (NHS, UK retail, UK financial services)
- Behavioural questions reflect competency frameworks commonly used by UK employers
- Industry questions include UK data landscape awareness and career progression expectations

---

## Getting Started

### Option 1 — Use it directly

Download [`index.html`](./index.html), open it in any browser. No installation needed.

### Option 2 — Run it from this repo via GitHub Pages

The live version is deployed at:
```
https://YOUR-USERNAME.github.io/data-analyst-interview-prep/
```

---

## How to Deploy Your Own Copy

1. **Fork or clone** this repository
2. Make sure the file is named `index.html` at the root
3. Go to **Settings → Pages**
4. Set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`
5. Click **Save** — your site will be live within ~60 seconds at:
   ```
   https://YOUR-USERNAME.github.io/REPO-NAME/
   ```

---

## Question Bank Structure

All 100 questions live as a JavaScript array inside `index.html`. Each question object has the following shape:

```js
{
  id: 1,
  cat: 'tech',           // tech | case | beh | ind
  q: 'Question text...',
  h: 'What the interviewer is assessing...',
  skills: ['SQL', 'Python'],
  industries: ['Finance & Banking', 'all'],
  minYr: 2,              // minimum years experience
  maxYr: 5,              // maximum years experience
  diff: 3                // difficulty 1 (foundational) to 5 (senior+)
}
```

To add or edit questions, open `index.html` in any text editor, find the `ALL_QS` array, and follow the same structure.

---

## Category Breakdown

### Skill-Based Technical (Q1–35)
Covers SQL joins, window functions, query optimisation, Python pandas, data cleaning, statistics, hypothesis testing, Power BI/Tableau, data warehouse design, machine learning fundamentals, Git, and pipeline automation. Difficulty escalates from foundational joins through to senior-level system design.

### Case Study & Scenario-Based (Q36–65)
Realistic business briefs requiring step-by-step analytical reasoning: diagnosing revenue drops, building churn models, interpreting A/B tests, forecasting, attribution modelling, anomaly investigation, CLV analysis, and ROI framing. Each requires the candidate to walk through their process.

### Behavioural & Competency (Q66–90)
STAR-method questions covering: communicating complex findings, handling stakeholder disagreements, managing competing priorities, delivering unwelcome news, building relationships, automating processes, and presenting to senior leadership.

### Industry & Role-Specific (Q91–100)
UK-focused questions on GDPR compliance, ICO awareness, post-Brexit data regulations, AI's impact on analyst roles, career progression, sector trend awareness, and motivation for the role.

---

## Customising for Your Organisation

If you are using this tool for team training or recruitment preparation, you can:

- **Add company-specific questions** by appending entries to the `ALL_QS` array
- **Add new skill tags** by including new strings in the `skills` array and adding a matching pill in the HTML `skill-pills` section
- **Add new industries** in the same way via the `ind-pills` section
- **Adjust difficulty weights** by modifying the `diff` field on individual questions

---

## Tech Stack

| Layer | Detail |
|---|---|
| Framework | Vanilla HTML/CSS/JavaScript — zero dependencies |
| Fonts | Syne (headings) + DM Sans (body) via Google Fonts |
| Deployment | GitHub Pages (static) |
| Data | Inline JS array — no backend, no database |



## Disclaimer

This tool is designed for interview preparation and educational purposes. The questions reflect common patterns in UK data analyst interviews based on industry knowledge up to 2025. They are not exhaustive and actual interview questions will vary by company, team, and role level.
