# 📦 Supply Chain Delivery Performance Analysis

**End-to-end analytics project uncovering why deliveries go late — and what it costs a global e-commerce platform.**

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-yellow)
![Scikit--learn](https://img.shields.io/badge/Scikit--learn-ML-orange)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

---

## 🎯 Overview

Global e-commerce logistics live and die by one promise: *deliver on time.* This project digs into a real-world shipping dataset to answer three questions:

1. How much money are late deliveries actually costing the business?
2. What operational bottlenecks are driving the delays?
3. Can we predict — and prevent — a late delivery before it happens?

**Domain:** Supply Chain Analytics
**Core Problem:** Actual shipping times frequently deviate from scheduled delivery windows, eroding customer trust and cutting into profit.

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python |
| Data Manipulation | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn (custom themes) |
| Machine Learning | Scikit-learn (Random Forest, Train/Test Split), Imbalanced-learn (SMOTE) |

---

## 🧹 Data Processing & Feature Engineering

**Cleaning**
- Started from a raw Kaggle dataset: **180,000+ records, 53 columns**
- Dropped irrelevant fields (product images, customer emails, zip codes) and filtered out cancelled orders
- Standardized all date-time formats

**Engineered Features**
| Feature | Definition |
|---|---|
| `Order Processing Time` | Shipping date − Order date |
| `Delay Days` | Order Processing Time − Scheduled Shipment Days |
| `Profitability Flag` | Order categorized as Profit / Loss / Break-even |
| `Time Features` | Month, Day of Week, Hour extracted from order timestamps |

---

## 📊 Key Business KPIs

- 🚨 **54.71%** of orders arrive late — a systemic issue, not a one-off
- 💰 **$2.1M** in profit tied up in delivery delays
- 📈 Average order profit: **$22**
- ⏱️ 90% of delayed orders arrive within **3 days** of the scheduled window

---

## 🔍 EDA Insights

**Profitability**
- 80.7% of orders are profitable
- 18.7% result in a loss

**Operational Bottlenecks**
- 🚚 **First Class shipping** — 100% delay rate (yes, all of them)
- 🌍 **Central Africa** — highest regional delay rate at 58.7%
- 💄 **Health & Beauty** — highest-delay product category

**Time Trends**
- 📅 Peak delay months: **August, October, December** (holiday/festival surge)
- 🕐 Peak delay hours: **12–1 PM** and **7–8 AM**
- 📆 Monday and Sunday orders are most delay-prone

---

## 🤖 Predictive Modeling

- **Model:** Random Forest Classifier — predicts late-delivery risk
- **Imbalance Handling:** SMOTE applied to balance the training set
- **Performance:**
  - Accuracy: **74%**
  - Precision: **78%** (catching high-risk orders before they go late)

---

## 💡 Strategic Recommendations

1. **Audit shipping capacity** — First & Second Class modes show disproportionate failure rates
2. **Deploy the predictive model** as a live at-risk order alert system
3. **Fix payment friction** — "Payment Review" and "Pending Payment" statuses correlate with delays
4. **Plan for seasonal surges** — build extra capacity ahead of December
5. **Enrich future data** — add carrier-level data, weather events, and warehouse utilization for a sharper model

---

## 📁 Project Structure (suggested)

```
supply-chain-analysis/
├── data/
│   └── raw_dataset.csv
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_eda.ipynb
│   └── 03_modeling.ipynb
├── src/
│   └── feature_engineering.py
├── README.md
└── requirements.txt
```

---

## 📌 Takeaway

This isn't a one-off delay problem — it's a systemic operational gap costing millions in profit. The data points to clear, fixable causes: shipping mode reliability, payment friction, and seasonal capacity planning. A 74%-accurate predictive model turns this from reactive firefighting into proactive intervention.

---

*Feel free to ⭐ this repo if you found the analysis useful!*
