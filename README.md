# player-peformance-analysis


# CRICKET ANALYTICS SYSTEM – ML PROJECT REPORT

## BATTERS & BOWLERS ANALYSIS

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat-square)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?style=flat-square)
![Pandas](https://img.shields.io/badge/Pandas-Data-darkgreen?style=flat-square)

---

## 1. PROJECT OVERVIEW
The **IPL Cricket Analytics System** is a machine learning platform designed to analyze, classify, and provide actionable insights for players in the Indian Premier League (IPL). Utilizing **K-Means Clustering** and **K-Nearest Neighbors (KNN)** with **Cosine Similarity**, the system moves beyond traditional statistics to evaluate true player impact.

### 1.1 Core Objectives
* **Phase-Based Analysis:** Evaluation across Powerplay (Overs 1–6), Middle (Overs 7–15), and Death (Overs 16–20) overs.
* **Match-up Intelligence:** Identification of batter vulnerabilities against specific bowler types.
* **Player Scouting:** KNN-driven recommendations to find statistically similar player replacements.
* **Venue Intelligence:** Stadium-based performance tracking.

### 1.2 Tech Stack
* **Language & ML:** Python 3.x, Scikit-Learn
* **Data Processing:** Pandas, NumPy
* **Visualization:** Plotly, Matplotlib, Seaborn

---

## 2. PROBLEM STATEMENT & SYSTEM ARCHITECTURE
Traditional metrics like batting averages or economy rates fail to capture situational performance. This project solves role ambiguity (e.g., identifying phase specialists), optimizes tactical match-ups, and aids scouting.

### System Layers
1. **Data Ingestion:** Processes raw IPL Ball-by-Ball datasets and Player Metadata.
2. **Preprocessing:** Handles missing values, filters low-sample records, and typesets variables.
3. **Machine Learning:** Executes K-Means Clustering and Cosine Similarity mapping.
4. **Analytics Layer:** Generates console reports and interactive dashboards.

---

## 3. DATA & FEATURE ENGINEERING

### 3.1 Data Quality Thresholds
To maintain analytical integrity, data is filtered using strict baselines:
* **Batters:** Must have faced a minimum of **50 balls** across at least **5 matches**.
* **Bowlers:** Must have bowled a minimum of **100 balls** across at least **5 matches**.

### 3.2 Engineered Features
* **Batting:** Strike Rate (SR), Average, Boundary %, Dot Ball %, and Phase-Specific SRs (Powerplay/Middle/Death).
* **Bowling:** Economy Rate (Econ), Average, Strike Rate, Dot %, and Phase-Specific Economies.
* **Contextual:** Venue Performance Profiles and League Baseline Averages.

---

## 4. MACHINE LEARNING MODELS

### 4.1 K-Means Clustering
Groups players automatically into tactical cohorts based on performance similarities.
* **Batter Clusters:** *Death Over Specialists, Powerplay Specialists, Middle Order Anchors, Elite Aggressive Batters, Versatile Batters.*
* **Bowler Clusters:** *Elite Strike Bowlers, Death Overs Specialists, Powerplay Enforcers, Economy Bowlers, Wicket-Taking Bowlers.*

### 4.2 KNN & Cosine Similarity
Calculates directional similarity percentages to find stylistic player matches rather than volume-based matches. 

### 4.3 Impact Score Formulas
* **Batter Impact Score:** Weighted by Strike Rate (35%), Average (25%), Boundary % (20%), and Death Overs Output (20%).
* **Bowler Impact Score:** Weighted by Economy (30%), Wickets (30%), Strike Rate (20%), Dot % (10%), and Death Overs Control (10%).

---

## 5. MODULE FUNCTIONALITIES & RESULTS

### 5.1 Batter Analytics Case Study: Virat Kohli
* **Metrics:** 237 Matches, 7263 Runs, 37.25 Avg, 130.98 SR.
* **Strengths & Role:** Core strength in the Middle Overs (7–15); classified as a **Middle Order Anchor**.
* **Top Stylistic Replacements:** KL Rahul, Rohit Sharma, Kane Williamson, Faf du Plessis, Shubman Gill.

### 5.2 Bowler Analytics Case Study: Jasprit Bumrah
* **Metrics:** 7.14 Economy, 22.46 Average, 18.9 Strike Rate, 145 Wickets.
* **Strengths & Role:** Dominant in Powerplay and Death; classified as an **Elite Death Bowler**.
* **Top Stylistic Replacements:** Kagiso Rabada, Trent Boult, Pat Cummins, Mohammed Shami, Anrich Nortje.

### 5.3 Key Project Findings
* **67% of batters** concentrate over 40% of their run volume into a single specific innings phase.
* Right-handed batters display the highest vulnerability index against left-arm pace bowling.
* Venue dimensions and pitches heavily skew historical success rates, validating the need for Venue Intelligence.

---

## 6. CONCLUSION & FUTURE WORK

### Contributions & Limitations
* **What it delivers:** Automated player indexing, data-driven replacement scouting, and match-up optimization dashboards.
* **Current Constraints:** Excludes debutants due to strict data thresholds; does not account for a player's recent temporal "form."

### Future Roadmap
* **Short-Term:** Integrate time-series analysis for recent form detection and deep learning embeddings.
* **Medium-Term:** Build real-time live auction valuation models and opposition strategy simulators.
* **Long-Term:** Implement cross-league transfer learning and integrate computer-vision ball-tracking data.

---

### FINAL CONCLUSION
The IPL Cricket Analytics System successfully bridges data science and cricket strategy, turning raw ball-by-ball entries into automated player classification, tactical recommendations, and optimized team-building insights.
