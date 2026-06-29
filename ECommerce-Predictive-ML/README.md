# Maximizing Sales ROI: Statistical Financial Analysis & Predictive Conversion Models

An end-to-end analytics project that integrates **MySQL, SQL, Python, Statistics, and Machine Learning** to analyze an e-commerce conversion funnel, evaluate marketing performance, and build a production-ready customer conversion prediction model.

---

## Project Overview

This project demonstrates a complete analytics workflow, from querying a relational database to generating business insights and training a predictive machine learning model.

The analysis focuses on answering key business questions such as:
- Which marketing channels generate the highest ROI?
- Where do users drop off in the conversion funnel?
- How do user behaviors vary over time?
- Are conversion differences statistically significant?
- Can we predict whether a user will purchase?

---

## Objectives

* Explore customer behavior throughout the purchase funnel.
* Analyze marketing channel performance.
* Measure financial Key Performance Indicators (KPIs).
* Perform statistical hypothesis testing to validate insights.
* Build a production-ready machine learning model for purchase prediction.
* Translate analytical findings into actionable business recommendations.

---

## Dataset

The project uses an event-level e-commerce dataset stored inside a **MySQL relational database**. Each record represents a customer event such as: `Page View`, `Add to Cart`, `Begin Checkout`, and `Purchase`.

### Available Features:
* **Identifiers & Timestamps:** User ID, Session ID, Event Date/Timestamp.
* **Behavioral Attributes:** Event Type, Traffic Source, Product Category.
* **Demographics & Devices:** Device Type, Country.
* **Financials:** Purchase Amount (Contains `NaN` for non-purchase events).

---

## Technology Stack

* **Database:** SQL (MySQL)
* **Data Manipulation:** Python (Pandas, NumPy, SQLAlchemy)
* **Data Visualization:** Matplotlib, Seaborn
* **Statistical Inference:** SciPy (Chi-Square Test, Confidence Intervals, Normality Testing)
* **Machine Learning:** Scikit-learn (Random Forest Classifier)

---

## Project Workflow & Structure

The notebook (`integrating-relational-database-with-predictive-ml.ipynb`) is systematically organized into four major phases:

### 1. Exploratory Data Analysis (EDA)
* **Database Initialization:** Connect MySQL with Python using SQLAlchemy, create relational schema, and validate data types.
* **Data Quality Checks:** Analyze missing values and handle `NaN` strategies to preserve financial metrics like AOV.

### 2. Financial & Marketing Analytics
* **Funnel Analytics:** Build a 30-day conversion funnel, calculate micro step-by-step conversion rates, and analyze funnel efficiency.
* **Marketing Performance:** Evaluate channels (`organic`, `paid_ads`, `social`, `email`) based on revenue generation and Average Order Value (AOV).
* **Time-Based Analytics:** Profile customer velocity and purchasing trends by hour of day and day of week.

### 3. Statistical Inference
* Run **Shapiro-Wilk normality tests** and KDE plots on transaction values.
* Deploy the non-parametric **Mann-Whitney U Test** to validate pricing variances between acquisition channels.
* Conduct a **Chi-Square ($\chi^2$) Test of Independence** to mathematically verify if conversion propensity is dependent on the traffic source.
* Compute **95% Confidence Intervals (CI)** using Student's t-distribution for financial risk forecasting.

### 4. Predictive Machine Learning
* **Feature Engineering:** Aggregate user-level clickstream telemetry and apply dummy encoding to categorical vectors.
* **Leakage Diagnostics:** Inspect baseline model behavior, detect architectural target leakage, and execute strategic data cleaning.
* **Model Deployment:** Train a robust, class-balanced **Random Forest Classifier** to isolate high-intent window shoppers for automated remarketing.

---

## Dataset Variables Schema

| Feature | Data Type | Description |
| :--- | :--- | :--- |
| **user_id** | `String` | Unique customer identifier. |
| **event_date** | `Timestamp`| Date and time of the interaction event. |
| **event_type** | `String` | Action taken by the user (`page_view`, `add_to_cart`, `checkout_start`, `purchase`). |
| **traffic_source** | `String` | Originating marketing channel (`organic`, `paid_ads`, `social`, `email`). |
| **amount** | `Float` | Transaction value in USD (Contains `NaN` for non-purchase events). |

---

## Skills Demonstrated

* Advanced SQL & Relational Database Architecture
* Pipeline Automation & Connection Strings
* Diagnostic & Inferential Statistical Modeling
* Advanced Feature Engineering & Target Leakage Removal
* Class-Balanced Machine Learning Classification
* Data-Driven Business Intelligence (BI)

---

## Running the Project

1. Install the required packages:
   ```bash
   pip install pandas numpy matplotlib seaborn sqlalchemy scipy scikit-learn mysql-connector-python
1.Set up your local MySQL database and execute the provided SQL schema.

2.Import the raw dataset into your database.

3.Update the database connection credentials (database_uri) in the environment setup cell.

4.Run the notebook sequentially.

Note: The SQL queries are written natively for MySQL. Running them directly in environments that use SQLite wrappers (such as default Kaggle local files) will produce syntax compatibility errors.

Author
Seif Fathi
Data Analyst & Python Developer specializing in Business Intelligence.

### Connect with me
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:seif.fathi22@gmail.com)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/201112158797)
