# Electronics Store Sales Analysis (12-Month Historical Data)

A comprehensive **Exploratory Data Analysis (EDA)** project utilizing **Python, Pandas, and Matplotlib** to analyze 12 months worth of electronics store sales data. The dataset contains hundreds of thousands of purchase records, broken down by order details, product types, pricing, and shipping addresses.

---

## Project Overview

The core objective of this project is to dive deep into historical sales data to extract actionable business insights, uncover purchasing patterns, and answer critical financial and operational questions to help improve future sales strategies.

The analysis is structured around answering key business questions, such as:
- What was the best month for sales? How much was earned that month?
- What city sold the most product?
- What time should we display advertisements to maximize customer likelihood of buying products?
- What products are most often sold together?
- What product sold the most, and why do you think it sold the most?

---

## Objectives

* **Data Aggregation:** Consolidate multiple monthly sales files into a single, unified dataset for annual analysis.
* **Data Wrangling & Cleaning:** Standardize data types, handle missing/corrupted values, and engineer new structural features (e.g., extracting Month, City, and Hour components).
* **Descriptive Analytics:** Extract high-level business metrics and KPIs to profile overall store performance.
* **Data Visualization:** Build clean, intuitive charts using Matplotlib to communicate historical trends to business stakeholders.

---

## Technology Stack

* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib

---

## Project Workflow

### 1. Background Information
* Project scoping and outlining the variables within the dataset.

### 2. Data Wrangling & Cleaning
To prepare the dataset for rigorous analysis, several critical data engineering steps were performed:
* Dropping rows containing missing or `NaN` values.
* Filtering out repetitive text headers introduced during file concatenation.
* **Type Conversion:** Converting `Quantity Ordered` from string to integer, `Price Each` from string to float, and `Order Date` into a standardized Datetime object.
* **Feature Engineering:** Creating dedicated columns for `Month`, `Sales` (Quantity $\times$ Price), `City` (parsed from the address), and `Hour` (extracted from the timestamp).

### 3. Exploratory Data Analysis (EDA)
* Aggregating financial metrics across time, geography, and product categories.
* Visualizing purchasing velocity and distribution trends.

### 4. Conclusions & Limitations
* Summarizing findings and exporting the fully cleaned dataset (`2019_clr_data.csv`) for secondary BI dashboarding or modeling applications.

---

## Dataset Variables Schema

| Feature | Data Type | Description |
| :--- | :--- | :--- |
| **Order ID** | `Integer` | Unique identifier for each transaction. |
| **Product** | `String` | The specific electronics item purchased. |
| **Quantity Ordered** | `Integer` | The number of units bought per product. |
| **Price Each** | `Float` | The unit price of the product in USD. |
| **Order Date** | `Datetime` | The exact timestamp of the transaction. |
| **Purchase Address** | `String` | The street, city, state, and zip code for shipment. |
| **Sales** *(Engineered)* | `Float` | Total monetary output calculated per record (`Quantity Ordered` $\times$ `Price Each`). |

---

## Project Limitations

1. **Temporal Constraint:** The dataset is strictly isolated to the year 2019, preventing year-over-year (YoY) trend comparisons.
2. **Analytical Scope:** The analysis focuses purely on descriptive statistics; it does not incorporate forecasting methodologies or predictive modeling due to the nature of the available features.

---

## How to Run

1. Clone the repository and install the required dependencies:
   ```bash
   pip install pandas numpy matplotlib

2. Place the raw 12-month CSV files in the same directory.
3. Execute the notebook sequentially to clean the data and generate the statistical plots.

Author

**Seif Fathi** Data Analyst & Python Developer specializing in Business Intelligence.

**Connect with me**

[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:seif.fathi22@gmail.com)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/201112158797)
