# 🏦 Investor Analysis AI-Engine

An AI-powered, self-service business intelligence dashboard built with **Streamlit**, **Pandas**, and the **Google GenAI SDK**. 

This application allows business and MIS analysts to upload raw datasets (Excel/CSV) and query them using natural language. The engine generates aggregated cross-tabulations, visual charts, deep numerical trend breakdowns, and analytical caveats while keeping underlying row-level data strictly local.

---

## 🌟 Key Features

* **Natural Language to Analytics:** Ask business questions in plain English (e.g., *"Show disbursement breakdown across branches"* or *"Delinquency rates across ticket sizes"*).
* **Guaranteed Dual Output:** Automatically generates both an aggregated cross-tab/pivot table and an accompanying visual chart (bar or line chart) for every query.
* **Executive Summaries & Caveats:** Produces detailed writeups that highlight baseline metrics, percentage variances, statistical skews, and concentration risks.
* **Privacy-First Architecture:** Only column headers and summary statistics are passed to the AI model. Row-level transaction data stays inside your runtime environment.
* **Failover & Auto-Retry:** Integrated exponential backoff handling to prevent service interruptions during model demand spikes.
* **Query Session History:** Keeps an audit trail of executed queries and key findings within the session.

---

## 📋 Project Structure

```text
├── app.py                     # Main Streamlit application (or Investors_Analysis_Utility.py)
├── requirements.txt           # Python dependencies
├── README.md                  # Project documentation
└── .streamlit/
    └── secrets.toml           # Local secrets storage (DO NOT commit to Git)
