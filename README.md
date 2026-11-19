# ConnectaTel Customer Usage & Segmentation Analysis

**Author:** [Rodrigo Garza García](https://www.linkedin.com/in/rodrigogarzamx/)  
**Professional focus:** Public & International Affairs · Business Analysis · Data Analytics  
**Portfolio page:** [Professional Website — Projects](https://rogarzag.github.io/#projects)  
**GitHub repository:** [connectatel-customer-usage-analysis](https://github.com/rogarzag/connectatel-customer-usage-analysis)  
**Project focus:** Data Analytics · Data Quality · Exploratory Analysis · Feature Engineering · Customer Segmentation  
**Project context:** TripleTen Data Analyst Bootcamp; guided portfolio project  
**Data / case coverage:** Telecommunications customer, plan, and usage datasets; analysis period not specified in the README  
**Professional links:** [GitHub profile](https://github.com/rogarzag) · [LinkedIn](https://www.linkedin.com/in/rodrigogarzamx/) · [Professional Website](https://rogarzag.github.io/)

## Project Overview

Customer usage, segmentation, and statistical analysis for a telecommunications dataset using Python.

## Project Context

This is a **guided portfolio project** completed as part of the **TripleTen Data Analyst Bootcamp**.

TripleTen provided the case framework and datasets. The data cleaning, feature engineering, statistical analysis, visualizations, customer segmentation, and business interpretation were completed as part of my project work.

## Business Objective

Analyze ConnectaTel customer behavior to:

- identify and address data-quality issues,
- understand customer usage patterns,
- compare customer distributions across plan types,
- create customer-level usage metrics,
- identify unusual usage patterns,
- segment customers by age and usage level,
- translate analytical findings into business recommendations.

## Datasets

The analysis uses three datasets located in the `data/` directory:

- `plans.csv` — information about ConnectaTel plans.
- `users_latam.csv` — customer demographics, registration information, plan type, and churn data.
- `usage.csv` — customer interactions, including calls and text messages.

The datasets used in this guided project are included in the repository to support reproducibility.

## Tools & Methods

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Data cleaning
- Exploratory Data Analysis (EDA)
- Descriptive statistics
- Feature engineering
- IQR outlier analysis
- Customer segmentation
- Business-oriented interpretation

## Analysis Workflow

1. **Data Loading and Exploration**
   - Reviewed dataset dimensions, columns, data types, and missing values.

2. **Data Quality Assessment**
   - Identified missing values, sentinel values, suspicious records, and out-of-range dates.

3. **Data Cleaning**
   - Replaced invalid age and city values.
   - Corrected registration dates outside the expected analysis period.
   - Preserved structurally expected missing values when fields did not apply to a particular interaction type.

4. **Customer-Level Feature Engineering**
   - Aggregated interaction-level data by customer.
   - Created:
     - `msg_cnt` — total messages per customer.
     - `call_cnt` — total calls per customer.
     - `call_min` — total accumulated call minutes per customer.

5. **Exploratory Analysis**
   - Analyzed age, messages, calls, and accumulated call minutes by plan type.

6. **Outlier Analysis**
   - Used boxplots and the IQR method to identify extreme usage values.

7. **Customer Segmentation**
   - Segmented customers by:
     - usage level,
     - age group.

8. **Business Interpretation**
   - Translated analytical findings into customer retention, engagement, loyalty, and plan-growth recommendations.

## Key Findings

### Plan Distribution

- `Basico` represents approximately **64.9%** of customers.
- `Premium` represents approximately **35.1%**.
- Age, message, call, and accumulated call-minute distributions show broadly similar patterns across both plans.
- The higher absolute frequencies observed for `Basico` are consistent with its larger customer base.

### Usage Segments

- **Medium Usage:** 73.6%
- **Low Usage:** 19.5%
- **High Usage:** 7.0%

Most ConnectaTel customers therefore fall within the **Medium Usage** segment.

### Age Segments

- **Adult (30–59):** 50.5%
- **Older Adult (60+):** 30.6%
- **Young (<30):** 19.0%

Customers aged 30 or older represent the majority of the customer base.

### Usage Patterns

- Message activity is mainly concentrated around **4–6 messages per customer**.
- Call activity is mainly concentrated around **3–5 calls per customer**.
- 75% of customers accumulate approximately **31.2 call minutes or less**.
- Messages, calls, and accumulated call minutes show right-skewed distributions.

### Outliers

Upper-end outliers were identified in the main usage variables:

- `msg_cnt`: values of **12 or more**
- `call_cnt`: values of **11 or more**
- `call_min`: values above approximately **61.3 accumulated minutes**

The observed extreme values were considered plausible customer behavior and were retained in the analysis.

## Business Recommendations

- Prioritize retention and increased engagement among **Medium Usage** customers, who represent the largest segment.
- Capitalize on the large **Basico** customer base through retention initiatives, increased service usage, and selective migration to higher-value offers.
- Strengthen **Premium** adoption through differentiated benefits and promotions.
- Develop loyalty initiatives for **High Usage** customers.
- Increase engagement among **Low Usage** customers.
- Maintain a competitive value proposition for the **Adult** segment, which represents approximately half of the customer base.
- Strengthen the offer for **Young** customers to increase their participation within the customer base.

## Repository Structure

```text
connectatel-customer-usage-analysis/
│
├── data/
│   ├── plans.csv
│   ├── usage.csv
│   └── users_latam.csv
│
├── ConnectaTel_Customer_Usage_Segmentation_Analysis.ipynb
└── README.md
```

## Reproducibility

The analysis is contained in `ConnectaTel_Customer_Usage_Segmentation_Analysis.ipynb`.

The required datasets are available in the `data/` directory and are loaded using relative paths. The notebook uses `pandas`, `numpy`, `matplotlib`, and `seaborn` and can be executed from top to bottom in a Jupyter-compatible environment.

## Conclusion

The analysis identifies Medium Usage customers as the largest segment and describes differences in plan, age, and usage patterns that can guide retention and engagement questions. Extreme usage observations were retained because they were considered plausible customer behavior. The recommendations are hypotheses for further business evaluation, not measured interventions or proven causes of churn.
