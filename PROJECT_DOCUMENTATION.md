# Project Documentation — Global AI Adoption in Education

## 1. Project Overview
This project analyses how artificial intelligence is being adopted in education across 10 countries from 2015 to 2026. It is built for educators, policymakers and EdTech stakeholders who need a clear, visual view of adoption trends, usage patterns and access gaps. The findings are presented as an interactive Tableau dashboard and an 8-point Tableau Story.

## 2. Objective
To explore how AI adoption in schools, student AI usage and teacher AI usage vary by country and region over time, and whether factors such as internet penetration and education quality are associated with that adoption.

## 3. Dataset
- Source: Global AI Adoption in Education dataset (provided through the SkillWallet project workspace)
- 1,360 records, 16 fields, monthly data from January 2015 to December 2026
- 10 countries across 6 regions (Africa, Asia, Europe, North America, Oceania, South America)
- Key fields: Schools AI Adoption %, Student AI Usage %, Teacher AI Usage %, Avg Daily AI Usage (min), Internet Penetration %, Rural/Urban AI Usage %, Education Index, Top AI Tool
- Data quality note: 441 of the 1,360 records have no value in the Government AI Policy field, so policy analysis from that field is limited.

## 4. Data Preparation
1. Connected the CSV dataset to Tableau Public.
2. Verified field types: percentages and daily minutes as measures, Country/Region/Top AI Tool as dimensions, Year extracted from the date field.
3. Assigned the geographic role to Country so the choropleth map renders.
4. Checked sampled rows for blanks and consistency; the only systematic gap is the Government AI Policy field noted above.
5. Created one calculated field: Adoption Category, based on Schools AI Adoption % — Low (0–33%), Moderate (33–66%), High (66–100%).

## 5. Visualizations Created (9)
1. KPI Cards — global averages: Student 30.99%, Teacher 29.91%, Schools 29.41%, Daily usage 32.82 min, Internet 74.70%, Education Index 0.78
2. Geospatial Map — average Schools AI Adoption % by country
3. Trend Line — Schools AI Adoption by region, 2015–2026 (about 3% rising to about 59%)
4. Bar Chart — average Daily AI Usage by country (all countries within roughly 29–33 minutes/day)
5. Grouped Bar Chart — Student vs Teacher AI Usage by country (students slightly higher in almost every country)
6. Bar Chart — Leading AI Tools by average daily usage (ChatGPT, Google Gemini, Khanmigo, Microsoft Copilot almost equal)
7. Grouped Bar Chart — Rural vs Urban AI Usage by region (urban higher everywhere)
8. Scatter Plot — Education Index vs Student AI Usage (usage stays near 30% regardless of education index)
9. Categorical Bar Chart — Adoption Level Breakdown: Low 769 records, Moderate 591, High 0 (total 1,360)

## 6. Dashboard
All key charts are combined into one interactive Tableau dashboard with KPI cards and filters for Country, Region and Year, so a viewer can compare countries and regions dynamically.

## 7. Story
The Tableau Story has 8 points: (1) Introduction using the full dashboard, (2) Geographic disparity from the map, (3) Temporal trend 2015–2026, (4) Scatter insight on education index, (5) AI tool competition, (6) Urban–rural digital equity, (7) Student vs teacher engagement, (8) Conclusions and recommendations from the adoption-level breakdown.

## 8. Performance Testing
- Data rendered: 1,360 rows and 16 columns (~0.35 MB); rendering stays smooth with filters applied.
- Filters used: Country (10), Region (6), Year (2015–2026).
- Calculated fields: 1 — Adoption Category (Low 0–33%, Moderate 33–66%, High 66–100%).
- Visualizations: 9 worksheets, 1 dashboard, 1 story (8 points).

## 9. Web Integration
The Tableau Public dashboard is embedded in a Flask web application (app.py renders templates/index.html, which embeds the dashboard and links to the full Tableau Public workbook).
Run it with: pip install flask, then python app.py, then open http://127.0.0.1:5000 in a browser.

## 10. Key Insights
- School AI adoption rose from about 3% in 2015 to about 59% in 2026 in every region.
- North America and Australia lead on the adoption map.
- A higher Education Index does not mean higher student AI usage — usage stays near 30%.
- Urban usage is higher than rural everywhere, but regional differences are small.
- No single AI tool dominates daily usage.
- No country-month has reached the High adoption category (66%+) yet.

## 11. Limitations
- Only 10 countries are covered, so global conclusions are indicative, not exhaustive.
- Government AI Policy is missing in 441 records, limiting policy analysis.
- Adoption is measured as percentages; the data does not show learning-outcome quality directly.

## 12. Links
- Tableau Public workbook: https://public.tableau.com/app/profile/dip.lankeshwar/viz/GlobalAIAdoptioninEducation_17912879117140/GlobalAIAdoptioninEducation
- GitHub repository: https://github.com/diplankeshwar/global-ai-adoption-in-education
- Project demonstration video (Google Drive): TO BE ADDED AFTER RECORDING
