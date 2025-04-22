# Real-Time M&A Predictive Analytics Dashboard

A real-time data pipeline and dashboard to forecast Mergers & Acquisitions (M&A) deal success using company financials, market data, macroeconomic indicators, and news sentiment.

### Why this project?
It empowers analysts to:

- Identify high-potential acquisition targets
- Monitor deal viability in real time
- Visualize market conditions influencing M&A outcomes

---

## Key Features

| Feature | Description |
|--------|-------------|
| **Real-Time Data** | Pulls financial, stock, macroeconomic, and news data every 6 hours |
| **Predictive Modeling** | Uses financial + market + sentiment data to predict M&A deal success |
| **Live Dashboard** | Built with Power BI: filters, KPIs, company snapshots, trends |
| **Google Sheets Sync** | Auto-uploads data to Google Sheets for live integration |
| **Secure** | All sensitive API keys are stored in `.env` and not exposed in the repo |

---

## How It Works

### Data Sources (via APIs)
- **Financial Modeling Prep (FMP)** – Company valuation metrics
- **Alpha Vantage** – Daily stock prices
- **FRED** – CPI and Unemployment rate
- **NewsAPI** – Real-time news articles for sentiment
- **Google Sheets** – Centralized storage for Power BI connection

### Prediction Workflow
```text
Financials + Market Data + Macros + News ➜ Feature Engineering ➜ Random Forest Model ➜ Success Prediction
```
### Power BI Dashboard Insights

- High-quality vs risky M&A candidates
- Public/media sentiment score
- Undervaluation via PE Ratios
- Macro headwinds (CPI, Unemployment)
- Prediction distribution and trends

### Tech Stack

- Python (pandas, Numpy, sklearn, requests, dotenv, gspread)
- Google Sheets (via gspread)
- Power BI (Live dashboard connected to Google Sheet)
- Git + GitHub (Version control and hosting)

### Setup Instructions

1. Clone the Repository:

```bash

git clone https://github.com/YOUR_USERNAME/mandA-predictive-analytics.git
cd mandA-predictive-analytics
```
2. Install Dependencies:
```bash
pip install -r requirements.txt
```
3. Create a .env File with Your API Keys:
```bash
FMP_API_KEY=your_key  
FRED_API_KEY=your_key  
NEWS_API_KEY=your_key  
ALPHA_VANTAGE_API_KEY=your_key
```
4. Add Google Sheets Credentials File:
Place your manda-credentials.json in the root folder.

5. Run the Pipeline Script:
```bash
python main.py
```
6. Open the Power BI Dashboard:
- Double-click M & A analysis dashboard.pbix to launch the interactive dashboard in Power BI Desktop.
NOTE:
- This script fetches real-time data, runs the M&A prediction model, and updates the dashboard via Google Sheets automatically every 6 hours.



