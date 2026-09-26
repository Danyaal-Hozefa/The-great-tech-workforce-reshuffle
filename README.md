# THE GREAT TECH WORKFORCE RESHUFFLE

### An Intelligence Platform for Layoffs, AI Hiring, Skills & Workforce Transformation in India

> **Core Theme:** India's Technology Workforce Transformation  
> **Historical Analysis:** 2022–2026  
> **Scenario Horizon:** 2026–2030  
> **Tool:** Microsoft Power BI  
> **Data Model:** Star Schema

---

## 📌 Project Overview

**The Great Tech Workforce Reshuffle** is a Power BI business intelligence project designed to investigate how India's technology workforce is changing.

Instead of simply asking **"Who got laid off?"**, the project examines the broader workforce transformation taking place across India's technology sector:

- Are technology companies expanding or reducing their workforce?
- How do hiring patterns compare with workforce reductions?
- How is AI-related hiring changing?
- Which skills are experiencing increasing demand?
- How are companies responding through AI training, reskilling and redeployment?
- How does workforce change appear alongside business and financial indicators?
- What could different AI adoption and workforce adaptation assumptions imply for 2026–2030?

The project combines historical workforce analysis with a scenario-planning layer to create a decision-support view of India's technology workforce transformation.

---

## 🎯 Business Problem

India's technology workforce is undergoing significant changes involving layoffs, hiring, AI adoption, skill requirements, reskilling and redeployment.

Looking at layoffs alone provides only one side of the story.

This project therefore brings multiple workforce signals together to answer a broader question:

> **Is India's technology workforce shrinking — or being reshaped?**

The dashboard is designed to help an analyst explore workforce scale, hiring demand, workforce reductions, AI activity, skill shifts and possible future scenarios in one analytical environment.

---

## 🔍 Key Questions

The project addresses six major analytical questions:

1. **What is happening to India's technology workforce overall?**
2. **Which companies are expanding, reducing or transforming their workforce?**
3. **How are AI and changing skill requirements reshaping workforce demand?**
4. **How are reskilling and redeployment activities evolving?**
5. **How does workforce change appear alongside revenue and AI investment indicators?**
6. **How might different AI growth and workforce adaptation assumptions shape the future workforce through 2030?**

---

# 📊 Dashboard Structure

The Power BI solution contains four analytical pages.

---

## 1️⃣ Executive Workforce Intelligence

### Business Question
**What is happening to India's technology workforce overall?**

This page provides the executive-level view of workforce transformation across 2022–2026.

### Key KPIs

- Total Current Employees
- Total Layoffs
- Total New Hires
- AI Hiring %
- Total AI Investment
- Total Reskilled

### Visual Analysis

**Technology Workforce Trend**  
Tracks workforce levels over time and highlights changes in the overall workforce trajectory.

**Hiring vs Layoffs Trend**  
Compares hiring activity with workforce reductions to show how expansion and contraction occur alongside each other.

**Fresher Workforce Trend**  
Shows how fresher-related workforce activity changes over the historical period.

**AI Investment & Hiring Demand**  
Examines the relationship between AI investment activity and AI-related hiring demand.

**Workforce Change vs Revenue Growth**  
Provides a company-level comparison between workforce change and revenue-growth indicators.

### Story

**Workforce Scale → Hiring & Reductions → Fresher Workforce → AI Activity → Business Context**

---

# 2️⃣ Company Analysis

### Business Question
**Who is reshaping India's technology workforce?**

This page moves from the overall market to company-level analysis.

### Key KPIs

- Companies Analyzed
- Total Current Employees
- Total Layoffs
- Total New Hires
- Hiring-to-Layoff Ratio

### Visual Analysis

**Company Workforce Profile**  
Provides a company-level benchmark using current workforce, workforce change, layoffs, new hires and hiring-to-layoff ratio.

**Largest Workforce Reductions**  
Highlights companies with the largest recorded workforce-reduction activity in the dataset.

**Largest Technology Workforces**  
Shows the companies with the largest current workforce observations.

**Hiring vs Workforce Reductions**  
Uses a company-level scatter analysis to compare hiring activity with workforce reductions while using workforce scale as additional context.

### Story

**Scale → Workforce Reduction → Hiring Strategy → Company Benchmark**

---

# 3️⃣ Skills & AI Transformation

### Business Question
**How are AI and changing skill requirements reshaping India's technology workforce?**

This page focuses on the changing composition of workforce demand and the organizational response to AI.

### Key KPIs

- AI Roles
- AI Hiring %
- AI Trained
- Reskilled
- Redeployed

### Visual Analysis

**AI Hiring Trend**  
Tracks AI-related hiring demand across 2022–2026.

