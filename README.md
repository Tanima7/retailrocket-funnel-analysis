# RetailRocket E-Commerce Funnel & Business Intelligence

An end-to-end e-commerce analytics project utilizing the **RetailRocket Recommender System Dataset**. This project analyzes the complete customer journey—from **Product View → Add to Cart → Purchase**—to identify conversion bottlenecks, cart abandonment patterns, customer retention metrics, and actionable revenue opportunities.

---

## 📌 Project Overview

E-commerce businesses rely on behavioral data to optimize conversions and maximize Customer Lifetime Value (CLV). This project processes raw, event-level interaction data to reconstruct the e-commerce funnel, perform RFM customer segmentation, evaluate cohort retention, and score cart recovery potential. Findings are served via SQL queries and an interactive Power BI dashboard.

---

## 🎯 Key Objectives

- **Conversion Funnel Analysis:** Map event flows (Views → Carts → Purchases) and pinpoint drop-off stages.
- **Cart Abandonment:** Evaluate abandonment rates and build a scoring model for targeted recovery.
- **Customer Intelligence:** Implement RFM segmentation and Cohort Retention Analysis to distinguish high-value users from churn risks.
- **Behavioral & Temporal Trends:** Analyze purchasing and activity patterns across hourly, weekday, and monthly dimensions.
- **Category & Product Performance:** Measure item-level velocity, volume, and revenue potential.

---

## 💾 Dataset Architecture

The project leverages the public **RetailRocket** dataset (raw data excluded from the repository due to file size limits):

- `events.csv` — Event logs containing user views, add-to-carts, and completed transactions with timestamps.
- `item_properties_part1.csv` & `item_properties_part2.csv` — Long-format key-value product attributes.
- `category_tree.csv` — Hierarchical category relationships.

> **Note:** Raw CSV files are ignored via `.gitignore`. Processed baseline outputs reside in `data/processed/`.

---

## 🛠 Tech Stack

- **Data Processing & Analytics:** Python (`pandas`, `numpy`)
- **Data Visualization:** Matplotlib, Seaborn
- **Database Querying:** SQL
- **Business Intelligence & Dashboards:** Power BI, DAX
- **Version Control:** Git & GitHub

---

## 🔄 End-to-End Workflow

1. **Data Inspection & Cleaning:** Process raw logs, handle missing values, and normalize event timestamps.
2. **Attribute Extraction:** Selectively extract business-relevant key-value pairs from unstacked product property files to generate a unified `product_master` table.
3. **Hierarchy Integration:** Map event records to category structures and normalized product profiles.
4. **Feature Engineering & Analytics:**
   - Funnel stage mapping and drop-off metrics.
   - Cohort retention matrices and RFM scoring logic.
   - High-intent cart abandonment recovery scoring.
5. **SQL & Power BI Delivery:** Write modular SQL queries for core KPIs and construct an interactive Power BI dashboard (`.pbix`).

---

## 📁 Project Structure

```text
retailrocket-funnel-analysis/
├── data/
│   └── processed/
│       ├── product_master.csv
│       ├── rfm_segments.csv
│       ├── cohort_analysis.csv
│       ├── cart_recovery_score.csv
│       └── category_performance.csv
├── notebooks/
│   └── 01_data_inspection.ipynb
├── sql/
│   └── business_queries.sql
├── outputs/
│   └── figures/
├── dashboard/
│   └── retailrocket.pbix
└── README.md
