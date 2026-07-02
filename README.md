# Students Social Media Addiction — Data Analysis & Prediction

Exploratory data analysis and machine learning project investigating the relationship between social media usage, sleep, mental health, and academic performance among students.
![Python](https://img.shields.io/badge/Made%20with-Python-3776AB?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Made%20with-Python-3776AB?logo=python&logoColor=orange)
##  Project Members
1. SONG SOLINE

2. YOEM MESA

3. VON NAROTH 

##  Overview

This project analyzes a dataset of student social media habits to uncover patterns between **daily usage time**, **addiction scores**, **sleep**, **mental health**, and **academic performance**. It combines statistical exploration, visualization, and a logistic regression model to predict whether social media use affects a student's academic performance.

##  Dataset

`Students Social Media Addiction.csv` — contains student-level records including:

- Demographics: `Age`, `Gender`, `Academic_Level`, `Country`, `Relationship_Status`
- Usage: `Avg_Daily_Usage_Hours`, `Most_Used_Platform`
- Wellbeing: `Sleep_Hours_Per_Night`, `Mental_Health_Score`, `Conflicts_Over_Social_Media`
- Target-related: `Addicted_Score`, `Affects_Academic_Performance`

##  Project Workflow

1. **Data Preprocessing & Statistics**
   - Data loading, structure overview, missing value & duplicate checks
   - Outlier / range validation
   - Categorical encoding (Gender, Academic Level, Platform)
   - Descriptive statistics (mean, median, std) and frequency tables

2. **Exploratory Data Analysis & Visualization**
   - Distribution plots for all numerical variables
   - Boxplots for outlier detection
   - Categorical feature distributions (bar & pie charts)
   - Cross-tabulations: platform vs academic impact, academic level vs addiction category, gender vs platform preference
   - Relationship analysis: usage vs addiction, sleep vs addiction, platform vs addiction, mental health vs usage, conflicts vs addiction

3. **Machine Learning — Logistic Regression**
   - Predicts `Affects_Academic_Performance` (binary) from `Addicted_Score`, `Avg_Daily_Usage_Hours`, `Sleep_Hours_Per_Night`, `Mental_Health_Score`
   - Train/test split (80/20, stratified)
   - Evaluation: accuracy, precision, recall, confusion matrix
   - Feature importance via odds ratios
   - 5-fold cross-validation

##  Key Results

- **Model performance:** ~97.9% accuracy, 0.968 precision, 1.000 recall
- **Usage & addiction:** Strong positive relationship — students using 5+ hours/day show high addiction scores (7+)
- **Sleep & addiction:** Strong negative relationship — under 6 hours of sleep correlates with high addiction scores
- **Platform risk:** TikTok and Instagram show the highest addiction association; LinkedIn the lowest
- **Mental health:** Usage negatively correlates with mental health scores
- **Conflicts:** More social-media-related conflicts strongly associate with higher addiction scores

##  Tech Stack

- Python 3
- `pandas`, `numpy` — data handling
- `matplotlib`, `seaborn` — visualization
- `scikit-learn` — modeling (Logistic Regression, train/test split, cross-validation, metrics)
- `scipy` — statistics

##  Getting Started

```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn
```

Place `Students Social Media Addiction.csv` in the project root, then open and run:

```bash
jupyter notebook IDS_Project_draft.ipynb
```

##  Limitations

- Self-reported data may introduce bias
- Cross-sectional design — no causal conclusions possible
- Limited to a student population
- Doesn't account for social media *content type*

##  Future Work

- Longitudinal tracking of addiction progression
- Testing intervention strategies
- Platform-specific deep-dive analysis
- Integration with real academic performance records
- Personalized intervention tools

## 💡 Recommendations

**For students:** limit usage to <3 hrs/day, prioritize 7+ hours of sleep, monitor conflicts, diversify platform use, track mental health.

**For institutions:** use ML-based screening to flag at-risk students, run digital wellness/sleep hygiene workshops, provide counseling support.

---
*Part of an Intro to Data Science (IDS) coursework project.*
