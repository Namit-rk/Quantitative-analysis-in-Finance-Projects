## **1. Project Description: Smart Allocation of Funds in FAANG Companies – A Statistical Analysis**  

### **Overview**  
This project explores a **quantitative portfolio allocation strategy** applied to major tech stocks—**AAPL, GOOG, MSFT, AMZN, NFLX, and META**—from **2013 to 2020**. By using statistical and risk-based metrics, the study evaluates portfolio performance, balancing **return maximization and risk control**.In this project I walk Through my logic of using quantitative metrics to find an optimal aloocation of funds between the chosen stocks.

### **Key Highlights**  
- 📈 **Annual Return:** **23.53%** – Driven by the strong growth of FAANG stocks.  
- 📉 **Volatility:** **18.10%** – Reflecting the inherent risks of tech investments.  
- ⚖ **Sharpe Ratio:** **1.30** – Indicating a good risk-adjusted return.  
- 🔻 **Value at Risk (VaR 95%):** **-0.37%** – Measuring downside risk.  

### **Methodology**
1.  Stock Selection: Focused on high-growth FAANG stocks.
2.  Portfolio Construction: Allocated funds using quantitative metrics to optimize returns.
3.  Performance Evaluation: Assessed using Sharpe Ratio, VaR, and volatility.
4.  Risk Analysis: Measured downside risk and sector concentration effects.

---

## 2. 📈 Stock Market Crash Analysis using Network Science | India (2008 vs. 2020)

### 🔍 Overview
This project applies **network science** to analyze systemic behavior in the Indian stock market during two major crash events:
- 🦠 **Exogenous Crash** – COVID-19 pandemic (2020)
- 💥 **Indigenous Crash** – Global Financial Crisis (2008)

By constructing dynamic correlation networks of 200 major Indian stocks using `yfinance`, the project reveals structural differences between **external** and **internal** market crashes.


### 🛠️ Tools & Technologies
- **Python**: `pandas`, `numpy`, `yfinance`, `networkx`, `matplotlib`
- **Visualization**: `plotly`, `pyvis`
- **Network Analysis**: degree centrality, average correlation, network density
- **Community Detection**: Louvain algorithm
- **Jupyter Notebooks** for EDA & temporal analysis

### 📊 Key Features & Findings

- **📉 Crash Period Comparison**
  - **2020 COVID Crash (Exogenous):**  
    Network metrics (avg. correlation ↑ to 0.76, density ↑ to 0.73) spiked rapidly, signaling widespread panic and synchronized movement across sectors. The market restructured within 2–3 weeks.
  - **2008 Financial Crash (Indigenous):**  
    Network showed a slow buildup of connectivity (centrality ↑ from 0.38 to 0.63), indicating growing internal systemic stress. Recovery was slower and more fragmented.

- **🎯 Centrality Tracking & Market Leaders**  
  Identified key central stocks during stress periods:  
  - `JINDALSTEL.NS`, `VEDL.NS`, `BAJAJFINSV.NS` emerged as hubs in 2020  
  - `KOTAKBANK.NS`, `ICICIBANK.NS`, `DLF.NS` dominated during 2008  
  These stocks acted as potential **shock propagators or stabilizers**, depending on their sector role.

---

## 3. 📈 Stock Seasonality Prediction using Next-Gen Reservoir Computing

This project applies a **next-generation reservoir computing (RC)** algorithm to forecast the **seasonal component** of a stock price time series simulated using **Geometric Brownian Motion (GBM)**.
This work builds directly on techniques developed during my **Master’s thesis**, where I explored advanced RC frameworks for modeling nonlinear dynamical systems.

### 🧪 Methodology

* The stock price was **simulated using GBM**, a widely used stochastic model in quantitative finance.
* The resulting time series was **decomposed** into:

  * **Trend**
  * **Seasonal**
  * **Residual**
* Focused on **predicting the seasonal component**, which is often critical in short- to mid-term forecasting.
* Used a **next-gen reservoir computing algorithm** trained on past seasonal patterns to forecast **100 future time steps**.

### 📊 Results

* **Prediction Horizon:** 100 time steps (days)
* **Normalized MSE (NMSE):** 0.26
* The model was able to **accurately capture the underlying seasonal structure** despite the stochasticity of the GBM process.

