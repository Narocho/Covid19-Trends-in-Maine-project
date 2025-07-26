# Covid19-Trends-in-Maine-project
Analyzed county-level COVID-19 data in Maine to study vaccine uptake, hospitalization severity, and risk trends. Used cohort analysis and computed severity indexes to uncover regional disparities and public health gaps.

🧭 Project Purpose
To convert raw COVID-19 health data into actionable public health insights by transforming variables, analyzing trends, identifying high-risk county cohorts, and simulating where interventions like boosters could reduce hospital burden.

🔄 Pipeline Overview
Raw Data → Feature Engineering (Why?) → Descriptive Statistics → Data Analysis (Where it starts) → Cohort Analysis (Where grouping happens) → Statistical Reasoning → Intervention Simulation → Actionable Insights

1. 📂 Raw Data
The dataset is a snapshot of county-level public health metrics in Maine during the COVID-19 pandemic. It includes:

Demographics: county, Census (population)

Clinical outcomes: cases, deaths, hospitalizations

Vaccination status: First, Final, Additional, Doses administered

At this point, data is raw, non-normalized, and hard to interpret without transformation.

2. 🔧 Feature Engineering – Transforming Raw into Insightful
Why feature engineering?
We needed ratios and rates to normalize values by population size or other context — this lets us make fair comparisons across counties.

🛠️ Metrics Created:
Feature	Formula	Purpose
Vaccination Rate	Final / Census	Proportion of fully vaccinated residents
Boosters per Person	Additional / Final	Booster adherence within vaccinated population
Hospitalization Rate	Hospitalizations / Cases	Clinical burden relative to cases
Relative Severity	Deaths / Hospitalizations	Proxy for treatment effectiveness or late detection
J&J Prevalence	Final - First	Estimate of one-shot vaccinations
Bivalent Odds	(Final - J&J) / J&J	Proxy for updated vaccine access

Each new feature makes the dataset more analytically rich, unlocking patterns hidden in the raw counts.

3. 📊 Descriptive Statistics & Visual Exploration
Purpose: Understand distributions, detect outliers, spot early patterns.

Example Explorations:
Bar Charts: Vaccination rate and hospital rate by county

Scatter Plots: Boosters vs severity; vaccine coverage vs deaths

These plots revealed:

Some counties had very low booster rates and high severity

Other counties were outperforming with low hospitalization despite high case counts

This stage reveals correlations, disparities, and flags areas for deeper analysis.

4. 🔎 Data Analysis – Where true reasoning begins
This is where the project transitions from what happened to why it's happening.

We examined:

Relationships between metrics (e.g., does more booster coverage = lower severity?)

Cross-comparisons of counties using derived indicators

Multivariate insight: counties with high J&J and high death rate might signal access or trust issues

Analytical Moves:
Combined multiple engineered features to derive risk scores

Compared counties using multi-feature filters, not single metrics

Created dictionaries for all new features for quick comparison

5. 🧬 Cohort Analysis – Where grouping happens
Counties were grouped based on:

Vaccination rate (low, medium, high)

Booster uptake (low, high)

Hospitalization and severity

Example:

High-risk cohort: low vaccination + high hospitalization + high severity

Low-risk cohort: high boosters + low death/hospital ratio

Why this matters:

Grouping counties allows us to generalize patterns and think in terms of public health clusters, not isolated events.

6. 📐 Statistical Reasoning
Even this, feature engineering sets the stage for:

T-tests / ANOVA: comparing hospitalization means across groups

Correlation matrices: to validate trends seen visually

Regression modeling (next step): predict severity based on vaccine metrics

This level of reasoning gives analysis credibility and potential for scaling.

7. 

If we increased booster rates in high-risk counties, how would severity drop?

We:

Identified counties with low booster & high death/hospital ratios

Compared their metrics to outperforming counties


8. 🧭 Actionable Insights
.  project culminates in data-backed health strategy guidance. 

Counties with low bivalent odds + high J&J could benefit from updated vaccine campaigns

High-risk counties with low booster-per-vax ratios should be prioritized for outreach

Severity patterns suggest booster coverage plays a role in survival — policy should focus on not just full vaccination but full series completion

🧰 Tools & Skills Demonstrated
Python (Pandas, Matplotlib): cleaning, processing, visualizing

Feature Engineering: extracting meaning from raw data

Exploratory Data Analysis (EDA): visual reasoning

Cohort Analysis: public health segmentation

Health Analytics Thinking: applied insight for real-world problems
