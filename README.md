# End-to-End Business Intelligence Suite: Olist E-Commerce Logistics Analytics {IN PROGRESS}

An enterprise-grade, data-driven Business Intelligence (BI) suite engineered to transform raw, multi-tenant e-commerce data into interactive, executive-ready analytical dashboards. Utilizing the Olist Brazilian marketplace dataset from Kaggle, this project builds a complete data pipeline—spanning data cleansing, advanced SQL transformation, and dimensional relational modeling—to isolate logistical bottlenecks, track delivery performance, and optimize supply chain visibility.

## 🚀 Core Analytical Insights & KPIs
*   **Fulfillment & Delivery Velocity:** Tracks transit times, carrier performance, and estimated vs. actual delivery time variations.
*   **Financial & Freight Analytics:** Evaluates the economic impact of freight costs on customer acquisition and total order values.
*   **Seller Operational Efficiency:** Measures order processing delays and product distribution patterns across multiple product categories.

## 🛠️ Tech Stack & Architecture
*   **Data Sourcing:** Kaggle Olist Dataset (9 Modules: Customers, Orders, Payments, Reviews, Products, Sellers, Items, Geolocation, Category Translations).
*   **Data Engineering (ETL):** Python (Pandas, NumPy) for initial data wrangling, missing value treatment, and timestamp standardisation.
*   **Database & Query Optimization:** SQL (DDL/DML) for structural data joining, index filtering, and metric aggregation.
*   **Business Intelligence & Dashboarding:** Power BI (DAX, Power Query) for interactive dashboard deployment and advanced relational modelling.

## 📁 Repository Structure (BEING IMPLEMENTED)
```text
├── data/                   # Directory for raw and processed datasets (Git-ignored)
├── python_scripts/         # ETL and data engineering components
│   ├── data_cleaning.py    # Standardises date formats, handles null records
│   └── structural_join.py  # Exports clean merged datasets into tabular formats
├── sql_queries/            # Complex analytical SQL transformations
│   ├── delivery_kpis.sql   # Calculates actual vs estimated delivery windows
│   └── regional_trends.sql # Aggregates regional order densities and freight spend
├── reports/                # Visual asset templates
│   └── olist_bi_suite.pbix # Central Power BI application file
└── README.md
```

## ⚙️ Project Workflow & Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/creepyherobrineIII/Olist-Business-Intelligence-Suite.git
   cd Olist-Business-Intelligence-Suite
   ```

2. **Data Acquisition:**
   * Download the raw e-commerce dataset from [Kaggle's Olist Dataset](https://kaggle.com).
   * Unzip and place all CSV files inside a local `/data/raw/` directory.

3. **Execute Python Data Preprocessing:** (CURRENT STAGE)
   Ensure you have your environment libraries installed (`pip install pandas numpy`), then clean the raw logs:
   ```bash
   python python_scripts/data_cleaning.py
   ```

4. **Database Injection & Query Execution:** (TO BE DONE)
   * Import the clean tables into your preferred SQL environment (PostgreSQL / MySQL / SQL Server).
   * Run the scripts inside `/sql_queries/` to generate optimized views or materialized summary tables for performance.

5. **Power BI Visualization:** (TO BE DONE)
   * Open `/reports/olist_bi_suite.pbix` using Power BI Desktop.
   * Update the data source settings to point to your local SQL tables or processed CSV files, then hit **Refresh**.

## 📊 Relational Data Model Design (TO BE DONE)
The data schema inside Power BI follows an optimized **Star / Snowflake Schema** architecture to ensure fast rendering times:
*   **Fact Table:** `fact_order_items` (Captures price, freight value, dates, and core transaction links).
*   **Dimension Tables:** `dim_customers`, `dim_sellers`, `dim_products`, and `dim_geolocation` linked through strict primary/foreign key configurations.


## 📄 License
This project is open-source and available under the MIT License.