**Skill Demand & Growth**  
Compares skill-demand observations with demand-growth indicators to identify skills showing different combinations of scale and growth.

**Reskilling vs Redeployment**  
Compares workforce adaptation activity across years.

**AI Project Activity Across Companies**  
Compares recorded AI project activity across companies.

### Story

**AI Demand → Skill Shift → Workforce Response → Company AI Activity**

---

# 4️⃣ Scenario Planner

### Business Question
**How might AI growth, productivity effects, reskilling and redeployment influence India's technology workforce through 2030?**

Unlike the first three pages, this page is designed for **scenario analysis rather than historical reporting**.

### Scenario Types

- Low AI Adoption
- Base AI Adoption
- High AI Adoption

### Scenario Horizon

**2026 → 2030**

### Key Controls

**Select Scenario**  
Allows the user to switch between the defined AI-adoption scenarios.

**AI Growth Assumption**  
A What-If parameter allows the user to adjust the AI growth assumption within the modeled range.

### Key KPIs

- Base AI Jobs
- Projected AI Jobs
- AI Job Growth %
- Scenario Workforce Impact

### Visual Analysis

**AI Jobs Scenario Trajectory**  
Shows how projected AI jobs develop across the scenario horizon.

**AI Jobs by Scenario**  
Compares projected AI jobs across the modeled scenarios.

**AI Growth vs Workforce Adaptation**  
Explores the relationship between AI growth assumptions and reskilling assumptions.

**Scenario Assumptions**  
Displays the assumptions underlying each scenario.

### Story

**Assumption → Scenario → Workforce Impact → Decision Context**

> Scenario outputs are modeled projections based on explicit assumptions. They are not forecasts of actual future employment.

---

# 🏗️ Data Architecture

The project uses a **star-schema-oriented Power BI model** containing fact tables and dimension tables.

## Fact Tables

1. `Fact_Layoffs`
2. `Fact_Hiring`
3. `Fact_Skills`
4. `Fact_Workforce`
5. `Fact_Financials`
6. `Fact_AI_Transformation`
7. `Fact_Labour_Market`
8. `Fact_Company_Events`
9. `Fact_Workforce_Scenarios`

## Dimension Tables

1. `Dim_Date`
2. `Dim_Company`
3. `Dim_Geography`
4. `Dim_Role`
5. `DimSkill`
6. `Dim_Source`

The model uses dimension-to-fact relationships with single-direction filtering.

Fact-to-fact relationships are intentionally avoided in the main analytical model.

---

# 📦 Dataset Scale

The final analytical dataset contains:

| Table | Rows |
|---|---:|
| Fact_Layoffs | 750 |
| Fact_Hiring | 720 |
| Fact_Skills | 900 |
| Fact_Workforce | 1,800 |
| Fact_Financials | 1,800 |
| Fact_AI_Transformation | 600 |
| Fact_Labour_Market | 300 |
| Fact_Workforce_Scenarios | 300 |
| Fact_Company_Events | 750 |
| Dim_Company | 30 |
| Dim_Skill | 30 |
| Dim_Date | 60 |
| Dim_Geography | 25 |
| Dim_Role | 30 |
| Dim_Source | 5 |

---

# 🧮 Power BI & DAX

The project includes approximately **35 core DAX measures** covering:

- Basic aggregations
- `CALCULATE`
- Conditional filtering
- Ratios and percentages
- Time intelligence
- Year-over-year analysis
- YTD analysis
- Company ranking
- `RANKX`
- `FILTER`
- `SWITCH`
- Conditional business logic
- AI-related workforce metrics
- Scenario calculations

Examples include:

```DAX
Total Layoffs
Total New Hires
AI Hiring %
Fresher Hiring %
Hiring-to-Layoff Ratio
Layoff Rate
Reskilled %
Layoffs - YoY %
Hiring - YoY %
Company Layoff Rank
Company Hiring Rank
Company AI Investment Rank
AI Layoffs Share
Projected AI Jobs
AI Job Growth %
Scenario Workforce Impact
```

---

# 🎛️ Interactivity

The dashboard includes interactive Power BI features such as:

- Year slicers
- Company slicers
- Region slicers
- Scenario selection
- What-If parameter
- Cross-filtering
- Cross-highlighting
- Tooltips
- Drill-through
- Page navigation
- Interactive comparisons

Changing slicers dynamically updates the relevant KPIs and visuals according to the relationships and filter context in the Power BI model.

---

# 🔮 Scenario Modeling

The scenario planner uses three modeled scenarios:

| Scenario | AI Growth Assumption | Productivity Impact | Reskilling Rate | Redeployment Rate |
|---|---:|---:|---:|---:|
| Low AI Adoption | 15% | 5% | 20% | 15% |
| Base AI Adoption | 32% | 10% | 35% | 30% |
| High AI Adoption | 50% | 18% | 55% | 45% |

