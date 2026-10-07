# Global AI Adoption in Education

A Tableau project analysing how artificial intelligence is being adopted in education across 10 countries from 2015 to 2026, built for educators, policymakers and EdTech stakeholders.

## Problem Statement
Despite rapid growth in AI use by students, teachers and institutions, there is limited clarity on how AI adoption varies across countries and regions, and whether factors such as internet access, education quality and government policy influence it. This project explores those patterns using interactive Tableau dashboards and a data story.

## Dataset
- Source: Global AI Adoption in Education dataset
- 1,360 records, 16 fields, monthly data (2015–2026)
- 10 countries across 6 regions
- Key fields: Schools AI Adoption %, Student AI Usage %, Teacher AI Usage %, Avg Daily AI Usage (min), Internet Penetration %, Education Index, Urban/Rural AI Usage %, Top AI Tool
- Note: 441 of 1,360 records have no value in the Government AI Policy field

## Tools Used
- Tableau Public (data visualisation, dashboard and story)
- Flask (web integration)
- GitHub (project hosting and documentation)

## Visualizations Created (9)
1. KPI Cards — global averages for student, teacher and school adoption, daily usage, internet penetration and education index
2. Geospatial Map — Schools AI Adoption by country
3. Bar Chart — Country-Level Daily AI Usage
4. Grouped Bar Chart — Student vs Teacher AI Usage Comparison by country
5. Trend Line Chart — AI Adoption Journey (2015–2026) by region
6. Bar Chart — Comparison of Leading AI Tools by daily usage
7. Grouped Bar Chart — AI Usage in Rural vs Urban Communities by region
8. Scatter Plot — Education Index vs Student AI Usage
9. Categorical Bar Chart — AI Adoption Level Breakdown (Low / Moderate / High)

## Dashboard and Story
All key charts are combined into one interactive dashboard with KPI cards and filters (Country, Region, Year). An 8-point Tableau Story presents the introduction, geographic adoption, 2015–2026 trend, AI-tool usage, urban–rural equity, student–teacher engagement, an additional education-index insight, and the conclusions/recommendations.

## Key Insights
- School AI adoption rose from about 3% in 2015 to about 59% in 2026 in every region
- North America and Australia lead on the adoption map
- A higher Education Index does not mean higher student AI usage — usage stays near 30%
- Urban usage is higher than rural everywhere, but regional differences are small
- No single AI tool dominates: ChatGPT, Google Gemini, Khanmigo and Microsoft Copilot are used almost equally
- No country-month has reached the High adoption category (66%+) yet: 769 records are Low, 591 Moderate, 0 High

## Performance Testing
- Data rendered: 1,360 rows and 16 columns (~0.35 MB), rendering remains smooth with multiple filters applied
- Filters used: Country (10), Region (6), Year (2015–2026)
- Calculated fields: 1 — Adoption Category (Low 0–33%, Moderate 33–66%, High 66–100%)
- Visualizations: 9 worksheets, 1 dashboard, 1 story

## Web Integration
The Tableau Public dashboard is embedded in a Flask web application.
Run it with:
1. Install Flask: pip install flask
2. Run: python app.py
3. Open http://127.0.0.1:5000 in a browser

## Live Demo
Tableau Public: https://public.tableau.com/app/profile/dip.lankeshwar/viz/GlobalAIAdoptioninEducation_17912879117140/GlobalAIAdoptioninEducation

