# Retail_Sales-Customer_Analytics

2. The tools we will use

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

/Text
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
│
└── README.md
/
