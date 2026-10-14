# Vendor Performance Analysis | Python, SQL, MySQL & Power BI

## Project Overview

The **Vendor Performance Analysis** project focuses on evaluating vendor performance, sales trends, purchasing contribution, profitability, and inventory efficiency using data analytics.

The project uses Python for data cleaning and exploratory data analysis, SQL and MySQL for data extraction, statistical techniques to investigate vendor and product performance, and Power BI to present business insights through interactive dashboards.

The goal is to help businesses understand which vendors contribute the most to sales and purchases, identify low-performing products, analyze profit margins, and highlight capital tied up in unsold inventory.

## Dashboard Preview

### 1. Vendor Performance Dashboard — Detailed Analysis

![Vendor Performance Dashboard - Detailed Analysis](images/vendor-performance-dashboard-detail.png)

### 2. Vendor Performance Dashboard — Business Insights

![Vendor Performance Dashboard - Business Insights](images/vendor-performance-dashboard.png)

## Objectives

- Analyze overall sales, purchase costs, and gross profit.
- Identify the top-performing vendors and brands by sales.
- Calculate vendor contribution to total purchases.
- Identify products with low sales but high profit margins.
- Analyze stock turnover and slow-moving inventory.
- Estimate the capital tied up in unsold inventory.
- Compare profit margins and investigate their statistical confidence intervals.
- Build interactive Power BI dashboards for business reporting.

## Tools and Technologies

| Tool | Purpose |
|---|---|
| Python | Data analysis and calculations |
| Pandas | Data manipulation and aggregation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical charts and visual analysis |
| SQL | Data extraction and filtering |
| MySQL | Data storage and querying |
| SQLAlchemy | Connecting Python to MySQL |
| SciPy | Statistical analysis |
| Power BI | Interactive dashboards and KPI reporting |
| Jupyter Notebook | Analysis and documentation |

## Project Workflow

1. **Data extraction:** Connect Python to MySQL and retrieve vendor sales summary data using SQL queries.
2. **Data exploration:** Review dataset structure, summary statistics, numerical distributions, and categorical variables.
3. **Data quality analysis:** Investigate missing or unusual values, zero sales, non-positive profit margins, and potential outliers.
4. **Data filtering:** Apply SQL filters to focus the analysis on records with positive gross profit, positive profit margin, and positive sales quantity.
5. **Exploratory data analysis:** Use distribution plots, boxplots, count plots, and correlation heatmaps.
6. **Vendor and brand analysis:** Rank vendors and brands by sales and evaluate purchase contribution.
7. **Inventory analysis:** Examine stock turnover and estimate the value of unsold inventory.
8. **Statistical analysis:** Compare profit margin distributions and calculate 95% confidence intervals.
9. **Dashboard development:** Present business KPIs, vendor rankings, purchasing contribution, and performance comparisons in Power BI.

## Key Analysis and Business Questions

### 1. Sales and Profitability
- What are the total sales, total purchases, and gross profit?
- Which vendors and brands generate the highest sales?
- How do sales and purchase costs vary across products?
- How does profit margin vary across the dataset?

### 2. Vendor Contribution Analysis
- Which vendors contribute the most to total purchases?
- What percentage of purchasing expenditure comes from the top 10 vendors?
- How dependent is the business on its major suppliers?
- Which vendors should be monitored to manage supplier concentration risk?

### 3. Brand Performance Analysis
- Which brands have low sales but high profit margins?
- Which brands may benefit from promotional or pricing adjustments?
- How do sales values compare across brands?

### 4. Inventory Analysis
- Which vendors have low stock turnover?
- Which products may represent slow-moving inventory?
- How much capital is tied up in unsold inventory?
- Which vendors contribute the most to unsold inventory value?

### 5. Statistical Analysis
- What is the relationship between numerical variables?
- How do profit margins vary between higher-sales and lower-sales groups?
- What are the 95% confidence intervals for the selected profit margin groups?

## Dashboard Highlights

The Power BI dashboard includes the following business metrics and visualizations:

- **Total Sales:** Overall sales value.
- **Total Purchase:** Overall purchasing expenditure.
- **Gross Profit:** Difference between sales and purchase costs, as defined in the analysis.
- **Profit Margin:** Profitability indicator.
- **Unsold Capital:** Estimated value of unsold inventory.
- **Purchase Contribution:** Vendor-wise contribution to total purchases.
- **Top Vendors by Sales:** Ranking of leading vendors.
- **Top Brands by Sales:** Ranking of leading brands.
- **Low-Performing Vendors:** Identification of vendors requiring further investigation.
- **Low-Performing Brands:** Comparison of brand sales and performance indicators.

## Key Business Insights

The analysis is designed to support the following business decisions:

- Identify vendors responsible for a large share of purchasing expenditure.
- Focus sales and marketing efforts on products with growth potential.
- Investigate vendors and products with weak inventory turnover.
- Monitor capital tied up in inventory that has not been sold.
- Compare profitability across products and vendor groups.
- Use dashboard KPIs to support data-driven purchasing and sales decisions.

*Final business conclusions should be based on the actual query outputs, validated calculations, and dashboard filters.*

## Repository Structure

```text
Vendor-Performance-Analysis/
│
├── README.md
├── Vendor Performance Analysis.ipynb
│
├── images/
│   ├── vendor-performance-dashboard.png
│   └── vendor-performance-dashboard-detail.png
│
├── sql/
│   └── analysis_queries.sql
│
└── powerbi/
    └── Vendor_Performance_Dashboard.pbix
```

*The folders and optional files above are the recommended structure. Add them to GitHub when they are available in your project.*

## How to Run the Project

### Prerequisites

- Python 3.10 or a compatible version
- Jupyter Notebook
- MySQL Server
- A MySQL database containing the required vendor sales summary table
- Power BI Desktop to open the dashboard file

### Step 1: Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/Vendor-Performance-Analysis.git
cd Vendor-Performance-Analysis
```

Replace `YOUR-USERNAME` with your GitHub username.

### Step 2: Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn sqlalchemy pymysql scipy jupyter
```

### Step 3: Configure the MySQL Database

Create or configure the `vendor_project` database and make sure the `Vendor_sales_summary` table is available.

Update the database connection in the notebook to use your own credentials. Do not upload your real password.

Example:

```python
from sqlalchemy import create_engine
import os

user = os.getenv("MYSQL_USER")
password = os.getenv("MYSQL_PASSWORD")
host = os.getenv("MYSQL_HOST", "localhost")
database = os.getenv("MYSQL_DATABASE", "vendor_project")

engine = create_engine(
    f"mysql+pymysql://{user}:{password}@{host}:3306/{database}"
)
```

Set the required environment variables before running the notebook.

### Step 4: Run the Jupyter Notebook

```bash
jupyter notebook
```

Open `Vendor Performance Analysis.ipynb` and run the cells in sequence.

### Step 5: Open the Power BI Dashboard

Open the `.pbix` file in Power BI Desktop. If the original database connection is unavailable, configure the data source and refresh the data as required.

**Note:** The database, source dataset, and Power BI file must be included or made available separately for another person to reproduce the complete project. Screenshots alone are not sufficient to recreate the interactive dashboard.

## Future Improvements

- Automate data refresh and reporting.
- Add vendor performance scoring and risk indicators.
- Improve inventory forecasting and demand planning.
- Add date-based sales and profitability trends.
- Develop more detailed supplier concentration analysis.
- Publish the dashboard to Power BI Service where appropriate.

## Skills Demonstrated

Python · SQL · MySQL · Data Cleaning · Exploratory Data Analysis · Statistical Analysis · Data Visualization · Business Intelligence · Power BI Dashboards · Vendor Analytics · Inventory Analysis · Profitability Analysis

## Author

**Karan Dabhade**

Aspiring Data Analyst | Python | SQL | MySQL | Power BI | Excel

[LinkedIn](https://www.linkedin.com/in/karan-dabhade/)

---

If you find this project useful, feel free to explore the repository and share your feedback.
