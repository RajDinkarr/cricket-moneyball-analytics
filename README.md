# Multi-Format Cricket Moneyball Analytics Engine

An end-to-end data engineering and analytics pipeline that processes over 79,000 rows of ball-by-ball cricket data across T20, ODI, and Test matches to identify elite player performance metrics.

## 🛠️ Tech Stack & Architecture
* **Python (Pandas, PyYAML, NumPy):** For ETL pipeline execution, parsing nested file structures, and automated feature engineering.
* **PostgreSQL:** For relational data warehousing, strict schema type design, and advanced analytical grouping.
* **Power BI:** For building an executive-ready interactive visualization layer (Upcoming).

## 🚀 Key Engineering Challenges Solved
1. **Nested Key Extraction Bug:** Debugged a structural dictionary mismatch in raw Cricsheet data to accurately map hidden nested run arrays (`'batsman'` data structure mapping).
2. **Database Schema Design & Scale Overflow:** Resolved a numeric field overflow error (`NUMERIC(3,1)` upgraded to `NUMERIC(4,1)`) to gracefully handle long-form Test match records exceeding 100+ overs.
3. **Data Volume Integration:** Successfully consolidated and cleaned 79,393 unique match delivery records across completely distinct match formats into a single unified database layer.

## 📈 Analytical Insights Discovered
* **T20 Power-Hitters (Aggression Engine):** Dynamically calculated scoring velocity, identifying elite strike-rates (e.g., RG Sharma leading at a 194.59 strike rate).
* **ODI Anchors (Consistency Engine):** Modeled strike rotation capabilities by analyzing low dot-ball percentages (e.g., JE Root maintaining an elite 36.22% dot-ball frequency).
* **Test Resilience (Survival Engine):** Built a custom `CASE WHEN` dismissal tracker to isolate true defensive endurance (e.g., SD Hope averaging 175.7 balls per individual dismissal).
