# Online Retail Growth Analytics

A concise end-to-end growth analytics pipeline for an “Online Retail” dataset. This project demonstrates best practices in data cleaning, funnel & cohort analysis, product ranking, seasonality modeling, and dashboarding.

---

## Description

We analyze 541,909 transactions (8 fields) from an e-commerce retailer to answer key growth questions:

- Data quality & cleaning  
- Sales volume & revenue trends  
- Funnel conversion & cohort retention  
- Product performance (top-selling vs. top-revenue items)  
- Customer behavior (repeat vs. one-time buyers, AOV)  
- Seasonality & rolling trends  

---

## Project Structure

.
├── data.csv                # Raw dataset  
├── pythonproject.ipynb     # Jupyter/Colab notebook with analysis code  
└── README.md               # This file  

---

## Prerequisites

- Python 3.7+  
- pandas, numpy, matplotlib  
- Jupyter Notebook or Google Colab  

---

## Setup & Installation

1. Clone the repo  
   git clone https://github.com/your-username/online-retail-analytics.git  
   cd online-retail-analytics  

2. Install dependencies  
   pip install pandas numpy matplotlib  

3. Place `data.csv` in the project root  

---

## Usage

1. Open `pythonproject.ipynb` in Jupyter or Colab  
2. Run all cells in order  
3. Review outputs:  
   - Data quality metrics  
   - Revenue & funnel charts  
   - Product ranking lists  
   - Cohort retention heatmap  
   - Seasonality plots  

---

## Methodology

1. Data Cleaning  
   - Drop rows missing `CustomerID` or `Description`  
   - Exclude non-positive `Quantity` and `UnitPrice` entries  

2. Feature Engineering  
   - Compute `TotalPrice = Quantity × UnitPrice`  
   - Extract `Month`, `Quarter`, and `Weekday` from `InvoiceDate`  

3. Analysis  
   - Revenue & Volume: total/net revenue, items sold, monthly trend  
   - Funnel & Cohorts: stage conversion rates, repeat vs. one-time buyers, AOV  
   - Product Analysis: top 10 by quantity vs. revenue  
   - Seasonality: monthly/quarterly trends, 30-day rolling average  

---

## Key Findings

- Net revenue: £8,300,065.81 over the period  
- Total items sold: 5,167,812  
- Busiest weekday: Fridays have the highest average items/invoice  
- Top products by volume:  
  - PAPER CRAFT , LITTLE BIRDIE  
  - MEDIUM CERAMIC TOP STORAGE JAR  
- Repeat buyers: 65.6% (one-timers: 34.4%)  
- Seasonal spikes: strong Q4 holiday lift  

---

## Limitations

- ~25% missing `CustomerID` biases cohort analysis  
- No true “add to cart” or promotional flags captured  
- Bulk orders may mask individual behavior  

---

## Recommendations

1. Enforce `CustomerID` capture at checkout  
2. Instrument cart-abandon events for full funnel visibility  
3. Tag promotional campaigns for lift analysis  
4. Launch re-engagement campaigns for one-time buyers  

---

## License

MIT © 2025 Rohan Adusumilli
