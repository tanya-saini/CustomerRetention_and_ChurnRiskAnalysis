# Customer Retention & Churn Risk Analysis Using RFM and ML

```text
                    TRANSACTION DATA
                           │
                           ▼
                   DATA PREPARATION
                           │
                           ▼
                  EXPLORATORY ANALYSIS
                           │
             ┌─────────────┴──────────────┐
             ▼                            ▼
       SALES / PRODUCT              CUSTOMER BEHAVIOR
             │                            │
             │                            ▼
             │                           RFM
             │                            │
             │                            ▼
             │                    CUSTOMER SEGMENTS
             │                            │
             └─────────────┬──────────────┘
                           ▼
                 CHURN / RETENTION
                     DEFINITION
                           │
                           ▼
                    ML PREDICTION
                           │
                           ▼
                 CHURN RISK SCORE
                           │
                           ▼
                 BUSINESS ACTIONS
```

RFM gives us customer behavioral features and segments.

Then the ML model uses those features to predict a future outcome.

---

define what "churn" means.
- Churn = 1 → no purchase in next 90 days
- Churn = 0 → purchased again

Cutoff = 1 September 2011

We calculate each customer's RFM using purchases up to September 1.

Then we look forward.

Retained

Customer makes at least one purchase during the following 90 days.

Churn/inactive

Customer makes no purchase during the following 90 days.

---

Primary model: Logistic Regression

Why?

Because it is:

relatively simple
highly interpretable
excellent for a business analytics project
naturally produces probabilities
easy to explain to recruiters
suitable for binary churn prediction

---

  ### 01. The tools we will use

We don't need to force every tool into the project. Each tool should have a job.

Tool	Purpose
- Jupyter / Python=	Cleaning, EDA, RFM, statistical analysis
- Pandas / NumPy=	Data manipulation
- Matplotlib / Seaborn=	Analytical visualizations
- SQL=	Business queries and validation
- Excel=	Quick validation, pivots, sanity checks
- Power BI=	Main professional dashboard
- Looker Studio=	Optional second dashboard/report
- Machine Learning=	Only if the data/business question justifies it
- Git/GitHub=	Project version control and portfolio

SQL should answer real business questions, while Python should handle the deeper analytical work.

```text
Retail_Analytics_Project/
│
├── data/
│   ├── raw/
│   │   └── Online Retail.xlsx
│   │
│   ├── processed/
│   │   ├── retail_cleaned.csv
│   │   └── customer_rfm.csv
│   │
│   └── exports/
│
├── notebooks/
│   ├── 00_project_setup.ipynb
│   ├── 01_data_ingestion_validation.ipynb
│   ├── 02_data_preprocessing.ipynb
│   ├── 03_eda_sales_analysis.ipynb
│   ├── 04_customer_analysis.ipynb
│   ├── 05_rfm_segmentation.ipynb
│   ├── 06_sql_business_analysis.ipynb
│   ├── 07_advanced_analysis.ipynb
│   ├── 08_modeling_optional.ipynb
│   ├── 09_evaluation_validation.ipynb
│   └── 10_dashboard_data_export.ipynb
│
├── sql/
│   ├── sales_queries.sql
│   ├── customer_queries.sql
│   └── rfm_queries.sql
│
├── dashboards/
│   ├── powerbi/
│   └── looker_studio/
│
├── reports/
│   └── project_report.md


--- 

                       RAW DATA
                          │
                          ▼
                 DATA VALIDATION
                          │
                          ▼
                  PREPROCESSING
                          │
                          ▼
                 CLEAN DATASETS
                          │
            ┌─────────────┴─────────────┐
            ▼                           ▼
       SALES ANALYSIS             CUSTOMER ANALYSIS
            │                           │
            │                           ▼
            │                          RFM
            │                           │
            │                           ▼
            │                    RFM SEGMENTATION
            │                           │
            └─────────────┬─────────────┘
                          ▼
                 CHURN DEFINITION
                          │
                          ▼
              RETENTION / CHURN EDA
                          │
                          ▼
              ASSOCIATION ANALYSIS
                          │
                          ▼
                  ML MODEL
                          │
                 ┌────────┴────────┐
                 ▼                 ▼
          Logistic Regression  Random Forest
                 │                 │
                 └────────┬────────┘
                          ▼
                   MODEL EVALUATION
                          │
                          ▼
                   CHURN PROBABILITY
                          │
                          ▼
                 BUSINESS SEGMENTS
                          │
            ┌─────────────┼─────────────┐
            ▼             ▼             ▼
          SQL          POWER BI      EXCEL
```

---


│
└── README.md
```
