# 🛒 Retail Sales & Customer Insights Analysis 

**Tools:** Microsoft Excel · Pivot Tables · XLOOKUP · Power Query (Data Cleaning)  
**Dataset:** ~1,952 retail transactions of a company across United States (2015)  
**Skills demonstrated:** Data cleaning, calculated metrics, dashboard design, business insight communication


## 📌 Project Overview

This project analyzes retail sales data for a U.S based store across multiple product categories, customer segments, and geographic regions. Starting from a messy raw dataset, I cleaned, transformed, and modeled the data entirely in Excel — then built an interactive dashboard to surface key business insights for a retail stakeholder.

The goal was to answer: **Who are our best customers? Which products and regions drive the most revenue? And how efficiently are we fulfilling orders?**



## 🗂️ Dataset Description

| Detail | Value |
|---|---|
| Total Transactions | 1,952 orders |
| Unique Orders | 1,365 |
| Unique Customers | 1,130 |
| Date Range | January – June 2015 |
| Geographic Coverage | 48 U.S. states + D.C. |
| Product Categories | Furniture, Office Supplies, Technology |


## 🧹 Data Cleaning (Raw Data → Calculated Metrics)

The raw dataset contained several quality issues that required systematic cleaning before any analysis could begin:

- **Inconsistent text casing** e.g., `"express "` vs `"Standard"`, `"west"` vs `"East"`
- **Trailing whitespace** in categorical fields like `Ship Mode` and `Product Category`
- **Typographical errors in segment labels** e.g., `"Corporateee"`, `"Home Officess"`
- **Missing customer names** resolved using `XLOOKUP` against a Customer Lookup table
- **Missing product names** resolved using `XLOOKUP` against a Product Lookup table
- **Duplicate rows**  identified and removed from the Raw Data sheet

### Calculated Columns Added

| Column | Formula Logic |
|---|---|
| `Net Sales` | `Unit Price × Quantity Ordered × (1 − Discount)` |
| `Shipping Duration` | `Ship Date − Order Date` (days) |
| `Order Month` | Extracted using `TEXT()` function |
| `Order Day` | Extracted using `TEXT()` function |
| `Customer Category` | `IF(COUNTIF(...) > 1, "Returning Customer", "New Customer")` |

---

## 📊 Dashboard & Key Findings

The final dashboard presents four KPI cards and multiple interactive pivot-based visuals with slicers.

### KPI Summary

| Metric | Value |
|---|---|
| Total Net Sales | **$1,792,865** |
| Total Unique Orders | **1,365** |
| Total Unique Customers | **1,130** |
| Average Shipping Duration | **2 days** |
| Average Discount | **6.3%** |

---

### 💡 Business Insights

**1. Returning customers drive the business.**  
75.2% of total net sales came from returning customers ($1.35M), compared to just 24.8% from new customers ($445K). This signals strong customer loyalty but also highlights the need for better new customer acquisition strategies.

**2. Corporate and Consumer segments lead revenue.**  
Corporate (34.5%) and Consumer (20.6%) segments account for over half of all sales. Home Office and Small Business segments are smaller but present a clear upsell opportunity.

**3. Office Machines, Chairs, and Telephones are top-performing sub-categories.**  
Together these three sub-categories contribute over $740K  more than 40% of total revenue. Rubber Bands and Labels are the lowest performers at under $7K combined.

**4. Sales peak on weekends.**  
Saturday ($419K) and Sunday ($201K) recorded the highest and lowest weekday revenue respectively, though Sunday edges out other midweek days. Friday ($282K) also performs strongly. Marketing and promotions could be timed accordingly.

**5. Los Angeles and New York City dominate city-level revenue.**  
These two cities alone account for over 51% of total net sales. Washington D.C. and Boston are the next strongest markets.

**6. April is the best-performing month (of H1 2015).**  
April generated the highest monthly net sales at $356,920  approximately 20% of the six-month total. January comes second at $256,180.

**7. Standard shipping is preferred.**  
65.1% of orders were shipped via Standard mode, compared to 34.9% via Express suggesting customers prioritize cost over speed, indicating strong price sensitivity.

**8. Most orders ship within 1–2 days.**  
~81% of orders had a shipping duration of 0–2 days, reflecting strong operational efficiency. A small tail of orders took 7–10 days, which may warrant investigation.

---

## 🏆 Top 5 Customers by Net Sales

| Customer | Net Sales |
|---|---|
| Kristine Connolly | $50,083 |
| Nina Horne Kelly | $41,245 |
| Yvonne Mann | $26,043 |
| Toni Swanson | $25,899 |
| Rosemary O'Brien | $25,447 |

---

## 📁 File Structure

```
retail-sales-analysis/
│
├── Customer Insight.xlsx         # Main workbook
│   ├── Raw Data              # Original (messy) dataset
│   ├── Product Lookup        # Sub-category to product name mapping
│   ├── Customer Lookup       # Customer ID to name mapping
│   ├── Calculated Metrics    # Cleaned & enriched dataset (25 columns)
│   ├── Pivot Table           # All pivot tables powering the dashboard
│   ├── Wireframe             # Planning sketch for dashboard layout
│   └── Dashboard             # Final interactive dashboard
│
└── README.md
📥 **(Download the Excel Workbook:https://1drv.ms/x/c/98E2FAE131AE12FE/IQBJHdOR2bRTTJXyA5iTDQ_bAd8kWqwBbrjHWTqtONdK7kg?e=gDfgIm)**
```

---

## 🔧 Skills Applied

- **Data Cleaning:** Identifying and resolving inconsistencies in raw data (casing, whitespace, duplicates, typos)
- **Formula Work:** `XLOOKUP`, `IF`, `COUNTIF`, `TEXT`, arithmetic formulas for calculated metrics
- **Pivot Tables:** Multi-dimensional summarization by segment, region, product, time, and shipping mode
- **Dashboard Design:** KPI cards, slicers for interactivity, visual hierarchy for business storytelling
- **Business Analysis:** Translating numbers into actionable retail insights

---

## 🚀 What I Would Do Next

- Build a Power BI version of this dashboard for more dynamic filtering and drill-through capability
- Segment new vs. returning customers by product category to identify cross-sell opportunities

---

## 👩🏾‍💻 About

Built by **Khadijah Olamide Bello** 
Recently transitioned from Agricultural Economics into data analytics, with a focus on business and consumer data in the Nigerian and Global market context.

🔗 [LinkedIn](https://www.linkedin.com/in/khadijah-bello-049624378) · [GitHub](https://github.com/Olamide-data)
