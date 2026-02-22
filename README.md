# Wellness Insights & Activity Metrics

An end-to-end data analytics project analyzing fitness tracker data from 33 individuals to uncover behavioral trends and inform smarter health marketing strategies.

**Tools:** Python · SQL Server · Tableau  
**[View Live Dashboard →](https://public.tableau.com/app/profile/adnan.khan.pathan6792/viz/FitnessInfoDashboard/Dashboard2)**

---

## Project Overview

A smart device company collects granular health data — steps, calories, sleep, heart rate, intensity, and weight — from its users. The goal of this project was to analyze that data to identify patterns in consumer behavior and surface growth opportunities for targeted marketing strategies.

**Key Questions Explored:**
- When are users most active during the day and week?
- What is the relationship between activity intensity, steps, and calories burned?
- How does sleep quality correlate with daily activity levels?
- Which user segments are most engaged, and how can the product team reach disengaged users?

---

## Dataset

- **Source:** Fitness tracker bands from 33 unique individuals
- **Datasets Used:** 10 files across daily and hourly granularities

| Dataset Group | Files | Approach |
|---|---|---|
| Daily Info | 4 files | Merged into single DataFrame |
| Hourly Info | 3 files (Steps, Calories, Intensities) | Merged into single DataFrame |
| Supplementary | Heart Rate, Sleep Info, Weight Info | Analyzed separately |

> Note: Daily and Hourly datasets share common ID and Date columns, enabling clean merges. Other datasets have differing row counts and are stored as separate normalized tables.

---

## Process

### 1. Exploratory Data Analysis & Cleaning (Python)
- Loaded and inspected all 10 datasets for nulls, duplicates, and inconsistencies
- Merged Daily and Hourly files into unified DataFrames using common keys
- Standardized datetime formats and handled missing heart rate and weight entries
- Prepared clean exports for SQL Server ingestion

**Notebooks:**
- `Exploring the Data.ipynb` — Initial EDA and data profiling
- `DACalories_M.ipynb`, `DASteps_M.ipynb`, `DAIntensities_M.ipynb` — Daily analysis
- `HCalories_M.ipynb`, `HSteps_M.ipynb`, `HIntensities_M.ipynb` — Hourly analysis
- `Heart Rate Info.ipynb`, `Sleep Info.ipynb`, `Weight Info.ipynb` — Supplementary datasets

### 2. Data Storage & Querying (SQL Server)
- Imported cleaned datasets into Microsoft SQL Server
- Created two consolidated tables via SQL joins for daily and hourly data
- Kept Heart Rate, Sleep, and Weight as separate normalized tables to preserve data integrity
- Wrote analytical queries to aggregate KPIs and segment users by activity level

### 3. Visualization (Tableau)
- Connected Tableau directly to SQL Server for a live data source
- Built an interactive dashboard with filters for activity type, time of day, and user segments
- Dashboard supports scheduled refresh for continuously collected data

---

## Key Insights

- **Peak activity windows** cluster in the early morning and early evening, suggesting optimal times for push notification campaigns
- **Sedentary users** make up a significant portion of the user base — targeted re-engagement alerts could meaningfully improve retention
- **Calorie burn correlates strongly with intensity minutes**, not just step count — a nuance that could inform how the app surfaces progress metrics to users
- **Sleep data** shows a subset of users consistently getting under 6 hours, presenting an opportunity for a sleep improvement feature or nudge

---

## Recommendations

Based on the analysis, the following product and marketing strategies were identified:

1. **Activity Alerts** — Trigger motivational notifications during identified low-activity windows to boost daily engagement
2. **Personalized Challenges** — Introduce step and intensity challenges segmented by user activity tier
3. **Sleep Nudges** — Flag users averaging under 6 hours of sleep and surface targeted wellness content
4. **Feedback Loop** — Implement in-app prompts after activity milestones to gather qualitative data alongside the quantitative metrics

---

## Project Structure

```
Wellness-Insights-and-Activity-Metrics/
│
├── Exploring the Data.ipynb          # EDA and data profiling
├── Getting the New Tables.ipynb      # SQL table creation logic
│
├── Daily Analysis/
│   ├── DACalories_M.ipynb
│   ├── DASteps_M.ipynb
│   └── DAIntensities_M.ipynb
│
├── Hourly Analysis/
│   ├── HCalories_M.ipynb
│   ├── HSteps_M.ipynb
│   └── HIntensities_M.ipynb
│
├── Supplementary/
│   ├── Heart Rate Info.ipynb
│   ├── Sleep Info.ipynb
│   └── Weight Info.ipynb
│
├── Clean Data.zip                    # Cleaned datasets
├── Data Used-...zip                  # Raw source data
├── EDA-...zip                        # EDA exports
└── SQL Queries-...zip                # SQL scripts
```

---

## Skills Demonstrated

- **Python** — Pandas, data cleaning, multi-file merging, EDA
- **SQL Server** — Schema design, joins, aggregation queries, normalized storage
- **Tableau** — Interactive dashboards, live SQL connection, parameter-driven filters
- **Business Analysis** — Translating data patterns into actionable recommendations

---

## Author

**Adnan Khan Pathan**  
[LinkedIn](https://www.linkedin.com/in/adnan-khan-pathan/)
[Gmail] (adnannkhan.pathan@gmail.com)
