# 📊 Dynamic Pricing & Demand Forecasting Engine (Python | Pandas | SQLite)

## 🚀 Overview

This project simulates a real-world retail pricing system that uses historical sales data to:

- Forecast product demand  
- Detect inefficiencies (e.g. high wastage)  
- Recommend pricing or supply adjustments  

The goal is to demonstrate how data analysis can directly support **business decision-making in retail operations**.

---

## 💡 Business Problem

Retail businesses often struggle with:

- Overstocking → leads to waste  
- Underpricing → reduces profit margins  
- Poor demand planning → lost revenue  

This project solves that by using historical transaction data to generate **data-driven pricing recommendations**.

---

## ⚙️ What This Project Does

### 1️⃣ Demand Forecasting
- Uses historical averages to estimate next-period demand  
- Helps anticipate product performance  

### 2️⃣ Pricing Recommendation Engine

Based on demand & wastage:

- 📈 High demand + low waste → **Increase Price**  
- 📉 High demand + high waste → **Reduce Supply**  
- ⚠️ Low demand + high waste → **Discount Price**  
- ✅ Otherwise → **Keep Stable**  

---

## 📊 Example Output

| Product_ID | Avg Demand | Forecast | Action |
|----------|-----------|----------|--------|
| 1001     | 1968      | 1968     | Reduce Supply |
| 1005     | 1875      | 1875     | Reduce Supply |

---

## 📈 Key Insight

The analysis revealed that several products showed consistently high demand but also high wastage.

This indicates inefficiencies in supply planning rather than pricing alone, leading to actionable recommendations such as reducing supply instead of increasing price.

This demonstrates how data analysis can uncover hidden operational issues beyond surface-level metrics.

---

## 📊 Dashboard & System Outputs

This section shows the full pipeline of the pricing engine — from raw data to final business decisions:

### 🗄️ Database View (Raw Data - SQL)
![Database View](database_view.png)

### 📈 Demand Forecast Output (Python)
![Forecast Output](forecast_output.png)

### ⚙️ Pricing Engine Decisions (Python Logic)
![Pricing Engine Output](pricing_engine_output.png)

### 📊 Airtable Dashboard (Final Business Output)
![Airtable Dashboard](airtable_dashboard.png)

---

## 🔄 Workflow

1. Raw transaction data → stored in SQLite  
2. Aggregation → calculate demand & wastage  
3. Forecast → estimate future demand  
4. Decision logic → generate pricing action  
5. Output → pushed to Airtable dashboard  

---

## 🧱 Project Structure

```
dynamic-pricing-engine/
│
├── data/
├── database/
├── outputs/
├── scripts/
├── airtable_dashboard.png
├── forecast_output.png
├── pricing_engine_output.png
├── database_view.png
├── README.md
```

---

## ▶️ How to Run

```bash
python scripts/run_pricing_engine.py
python scripts/run_forecast.py
python scripts/run_pricing_to_airtable.py
```

---

## 🛠 Tech Stack

- Python  
- Pandas  
- SQLite  
- Airtable API  

---

## 👤 Author

Seun Oseola
