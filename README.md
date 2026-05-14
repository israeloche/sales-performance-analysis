# Sales Data Analysis

An exploratory data analysis (EDA) project built in Python using a 1,500-row sales dataset. The notebook uncovers revenue trends, product performance, regional breakdowns, and salesperson effectiveness through data aggregation and visualizations.

---

## Overview

This project analyses a sales dataset to answer key business questions:

- Which products generate the most revenue and units sold?
- How does performance vary across regions?
- What does monthly revenue trend look like over time?
- Which salespersons have the highest customer ratings and transaction volumes?

---

## Dataset

**File:** `sales_dataset.csv`  
**Rows:** ~1,500 sales records

**Key columns used:**

| Column | Description |
|---|---|
| `Date` | Transaction date |
| `Product` | Product name |
| `Category` | Product category (e.g. Electronics, Accessories) |
| `Region` | Sales region |
| `Units Sold` | Number of units sold per transaction |
| `Total Revenue` | Revenue generated (in ₦) |
| `Salesperson` | Name of the salesperson |
| `Customer Rating` | Customer satisfaction score |

---

## Project Structure

```
Sales_Data_Analysis/
├── Sales_Data_Analysis.ipynb   # Main analysis notebook
├── sales_dataset.csv           # Input dataset
├── top_products_revenue.png
├── revenue_share_by_product.png
├── units_per_product.png
├── units_sold_per_region.png
├── units_sold_region_pie.png
├── revenue_per_region.png
├── revenue_by_region.png
├── monthly_revenue_bar.png
├── salesperson_scatterplot.png
└── README.md
```

---

## Analysis Sections

### 1. Product Analysis
- Lists all unique products in the dataset
- Ranks products by total revenue (bar chart)
- Visualises each product's revenue share (pie chart)
- Ranks products by total units sold (bar chart)

### 2. Regional Analysis
- Units sold per region — ranked table, bar chart, and pie chart
- Revenue generated per region — ranked table and bar chart
- Stacked bar chart breaking down revenue by **region × category** (Electronics vs. Accessories)

### 3. Monthly Analysis
- Aggregates revenue by month in chronological order
- Bar chart of monthly total revenue to reveal seasonal trends

### 4. Salesperson Analysis
- Average customer rating per salesperson, ranked
- Scatter plot of **Customer Rating vs. Total Transactions** per salesperson, with reference lines for mean rating and mean transaction count

---

## Requirements

Install dependencies with:

```bash
pip install pandas matplotlib seaborn
```

| Library | Purpose |
|---|---|
| `pandas` | Data loading, cleaning, and aggregation |
| `matplotlib` | Base plotting |
| `seaborn` | Statistical visualisations |

---

## Usage

1. Clone the repository and navigate to the project folder.
2. Ensure `sales_dataset.csv` is in the same directory as the notebook.
3. Launch Jupyter and open the notebook:

```bash
jupyter notebook Sales_Data_Analysis.ipynb
```

4. Run all cells (`Kernel → Restart & Run All`) to reproduce the full analysis and save chart exports.

---

## Output Charts

All charts are saved as `.png` files at 150 DPI in the project directory:

| File | Description |
|---|---|
| `top_products_revenue.png` | Top 10 products by total revenue |
| `revenue_share_by_product.png` | Revenue share pie chart by product |
| `units_per_product.png` | Units sold per product |
| `units_sold_per_region.png` | Units sold by region (bar) |
| `units_sold_region_pie.png` | Units sold by region (pie) |
| `revenue_per_region.png` | Total revenue by region |
| `revenue_by_region.png` | Revenue by region and category (stacked) |
| `monthly_revenue_bar.png` | Monthly revenue trend |
| `salesperson_scatterplot.png` | Rating vs. transactions per salesperson |
