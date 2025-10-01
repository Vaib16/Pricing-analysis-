# Tesco Pricing Analyst Demo Project  

This repository demonstrates how a pricing analyst can scale decision-making for **40,000+ SKUs across 120 categories** with daily price changes. The solution uses **Python for data modeling** and produces **BI-ready outputs** for reporting and automation.  

---

## 🚀 Objectives  
1. Automate **data validation** and anomaly detection to cut manual review.  
2. Monitor Tesco’s **price index vs competitors** to track value perception.  
3. Forecast **seasonal demand** for stock and budgeting alignment.  
4. Quantify **promotion uplift vs margin impact** for campaign evaluation.  

---

## 📂 Project Components  

### 1. Data Validation & Exceptions Queue  
- Rules for missing prices, extreme jumps (>20%), and overpriced SKUs (>5% vs competitor).  
- Produces `exceptions_queue.csv`, reducing daily scope from **40,000 SKUs → ~50 high-risk SKUs**.  

### 2. Price Index Tracker  
- Calculates monthly price index = `our_price ÷ best_competitor_price`.  
- Aggregates at **SKU and category level** to surface competitive drift.  

### 3. Seasonal Forecasting  
- Time-series decomposition (trend + seasonality) with Holt-Winters modeling.  
- Generates **baseline demand forecasts** and seasonal multipliers.  

### 4. Promotion Impact Analysis  
- Detects promo windows (≥15% MoM price drop).  
- Compares units sold **Before / During / After**.  
- Evaluates **sales uplift vs margin compression**.  

---

## 📊 Results  

- ✅ **Exceptions Queue**: reduced daily review workload by >99%.  
- ✅ **Price Index Tracker**: flagged overpricing risks (e.g., Garden Tools index >1.10).  
- ✅ **Seasonal Forecasting**: projected demand peaks (e.g., December uplift).  
- ✅ **Promo Impact**: revealed trade-offs between sales growth and profitability.  

---

## 🛠️ Tech Stack  

- **Python**: pandas, numpy, matplotlib, statsmodels  
- **Jupyter Notebooks**: reproducible workflow and ETL  
- **BI-ready Outputs**: star-schema design for Power BI dashboards  

---

## 📌 Roadmap  

- Incorporate **COGS data** for true margin accuracy.  
- Build a **rule-based proposal engine** for pricing recommendations.  
- Extend Power BI dashboards with **promo efficiency KPIs** and automated alerts.  
- Integrate **dbt, Airflow, and Great Expectations** for governance and orchestration.  

---

## 📷 Sample Visuals  

---

## 📄 License  
MIT License – Free to use for learning, demo, and case-study purposes.  