The scenario layer is intended to demonstrate **what-if analysis and decision modeling in Power BI**.

It should not be interpreted as an externally validated economic or employment forecast.

---

# 💡 Key Analytical Themes

The project is built around five major themes:

### 1. Workforce Shock
Layoffs and restructuring activity provide visibility into workforce reductions.

### 2. Market Response
Hiring activity shows where workforce demand continues despite reductions elsewhere.

### 3. Skill Shift
Skill-demand indicators show how workforce requirements can change over time.

### 4. AI Transformation
AI hiring, AI investment, AI training, reskilling and redeployment provide indicators of organizational adaptation.

### 5. Future Scenarios
Scenario modeling demonstrates how different AI growth and workforce adaptation assumptions can produce different modeled outcomes.

---

# ⚠️ Data & Interpretation Notes

### Synthetic Analytical Dataset

The dataset is **synthetic and calibrated for BI/analytical demonstration**.

It is not a database of verified public-company employment statistics.

Company names, workforce values, hiring activity, layoffs, AI activity and other observations should therefore be treated as **modeled analytical data**, not as audited corporate disclosures.

### No Causal AI Claim

The dashboard does **not** establish that AI directly caused a particular layoff or workforce change.

AI-related indicators are analyzed as workforce-transformation signals and should not automatically be interpreted as causal relationships.

### Workforce Activity

Measures such as:

- AI Trained
- Reskilled
- Redeployed
- Freshers
- New Hires

can represent activity across repeated observations.

They should not automatically be interpreted as unique individuals unless the underlying grain supports that interpretation.

### Scenario Outputs

Scenario results are assumption-driven model outputs rather than predictions of actual future employment.

---

# 🛠️ Tools Used

- **Microsoft Power BI**
- **Power Query**
- **DAX**
- **Microsoft Excel**
- **Data Modeling**
- **Star Schema**
- **Time-Series Analysis**
- **Scenario / What-If Analysis**
- **Data Visualization**

---

# 📁 Repository Structure

```text
the-great-tech-workforce-reshuffle/
│
├── README.md
│
├── PowerBI/
│   └── The_Great_Tech_Workforce_Reshuffle_India_Final.pbix
│
├── Data/
│   └── Great_Tech_Workforce_Reshuffle_India_Analytics_Dataset_FINAL.xlsx
│
├── Documentation/
│   ├── Project_Proposal.docx
│   ├── Project_Report.docx
│   └── Validation_Report.txt
│
├── Screenshots/
│   ├── Page_1_Executive_Workforce_Intelligence.png
│   ├── Page_2_Company_Analysis.png
│   ├── Page_3_Skills_AI_Transformation.png
│   └── Page_4_Scenario_Planner.png
│
└── DAX/
    └── DAX_Measures.md
```

---

# 🚀 How to Explore the Project

### 1. Clone or download the repository

Download the repository from GitHub.

### 2. Open the Power BI file

Open the `.pbix` file using Microsoft Power BI Desktop.

### 3. Review the data model

Open **Model view** to inspect the star-schema relationships.

### 4. Explore the four dashboard pages

Start with:

**Executive Workforce Intelligence → Company Analysis → Skills & AI Transformation → Scenario Planner**

### 5. Interact with the dashboard

Use the slicers, drill-through functionality and scenario controls to explore different perspectives.

---

# 📈 Portfolio Value

This project demonstrates practical BI capabilities including:

- Business problem definition
- Data modeling
- Star-schema design
- Power Query transformation
- DAX development
- Time intelligence
- KPI design
- Interactive dashboard development
- Company benchmarking
- Workforce analytics
- AI/skills analytics
- Scenario modeling
- Executive storytelling
- Data interpretation
- Analytical limitations and governance

The objective is to demonstrate how Power BI can be used as a **decision-support platform**, rather than simply as a visualization tool.

---

# 👤 Author

**Shebaaz Khan**

Business Analytics / BI Analyst Aspirant  
Mumbai, India

### Areas of Interest

- Business Intelligence
- Data Analytics
- Power BI
- SQL
- Python
- Data Visualization
- Business Analysis
- AI & Workforce Analytics

---

## ⭐ Project Takeaway

> **The Great Tech Workforce Reshuffle moves beyond a simple layoffs dashboard to examine workforce transformation as a multi-dimensional business problem — combining workforce scale, hiring, layoffs, skills, AI activity, reskilling, redeployment, financial indicators and scenario modeling.**

---

**Built with Microsoft Power BI | India Technology Workforce Transformation | 2022–2030**
