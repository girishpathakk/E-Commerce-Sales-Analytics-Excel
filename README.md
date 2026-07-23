# 🛍️ Nyra Store — E-Commerce Sales Analytics Dashboard (2025)

> **An end-to-end Excel-based business intelligence project** analyzing 30,000+ fashion retail orders to uncover customer behavior, channel performance, and regional demand — driving data-backed strategy for 2026.

---

## 📌 Table of Contents

- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Dataset Description](#dataset-description)
- [Data Cleaning Process](#data-cleaning-process)
- [Business Questions Answered](#business-questions-answered)
- [Key Business Insights](#key-business-insights)
- [Strategic Recommendations](#strategic-recommendations)
- [Dashboard Preview](#dashboard-preview)
- [Tools Used](#tools-used)
- [How to Use This Project](#how-to-use-this-project)
- [Project Structure](#project-structure)
- [Author](#author)

---

## 📖 Project Overview

Nyra Store is an emerging e-commerce fashion retailer that experienced rapid growth in 2025 across multiple sales channels (Amazon, Myntra, Flipkart, Meesho, Ajio, Nalli, and others). Despite strong sales volume, the business lacked **actionable intelligence** to guide strategic decisions.

This project delivers a **fully interactive Excel dashboard** built on 30,000+ real sales records. It answers 8 critical business questions across customer demographics, channel performance, order fulfillment, and regional demand — enabling the management team to make informed decisions for 2026.

**What makes this project portfolio-worthy:**
- Raw data → Cleaned data → Pivot Tables → Interactive Dashboard (full ETL pipeline in Excel)
- 30,000+ rows of real-world, messy e-commerce data handled professionally
- Business storytelling with actionable recommendations — not just charts

---

## 🎯 Problem Statement

> *"Nyra Store experienced rapid growth in 2025 but lacks actionable intelligence regarding customer demographics, sales channel efficiency, and regional demand. To optimize inventory planning and maximize marketing ROI for 2026, management requires a comprehensive, data-driven dashboard. This project analyzes 2025 sales data to identify key purchasing trends, top-performing platforms, and core customer segments, culminating in strategic recommendations for the upcoming fiscal year."*

---

## 📊 Dataset Description

| Field | Description |
|---|---|
| **Order ID** | Unique identifier per order |
| **Cust ID** | Customer identifier |
| **Gender** | Customer gender (Men / Women) |
| **Age** | Customer age |
| **Age Group** | Derived: Teen / Young Adult / Adult / Senior |
| **Date** | Order date |
| **Month** | Derived from Date using `=TEXT(G, "mmm")` |
| **Status** | Order status (Delivered / Returned / Cancelled / Refunded) |
| **Channel** | Sales platform (Amazon, Myntra, Flipkart, Meesho, Ajio, Nalli, Others) |
| **SKU** | Product code |
| **Category** | Product category (Kurta, Set, Top, Western Dress, Saree, etc.) |
| **Size** | Product size (XS, S, M, L, XL, XXL, 3XL) |
| **Qty** | Quantity ordered |
| **Currency** | INR |
| **Amount** | Order value in INR |
| **Ship City / State / Postal Code** | Shipping location |
| **B2B** | Whether order is Business-to-Business |

**Dataset Size:** ~31,000 rows × 21 columns

---

## 🧹 Data Cleaning Process

The raw data contained several inconsistencies that were resolved before analysis:

### Issues Found & Fixed

| Issue | Raw Value | Cleaned Value | Method |
|---|---|---|---|
| Inconsistent gender labels | `W`, `M` | `Women`, `Men` | Find & Replace |
| Missing Month column | *(absent)* | `Jan`–`Dec` | `=TEXT(G2,"mmm")` formula |
| Inconsistent quantity | `One`, `Two` | `1`, `2` | Standardized |
| Age group categorization | Raw age numbers | Teen / Young Adult / Adult / Senior | IF formula buckets |

### Age Group Bucketing Formula Used
```excel
=IF(E2<=18,"Teen", IF(E2<=35,"Young Adult", IF(E2<=55,"Adult","Senior")))
```

### Month Extraction Formula
```excel
=TEXT(G2,"mmm")
```

---

## ❓ Business Questions Answered

| # | Business Question | Answer |
|---|---|---|
| 1 | Compare sales and orders using a single chart | Combo chart: Bar (Revenue) + Line (Orders) — March peaks both |
| 2 | Which month had highest sales & orders? | **March** — ₹1.93M revenue, 2,819 orders |
| 3 | Who purchased more — Men or Women? | **Women: 64%**, Men: 36% |
| 4 | What are the different order statuses? | Delivered 92%, Cancelled 3%, Returned 3%, Refunded 2% |
| 5 | Top 10 states contributing to sales? | Maharashtra (₹2.98M) → Karnataka → Uttar Pradesh → ... |
| 6 | Relation between Age and Gender by orders? | Adult Women (33.32%) are the single largest buying segment |
| 7 | Which channel contributes maximum sales? | **Amazon: 35%**, Myntra: 23%, Flipkart: 22% |
| 8 | Highest selling category? | **Set (40%)** followed by Kurta (32%) |

---

## 💡 Key Business Insights

### 1. 👩 Women Drive the Business — 64% of All Revenue
Women account for nearly two-thirds of all purchases. The dominant sub-segment is **Adult Women aged 26–45**, contributing 33.32% of all orders — making them the single most valuable customer group.

### 2. 📅 March is the Revenue Peak — Pre-Summer Demand Surge
March recorded the highest sales (₹1.93M) and maximum orders (2,819). This aligns with the pre-summer fashion buying cycle in India. Sales gradually decline post-April, with a small recovery in August (back-to-college season) and December (festive/year-end gifting).

### 3. 🛒 Amazon Alone Contributes 35% of All Revenue
Amazon is the dominant channel followed closely by Myntra (23%) and Flipkart (22%). Together, these three platforms account for **80% of total revenue** — the remaining 20% is split across Meesho, Ajio, Nalli, and Others.

### 4. 🗺️ Maharashtra & Karnataka are the Revenue Powerhouses
Top 5 states by revenue:
- Maharashtra: ₹2.98M
- Karnataka: ₹2.65M
- Uttar Pradesh: ₹2.10M
- Telangana: ₹1.71M
- Tamil Nadu: ₹1.68M

These 5 states together contribute **~52% of total revenue**, making them the primary geographic focus for marketing and inventory.

### 5. 📦 Set & Kurta = 72% of All Sales Volume
"Set" (ethnic co-ord sets) leads at 40% category share, followed by Kurta at 32%. This means **3 out of every 4 items sold is either a Set or Kurta** — a critical insight for inventory prioritization.

### 6. ✅ 92% Orders Successfully Delivered — Strong Fulfillment
Only 8% of orders face issues (returns, cancellations, refunds). This indicates a healthy logistics pipeline, but the 3% return rate needs product-size accuracy improvement.

### 7. 🧑‍🦱 Young Adults Show Emerging Growth Potential
Young Adult Women (19–35) contribute 19.46% of orders — the second-largest segment. This group is highly influenced by social commerce (Instagram, influencer marketing) and could be a growth lever for Meesho and Myntra channels.

---

## 🚀 Strategic Recommendations for 2026

### 📣 Marketing
- **Invest 60%+ of digital ad budget on Amazon** — run sponsored product campaigns for Set and Kurta categories targeting Women 26–45
- **Double down on Maharashtra and Karnataka** — geo-targeted campaigns with regional language content (Marathi, Kannada) for maximum relevance
- **Launch a Women's Day (March 8) sale campaign** — March is already the peak month; a structured campaign can push it 15–20% higher
- **Activate influencer marketing on Instagram/Meesho** for Young Adult Women (19–35) — this segment is the next growth engine

### 📦 Inventory Planning
- **Stock Sets and Kurtas heavily in Q1 (Jan–Mar)** to meet peak season demand — avoid stockouts in Maharashtra, Karnataka, UP
- **Maintain a 70:30 stock ratio (Women:Men)** across all SKUs to match actual demand distribution
- **Size standardization urgently needed** — "One Size" and inconsistent size labeling contributes to returns; implement clear size charts per SKU

### 🔄 Retention & Loyalty
- **Introduce a loyalty program targeting Adult Women** (26–45) — they buy repeatedly and have the highest lifetime value
- **Re-engage December buyers with January offers** — December shows a revenue uptick that can be converted into Jan–Feb retention

### 📉 Reducing Returns & Cancellations
- **Add detailed size guides** for XXL, XL, and 3XL — oversized categories have higher return rates
- **Enable order modification (not just cancellation)** — reducing cancellations by 1% saves ~₹210K annually
- **Post-delivery customer feedback collection** for returned items to identify root cause (sizing, quality, or expectation mismatch)

### 🌐 Channel Diversification
- **Grow Meesho presence** — it currently contributes only 5% but serves Tier 2/3 cities where Nyra is underpenetrated
- **Explore D2C (Direct-to-Consumer) website** to reduce marketplace commission fees (typically 15–25% on Amazon/Myntra)

---

## 📸 Dashboard Preview

> *Interactive Excel dashboard with slicers for Month, Category, and Channel.*

![Nyra Store Dashboard](https://github.com/girishpathakk/E-Commerce-Sales-Analytics-Excel/blob/main/nyra_store_sales_dashboard_2025.PNG)

**Dashboard Sheets:**
- `Store Sales Report 2025` — Raw data
- `Orders Vs Sales` — Combo chart (monthly trend)
- `Men Vs Women` — Gender analysis
- `Order Status` — Fulfillment breakdown
- `Top 5 States` — Regional heatmap
- `Age Vs Gender` — Demographic cross-tab
- `Orders: Channels` — Channel performance

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| **Microsoft Excel** | Data cleaning, transformation, pivot tables, dashboard |
| **Excel Pivot Tables** | Aggregation and cross-tabulation |
| **Excel Charts** | Combo chart, pie, bar, horizontal bar |
| **Excel Slicers** | Interactive filtering by Month, Category, Channel |
| **Excel Formulas** | `TEXT()`, `IF()`, `VLOOKUP()`, `COUNTIF()`, `SUMIF()` |

---

## 📂 How to Use This Project

1. **Clone or download** this repository
2. Open `nyra_store_annual_sales_report_excel.xlsx` in Microsoft Excel (2016 or later recommended)
3. Navigate to the **`Nyra Store data`** sheet to view raw → cleaned data
4. Go to the **Sales Dashboard 2025** sheet for the interactive view
5. Use the **slicers** (Month, Category, Channel) on the left to filter all charts simultaneously
6. Hover over any chart element for tooltip details

> ⚠️ Note: The file works best on Excel for Windows. Some features may be limited on Excel for Mac or Google Sheets.

---

## 🗂️ Project Structure

```
E-Commerce-Sales-Analytics-Excel/
│
├── README.md                                  ← You are here
├── nyra_store_annual_sales_report_excel.xlsx  ← Main Excel file (raw + cleaned + dashboard)
├── nyra_store_sales_dashboard_2025.png        ← Screenshot of the final dashboard
└── nyra_store_data_raw                        ← Raw data 
   
```

---

## 👤 Author

**Girish Pathak**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin)](https://linkedin.com/in/girishpathakk)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat&logo=github)](https://github.com/girishpathakk)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=flat&logo=gmail)](mailto:girish.pathak.ds@gmail.com)
---

## ⭐ If you found this project helpful, please give it a star!

*This project is part of my Data Analyst portfolio. It demonstrates end-to-end data analysis skills including data cleaning, exploratory analysis, visualization, and business storytelling — all using Microsoft Excel.*

---

> **Skills demonstrated:** Data Cleaning • Pivot Tables • Dashboard Design • Business Analysis • Data Storytelling • Excel Advanced Formulas • Slicers & Interactive Filtering
