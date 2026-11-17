# Allison Kramer | MSBA Data Analytics Portfolio
M.S. Business Analytics, Boston University Questrom (Dec 2026)
**Python · SQL · Machine Learning · Tableau · BigQuery**

Projects from my MSBA program, with notebooks, slides, and short writeups. Notebooks open in Google Colab, so you can run them in your browser with no setup.

---

## 1) Predicting Hospital Length of Stay in New York
**Goal:** Predict how long each inpatient will stay, so hospitals can plan staffing, beds, and budgets proactively instead of reactively.
**Data:** NY SPARCS Hospital Inpatient Discharges, 2024 (~2 million records, 33 columns)
**Stack:** Python, pandas, scikit-learn, LightGBM, Google Colab
**Code:** [Colab notebook](https://colab.research.google.com/drive/1DyYronD1hpq8dn1YW5wC7vq2fmZ4Ty9q?usp=sharing)

**What we did:**
- Cleaned and prepped ~2M records: fixed data types, handled missing values, removed non-numeric values from the target
- Built and tuned 5 models (Linear/Ridge/Lasso, Decision Tree, Linear SVR, Random Forest, LightGBM) using RandomizedSearchCV
- Combined the best models into a stacked regressor

**Key finding:** The stacked model predicts LOS within ~2.9 days on average (MAE 2.88, R² 0.50). Clinical severity and risk of mortality are the strongest drivers, followed by discharge disposition, demographics, and payer type.

**Slides:** [View presentation](https://docs.google.com/presentation/d/1I9KEblP3TdJyZHDoBXCDBci4VwrHurZ9whGpQjZbK2I/edit?usp=sharing)

---

## 2) Uncovering Federal Grant Funding Patterns (2004–2023)
**Goal:** Use unsupervised ML to find natural groupings in how U.S. federal agencies structure funding, allocate resources, and support programs.
**Data:** U.S. Government Grant Opportunities, 2004–2023 (funding amounts, award counts, eligibility, grant descriptions)
**Stack:** Python, pandas, scikit-learn (K-Means, K-Modes, K-Prototypes), sentence transformers
**Code:** [BA820_Team11_MLProject](https://github.com/akramerr/BA820_Team11_MLProject)

**My part:** Built agency funding strategy profiles with K-Means clustering, finding 4 distinct agency archetypes based on funding scale, opportunity volume, and award distribution. Tested robustness across model choices and parameters to confirm the clusters held up.

**Key findings:**
- High-opportunity agencies dropped from 84% to 74% after 2018, a shift from broad distribution toward concentrated investment
- High-volume funders allow 9.04 eligibility types on average vs. 1.48 for concentrated funders
- High-funding agencies focus on defense and infrastructure; high-opportunity agencies prioritize health and education

---

## 3) Green Taxi Trends in NYC (2019–2023)
**Goal:** Understand how ridership, revenue, and rider behavior changed as green taxis are phased out, and how COVID reshaped demand across boroughs.
**Data:** NYC OpenData, 5 years of green taxi trip records plus monthly pickup/dropoff data
**Stack:** SQL (BigQuery), Tableau
**Code:** [NYC-Green-Taxi-Project](https://github.com/akramerr/NYC-Green-Taxi-Project)

**What we did:**
- Cleaned and merged 5 annual datasets into one table (dropped unused columns, removed duplicates, imputed missing values, UNION DISTINCT)
- Designed an ER diagram linking trip records to monthly pickup/dropoff data
- Answered exploratory SQL questions on demand, revenue, payment methods, and surcharges, then built Tableau dashboards

**Key finding:** Ridership declined sharply over time. Manhattan led in pickups, weekday afternoons and Thu/Fri had peak demand, and cashless payments rose significantly after COVID.

**Slides:** [View presentation](https://docs.google.com/presentation/d/1KS6YpFSch8oNY6BFXtMaFely0tK2B3DweXmhcqNjmVE/edit?usp=sharing)

---

## 4) Crime vs. Employment in Los Angeles (2010–2025)
**Goal:** Explore whether unemployment relates to crime patterns across LA.
**Stack:** Python, pandas, Matplotlib, Seaborn

**Key finding:** The correlation between unemployment and crime was weak and inconsistent. Location-based hotspots explained more of the pattern.

**Slides:** [View presentation](https://docs.google.com/presentation/d/1xasSNnrMwZormB-dJKUxsLB76GSGQEomLBr8xxOp8Fg/edit?usp=sharing)

---

## In Progress: Soccer Player Contribution Analysis (StatsBomb Event Data)
Using match event data to find undervalued players in less stat-visible positions, building toward ML models of which pass sequences lead to shots and goals. Code coming soon.

---

**Contact:** akramerr@bu.edu · [LinkedIn](https://www.linkedin.com/in/allison-kramer)
