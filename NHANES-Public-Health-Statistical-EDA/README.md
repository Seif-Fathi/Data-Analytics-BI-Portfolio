# Public Health & Demographics Analysis: Statistical Inference on NHANES Data

A rigorous **Statistical Data Analysis & Inference** project using the National Health and Nutrition Examination Survey (**NHANES**) dataset (2015-2016). This project demonstrates the application of data cleaning, exploratory data visualization, estimation statistics, and parametric/non-parametric hypothesis testing to uncover demographic and physiological insights.

---

##  Project Overview

In public health, drawing conclusions from raw survey sample data requires mathematical validation to ensure observed patterns represent true population characteristics rather than random sampling noise. 

This project explores the NHANES registry to evaluate behavioral and physical attributes across demographics. The study transitions from descriptive analytics into inferential testing to answer critical health-related questions with high mathematical confidence.

The analysis answers key structural questions:
- What are the underlying distributions of baseline health metrics (Age, Weight, Height, BMI)?
- How does Systolic Blood Pressure morph dynamically across different age cohorts and genders?
- What is the statistical confidence level regarding the true proportion gap between male and female smokers?
- Is there a statistically significant difference in smoking rates among young adults (ages 20-25) based on gender?
- Are specific physical metrics skewed, and how can mathematical transformations stabilize them for downstream predictive modeling?

---

## Objectives

* **Demographic Mapping:** Profile demographic markers including Education Level, Marital Status, Gender, and Age structures.
* **Biometric Visualization:** Implement conditional visual plotting (grouped boxplots and stratified distribution shapes) to evaluate complex relationships like blood pressure variances.
* **Estimation Statistics:** Compute exact **95% Confidence Intervals (CI)** for population proportion and population mean differences.
* **Inferential Hypothesis Testing:** Formulate and execute **Two-Sample Z-Tests for Proportions** and **Independent T-Tests** to mathematically accept or reject operational null hypotheses.
* **Feature Engineering & Transformation:** Detect feature skewness using numerical calculation and mitigate it using logarithmic transformations.

---

## Technology Stack

* **Language:** Python
* **Data Wrangling:** Pandas, NumPy
* **Statistical Computation:** SciPy (Stats & Distributions module)
* **Data Visualization:** Matplotlib, Seaborn

---

## Project Workflow

### 1. Introduction & Feature Isolation
* Extracting a target sub-matrix from the macro NHANES dataset to focus strictly on physiological, behavioral, and demographic features of interest.

### 2. Rigorous Data Cleaning
* Re-coding encoded categorical identifiers (e.g., numeric codes for Education and Marital Status) into human-readable, explicit string labels.
* Handling missing entries systematically: Categorical missing vectors are isolated into a distinct `"Missing"` flag, while missing values in quantitative metrics are imputed based on stratified gender means to eliminate data bias.

### 3. Graphical Summaries & Stratified Profiling
* Generating multi-panel histograms to compute central tendency shapes (Uniform vs. Normal vs. Right-Skewed distribution shapes).
* Building stratified side-by-side boxplots to analyze complex interactions between **Systolic Blood Pressure, Gender, and Custom Age Cohorts**.

### 4. Inferential Estimation (95% Confidence Intervals)
* **Proportion Difference:** Quantifying the absolute gap between the percentage of male vs. female smokers in the population.
* **Mean Difference:** Constructing intervals around the true average BMI variation between male and female subpopulations.

### 5. Advanced Hypothesis Testing
* Conducting statistical inference under explicit mathematical frameworks ($H_0$ vs. $H_a$).
* Evaluating smoking prevalence variances specifically in young adults (Ages 20-25) via a **Two-Sample Test of Proportions**.
* Performing distributional stability checks using skewness scoring and executing **Log-Transformations** to condition metrics (Weight, BMI, Blood Pressure) for Gaussian stability.

---

## Dataset Variables Schema

| Feature | Original Code | Target Data Type | Description |
| :--- | :--- | :--- | :--- |
| **Smoking Status** | `SMQ020` | `String` | Categorical indication of smoking history (`Yes`, `No`). |
| **Marital Status** | `DMDMARTL` | `String` | Target customer demographic structure (`Married`, `Divorced`, `Separated`, etc.). |
| **Gender** | `RIAGENDR` | `String` | Assigned biological sex (`Male`, `Female`). |
| **Age** | `RIDAGEYR` | `Integer` | Continuous age profile of the participant in years. |
| **Education Level** | `DMDEDUC2` | `String` | Highest education milestone achieved. |
| **Weight** | `BMXWT` | `Float` | Continuous body mass indicator measured in kilograms (kg). |
| **Height** | `BMXHT` | `Float` | Continuous physical height indicator measured in centimeters (cm). |
| **BMI** | `BMXBMI` | `Float` | Calculated Body Mass Index continuous metric. |
| **Systolic Blood Pressure** | `BPXSY1` | `Float` | Initial automated systolic reading in mmHg. |

---

## Key Statistical Insights Verified

* **The Demographic Blood Pressure Inversion:** Visual profiling confirms that while younger men maintain higher average systolic blood pressure than younger women, this gap narrows dramatically past age 50 and completely reverses post age 70, highlighting critical healthcare demographic tracking considerations.
* **Smoking Gender Variance:** Inferential testing on young adults (Ages 20-25) isolates a statistically significant 10 percentage-point increase in smoking prevalence among males over females ($p \approx 0.01$), allowing us to strongly reject the null hypothesis of conversion independence.
* **Pricing & Transformation Stability:** Identifying right-skewed profiles in weight metrics led to successful stabilization via log transformation, providing a clean pathway for future predictive regression algorithms.

---

## Methodological Context (Complex Surveys Note)
> **Note on Sampling Logic:** NHANES utilizes a cluster-based complex survey design rather than a pure Independent and Identically Distributed (I.I.D.) sample. For the pedagogical and exploratory boundaries of this notebook, data vectors are analyzed assuming standard randomized representative properties.

---

## ⚙️ How to Run
1. Install core dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scipy
2. Place the required NHANES.csv dataset inside your local workspace root directory.
3. Execute the notebook cells sequentially to reproduce the confidence intervals and statistical tests.

Author

**Seif Fathi** Data Analyst & Python Developer specializing in Business Intelligence.

### Connect with me
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:seif.fathi22@gmail.com)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/201112158797)
