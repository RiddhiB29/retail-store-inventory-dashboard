#  Retail Store Inventory Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

---

##  Project Overview
This project analyzes **2 years of daily retail inventory data** across 5 stores and 20 products to uncover sales trends, inventory inefficiencies, and the true impact of promotions and pricing on revenue.

Built an interactive 4-page Power BI dashboard using a Burgundy & Beige theme with dynamic slicers, cross-filtering, and DAX measures.

---

##  Tools Used
| Tool | Purpose |
|------|---------|
| Python (Pandas) | Data cleaning & EDA |
| Matplotlib & Seaborn | Data visualization |
| Power BI Desktop | Interactive dashboard |
| DAX | KPI measures & calculations |
| GitHub | Version control & showcase |

---

## 📊 Dataset
| Feature | Detail |
|---------|--------|
| Rows | 73,100 |
| Columns | 15 |
| Period | Jan 2022 – Jan 2024 |
| Stores | 5 |
| Products | 20 |
| Categories | Electronics, Clothing, Furniture, Groceries, Toys |

---

## 🧹 Data Cleaning
The dataset was clean with zero missing values. Three fixes were applied:
- Clamped 673 negative Demand Forecast values to 0
- Converted Date column from text to datetime format
- Relabeled Holiday/Promotion from 0/1 to meaningful text labels

---

## 📈 Dashboard Pages

### Page 1 — Sales & Revenue Overview
![Dashboard](images/dashboard%20pdf.pdf)

| KPI | Value |
|-----|-------|
| Total Revenue | $494.97M |
| Total Units Sold | 10M |
| Avg Order Value | $6.77K |
| Stockout Days | 360 |

### Page 2 — Inventory Health
| KPI | Value |
|-----|-------|
| Stockout Days | 360 |
| Stockout Rate | 0.49% |
| Avg Utilization | 49.80% |
| Excess Stock | 138 units avg |

### Page 3 — Promotions & Pricing
| KPI | Value |
|-----|-------|
| Promo Revenue | $246.22M |
| Normal Revenue | $248.75M |
| Revenue Lift % | -1.02% |

### Page 4 — External Factors
| KPI | Value |
|-----|-------|
| Top Region | East |
| Peak Month | July |
| Weather Impact | None |
| Seasonal Impact | None |

---

## 📊 EDA Charts

### Revenue by Category & Store
![Chart 1]images/python%20chart1.png

### Monthly Revenue Trend
![Chart 2]images/python%20chart2.png

### Correlation Matrix & Discount Analysis
![Chart 3](images/chart3_correlation.png)

### Weather & Season Impact
![Chart 4](images/chart4_external.png)

### Promotions Analysis
![Chart 5](images/chart5_promotions.png)

### Stockout Risk & Inventory Utilization
![Chart 6](images/chart6_inventory.png)

### Key Insights Summary
![Chart 7](images/chart7_summary.png)

---

## 🔑 Key Business Insights

### 1️ Promotions Are Not Working
Normal days generate **$248.75M** vs promo days **$246.22M** — a **-1.02% revenue decline** during promotions. The business is spending on promotions that are actually hurting revenue.

### 2️ Discounts Drive Volume But Kill Margins
Higher discounts increase units sold slightly but significantly reduce revenue per unit. The current discount strategy is not optimized for profit.

### 3️ Inventory Is Overstocked
Average inventory utilization is only **49.80%** — meaning stores are carrying twice the stock they actually need. This ties up capital unnecessarily.

### 4️ P0019 Is A Stockout Risk
Product P0019 has the highest stockout days **(25 days)** — meaning customers are regularly finding empty shelves for this product.

### 5️ All Stores Perform Equally
Revenue ranges from **$97.43M to $100.50M** across all 5 stores — less than 3% difference. No single store is significantly outperforming or underperforming.

### 6️ External Factors Have No Impact
Weather and seasonality show **near-zero correlation** with sales — the business performs consistently regardless of external conditions.

### 7️ Price Matches Competitors Perfectly
Correlation between our price and competitor pricing is **0.99** — we are almost perfectly aligned with market pricing.

---

## 💡 Recommendations

### 1. Re-evaluate Promotion Strategy
> Promotions are reducing revenue by 1.02%. Consider replacing blanket discounts with targeted promotions for slow-moving products only.

### 2. Reduce Inventory Levels
> With only 49.80% utilization, stores can safely reduce stock by 20-30% to free up working capital without risking stockouts.

### 3. Fix P0019 Supply Chain
> P0019 has 25 stockout days — the highest in the dataset. Increase reorder frequency and safety stock for this product immediately.

### 4. Investigate Discount Strategy
> Discount has near-zero correlation with units sold (0.00). This means discounts are not driving customer purchases — they are simply reducing margins. Consider eliminating or restructuring discounts.

### 5. Leverage July Peak
> July is consistently the peak revenue month. Plan inventory builds and marketing pushes ahead of July to maximize this natural demand spike.

---

## Project Structure
```
retail-store-inventory-dashboard/
│
├── images/                              # Charts and dashboard screenshots
│   ├── dashboard_pdf.pdf                # Power BI dashboard (all 4 pages)
│   ├── chart1_revenue.png               # Revenue by category & store
│   ├── chart2_trend.png                 # Monthly revenue trend
│   ├── chart3_correlation.png           # Correlation matrix
│   ├── chart4_external.png              # Weather & season impact
│   ├── chart5_promotions.png            # Promotions analysis
│   ├── chart6_inventory.png             # Stockout & inventory
│   └── chart7_summary.png              # Key insights summary
│
├── retail_store_inventory.csv           # Original dataset
├── retail_store_inventory_clean.csv     # Cleaned dataset
├── Retail_Store.ipynb                   # Python cleaning & EDA notebook
├── Retail_Store_Dashboard.pbix          # Power BI dashboard
└── README.md                            # Project documentation
```

---

##  How to Run
1. Clone this repository
2. Open `Retail_Store.ipynb` in Jupyter Notebook
3. Run all cells to reproduce cleaning and EDA charts
4. Open `Retail_Store_Dashboard.pbix` in Power BI Desktop
5. Explore all 4 interactive dashboard pages!

---

