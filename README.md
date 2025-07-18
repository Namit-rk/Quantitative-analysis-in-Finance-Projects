
## 1. Markowitz Portfolio Optimization & Backtesting

This project applies **Modern Portfolio Theory (MPT)** to construct and evaluate an optimized portfolio of 5 selected U.S. stocks. The goal is to minimize portfolio risk for a given expected return and compare the performance of the optimized portfolio against an **equally-weighted portfolio** and the **S\&P 500 index**.

### 🔧 Methodology

1. **Stock Selection**
   Five stocks were selected based on their strong performance up to 2023. After 2023, one stock underperformed while another showed exponential growth — introducing realistic variance and stress-testing the optimization strategy.

2. **Expected Return & Covariance Estimation**

   * Computed **log returns** on pre-2023 data.
   * Estimated **expected returns (μ)** and **covariance matrix (Σ)**.

3. **Portfolio Optimization**

   * Used **Markowitz mean-variance optimization**.
   * Constraints:

     * Fully invested (sum of weights = 1)
     * Long-only (no short-selling)
     * Expected return ≥ a target threshold
   * Visualized the **efficient frontier** and identified the **optimal Sharpe ratio portfolio**.

4. **Backtesting (2023–2025)**

   * Tested performance of:

     * The **optimized portfolio**
     * An **equal-weighted portfolio** (1/N allocation)
     * The **S\&P 500 index** (`^GSPC`) as a benchmark

5. **Performance Metrics**
   For each portfolio:

   * Cumulative Return
   * Annualized Return (CAGR)
   * Sharpe Ratio
   * Maximum Drawdown
   * Conditional Value at Risk (CVaR) at 95%

### 📊 Results Summary

| Metric            | Optimized Portfolio | Equal-Weighted | S\&P 500 |
| ----------------- | ------------------- | -------------- | -------- |
| Cumulative Return | 84.8%               | 107.7%         | 54.4%    |
| Annualized Return | 36.3%               | 44.6%          | 24.5%    |
| Sharpe Ratio      | 1.51                | 1.31           | 1.20     |
| Max Drawdown      | -14.1%              | -31.1%         | -10.2%   |
| CVaR (95%)        | -3.0%               | -3.9%          | -1.7%    |

* ✅ **Optimized portfolio** showed better risk-adjusted performance with lower drawdown.
* ⚖️ **Equal-weighted portfolio** had slightly higher raw returns, but at significantly higher risk.
* 🆚 Both portfolios outperformed the **S\&P 500** in return and Sharpe ratio.

### 🧠 Key Insights

* Optimization via MPT can help create **more stable portfolios** with improved downside protection.
* **Equal weighting** may offer high returns in certain environments, but risk can be substantially higher.
* **Risk metrics** like Sharpe, CVaR, and Max Drawdown give deeper insights than return alone.

---

## **2. Project Description: Smart Allocation of Funds in FAANG Companies – A Statistical Analysis**  

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

