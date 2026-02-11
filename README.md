# Feature A Impact Analysis – Spain

Final Comprehensive Submission

Notebook:
`Feature_A_Impact_Analysis_COMPLETE_FINAL Anup Bhade.ipynb`

---

## Overview

This notebook evaluates the impact of Feature A, launched in Spain in July 2022, on core business health metrics.

Because the feature was released without a controlled experiment, the analysis applies structured observational methods with multiple validation layers. The goal is to assess whether Feature A improves user quality and progression toward core banking behavior.

---

## Business Question

Did Feature A improve engagement and long-term banking behavior in Spain?

Primary metrics analyzed:

* MAU – Monthly Active Users
* PAU – Primary Account Users
* PAU+ – Engineered high-value user metric

---

## Analytical Approach

The notebook follows a layered framework:

### 1. Data Preparation

* Filter dataset to Spain (country_code = ES)
* Convert date fields
* Create post-launch indicator (post_feature_A)
* Build post-launch comparison dataset

### 2. Market-Level Comparison (Before vs After)

Compares MAU and PAU before and after July 2022 to detect overall engagement shifts in Spain.

### 3. Feature Adoption Comparison

Post-launch comparison between:

* Feature A adopters
* Non-adopters

This identifies behavioral differences associated with adoption.

---

## Visualizations Included

### Engagement Divergence Chart

Bar chart comparing MAU and PAU between Feature A users and non-users.
Highlights differences in activity and core usage concentration.

### Retention Proxy Chart

MAU rate comparison to evaluate engagement consistency.

### Funnel Velocity View

Shows progression from:

* Activation (MAU)
* To primary usage (PAU)

This measures acceleration toward core banking behavior.

---

## Causal Validation

### Difference-in-Differences Assumption Check

Pre-launch MAU trends plotted for:

* Future Feature A adopters
* Never-users

This supports the parallel-trend assumption required for DiD-style reasoning.

### Propensity Score Estimation

Logistic regression models adoption likelihood using:

* feature_B
* feature_C
* MAU
* PAU

Validation includes:

* Density plot for common support
* Standardized Mean Difference (SMD) diagnostics for covariate balance

---

## Metric Engineering

### Engagement Depth Index

Defined as:

feature_A + feature_B + feature_C

This measures breadth of product usage and its relationship with PAU.

### PAU+ Construction

Defined as:

* PAU == 1
* Engagement depth ≥ 2

This identifies high-value, deeply engaged users.

---

## Feature Complementarity

An interaction variable (B_and_C) tests whether features B and C reinforce each other.

Results suggest complementary effects on core usage.

---

## Average Ticket Computation

If transaction data is available, the notebook computes mean transaction value per user per month to measure monetary engagement intensity.

---

## Key Findings

* Feature A does not materially increase overall MAU volume.
* Feature A users exhibit significantly higher PAU rates.
* Engagement depth strongly predicts core banking behavior.
* PAU+ concentration is higher among adopters.
* Complementarity between features supports cross-feature strategy.
* Validation checks (parallel trends and propensity diagnostics) support robustness.

---

## Limitations

* Observational study (no randomized control group)
* Possible residual confounding
* Requires controlled experimentation for full causal confirmation

---

## Tools Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn

---

## Strategic Implication

Feature A appears to improve user quality and depth of engagement, even if total activity volume remains stable.

Recommended next steps:

* Increase adoption through onboarding improvements
* Explore feature bundling strategies
* Implement controlled rollout frameworks for future releases

## Tools
Python, Pandas, Scikit-learn, Matplotlib

Step 1: Create Repo (same as above)

Create an empty repo (README optional).

Step 2: Clone Repo Locally
git clone https://github.com/AnupBhade/feature-a-impact-analysis.git
cd feature-a-impact-analysis

Step 3: Add Your Files
Put these inside the folder:
feature_A_analysis.ipynb
README.md


Step 4: Commit & Push
git add .
git commit -m "Add Feature A impact analysis notebook"
git push origin main
