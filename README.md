# 📊 Vendor Performance & Inventory Analytics Pipeline

---

## 🚀 Project Overview
This project focuses on analyzing vendor performance and inventory efficiency using an end-to-end data pipeline built with Python and SQL.

The goal is to transform raw transactional data into meaningful business insights that help organizations make better decisions related to vendor selection, pricing, and inventory management.

This project simulates a real-world retail/wholesale analytics scenario and demonstrates strong skills in data engineering, data analysis, and business intelligence.

---

## Problem Statement
In many organizations, data related to purchases, sales, and vendors exists in separate systems. This makes it difficult to:

- Identify profitable vendors
- Detect slow-moving inventory
- Understand pricing efficiency
- Analyze vendor contribution to revenue

Without proper analysis, businesses may face:
- High inventory holding costs  
- Low profit margins  
- Inefficient vendor relationships  

---

## Project Objectives
- Build an automated data pipeline to integrate multiple datasets
- Analyze vendor performance across sales and purchases
- Calculate key business metrics like profit and turnover
- Identify underperforming vendors and brands
- Support data-driven decision-making

---

## Dataset Information

- **Source:** CSV files (local dataset)
- **Type:** Structured transactional data
- **Format:** `.csv`
- **Storage:** SQLite database (`inventory.db`)

### Key Tables:
- `purchases` → Purchase transactions
- `purchase_prices` → Product pricing details
- `sales` → Sales transactions
- `vendor_invoice` → Freight and vendor costs

### Key Columns:
- VendorNumber / VendorName
- Brand & Description
- PurchasePrice & SalesPrice
- Quantity & SalesQuantity
- SalesDollars & PurchaseDollars

### Granularity:
- Vendor + Brand level aggregation

---

## Tools & Technologies Used

| Tool | Purpose |
|------|--------|
| Python | Core programming |
| Pandas | Data manipulation & analysis |
| SQL | Data aggregation & joins |
| SQLite | Database storage |
| SQLAlchemy | Database connection |
| Logging | Monitoring pipeline execution |

---

## Project Workflow / Steps

1. 📥 Load raw CSV data  
2. 🗄️ Store data into SQLite database  
3. 🔗 Perform SQL joins and aggregations  
4. 🧹 Clean and preprocess data using Pandas  
5. 📈 Create new business metrics  
6. 💾 Store final results into a summary table  

---

## Data Cleaning & Preparation

- Converted data types (e.g., Volume → float)
- Handled missing values by replacing with 0
- Removed extra spaces from text fields
- Ensured consistency across vendor and product data

---

## Exploratory Data Analysis (EDA)

Performed analysis to understand:

- Distribution of sales and purchase values  
- Vendor contribution to total revenue  
- Relationship between purchase cost and sales revenue  
- Inventory movement trends  

---

## Key Insights / Findings

- Top vendors contribute significantly to overall revenue and profit  
- Some vendors have high purchase costs but low sales → inefficient inventory  
- Low stock turnover indicates overstocking issues  
- Profit margins vary significantly across brands  
- Freight costs impact vendor profitability  

---

## Final Outcome / Results

- Created a **vendor-level summary table** (`vendor_sales_summary`)
- Generated key business KPIs:
  - Gross Profit  
  - Profit Margin (%)  
  - Stock Turnover  
  - Sales-to-Purchase Ratio  

This dataset can be directly used for reporting and decision-making.

---

## Business Impact / Real-World Value

- Helps businesses identify **high-performing vendors**
- Reduces **inventory holding costs**
- Improves **pricing strategies**
- Enables **data-driven procurement decisions**
- Provides foundation for **business intelligence dashboards**

---

## How to Run the Project

### Step 1: Clone the Repository
```bash
git clone <your-repo-link>
cd project-folder
Step 2: Install Dependencies
pip install pandas sqlalchemy
Step 3: Place Data

Add CSV files into the /data folder

Step 4: Run Data Ingestion
python ingestion_db.py
Step 5: Generate Vendor Summary
python get_vendor_summary.py
```

```bash
Project Folder Structure
project-folder/
│
├── logs/                        # Log files
├── ingestion_db.py              # Data ingestion script
├── get_vendor_summary.py        # Data transformation & analysis
├── inventory.db                 # SQLite database
├── notebooks/                   # Jupyter notebooks (EDA)
└── README.md
```

---
## Screenshots

### Brands for Promotional or Pricing Adjustments
<p align="center">
  <img src="Brands for Promotional or Pricing Adjustments.png" width="800"/>
</p>

### Confidence Interval Comparison Top vs Low Vendors
<p align="center">
  <img src="Confidence Interval Comparison Top vs Low Vendors.png" width="800"/>
</p>

### Correlation Heatmap
<p align="center">
  <img src="Correlation Heatmap.png" width="800"/>
</p>

### Count Plots For Categorical Columns
<p align="center">
  <img src="Count Plots For Categorical Columns.png" width="800"/>
</p>

### Impact of bulk purchasing on unit price
<p align="center">
  <img src="Impact of bulk purchasing on unit price.png" width="800"/>
</p>

### Plots For Top Vendors
<p align="center">
  <img src="Plots For Top Vendors.png" width="800"/>
</p>

### Vendor Contribution to total Purchases
<p align="center">
  <img src="Vendor Contribution to total Purchases.png" width="800"/>
</p>

### Top 10 Vendors Purchase Contribution %
<p align="center">
  <img src="Top 10 Vendors Purchase Contribution %.png" width="800"/>
</p>

---

## Author

Mithun Adhe

Email: mithunadhe1664@gmail.com 

LinkedIn: https://linkedin.com/in/mithun-adhe


⭐ If you found this project useful, consider giving it a star!
