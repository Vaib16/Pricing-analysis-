# Tesco Pricing Analyst Demo Project

This repository demonstrates how a pricing analyst can manage **40,000+ SKUs across 120 categories** with daily price changes, using Python + BI.  
It aligns with Tesco’s Pricing Analyst role (2025).

---

## 🚀 Objectives
- Automate **data validation** and anomaly detection.
- Track Tesco’s **price index vs competitors** to monitor value perception.
- Forecast **seasonal demand** for budgeting and promotions.
- Measure **promo uplift vs margin impact** for campaign evaluation.

---

## 📂 Project Tasks

### 1. Data Validation & Exceptions Queue
- Flags missing data, extreme jumps (>20%), and overpriced SKUs (>5% vs competitor).
- Produces `exceptions_queue.csv` (~50 risky SKUs/day out of 40k).

### 2. Price Index Tracker
- Computes monthly price index = `our price ÷ best competitor price`.
- Tracks trends at **category × month** level.

### 3. Seasonal Forecasting
- Decomposes demand into **trend + seasonality**.
- Forecasts baseline + uplift (e.g. December peaks).

### 4. Promo Impact Analysis
- Identifies promo months (≥15% price drop).
- Compares units sold **Before vs During vs After**.
- Evaluates **volume uplift vs margin compression**.

---

## 📊 Results

- ✅ Exceptions Queue: reduced review workload 40k → ~50 SKUs/day.  
- ✅ Price Index: flagged categories drifting above competitor index.  
- ✅ Seasonal Forecast: projected demand uplift for key months.  
- ✅ Promo Analysis: highlighted volume/margin trade-off.  

---

## 🛠️ Tools
- **Python**: pandas, matplotlib, statsmodels  
- **Power BI**: dashboards for exceptions & index trends  
- **Jupyter Notebooks**: reproducible analysis  

---

## 📌 Next Steps
- Integrate cost data to refine margin estimates.  
- Automate a **rule-based proposal engine**.  
- Extend dashboards with **promo efficiency KPIs**.  

---

## 📷 Sample Visuals
![Price Index Trend](reports/visuals/price_index_trend.png)  
![Promo Impact](reports/visuals/promo_impact.png)

---

## 📄 License
MIT License. Free to use for learning and demonstration.
