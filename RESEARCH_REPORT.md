# Research Report: The Geometry of Risk
**Mapping Systemic Fragility via Spectral Decomposition**

**Date:** November 2025
**Domain:** Quantitative Macro Strategy

---

## 1. Abstract
The structural promise of Modern Portfolio Theory (MPT) is diversification: the idea that uncorrelated assets protect capital during volatility. This research challenges that assumption for the 2025 macro regime.

Using **Principal Component Analysis (PCA)** and **PageRank (Eigenvector Centrality)**, we decoded the hidden correlation structure of global markets. Our findings indicate a fundamental regime shift: Global markets have re-coupled around a single driver—**Energy Input Costs**—creating a "Supply-Side" regime where geographic diversification provides little to no structural hedge.

---

<img width="495" height="318" alt="image" src="https://github.com/user-attachments/assets/3b98e53f-528a-4cf0-9000-69749c605836" />


## 2. The Macro Signal: The "Oil Shock" Regime
To identify the primary driver of global asset returns, we performed a Spectral Decomposition on a multi-asset covariance matrix (Indices, Commodities, Rates).

### Key Finding: The "Factor 1" Dominance
The First Principal Component (PC1)—which represents "Global Beta"—showed a factor loading of **0.88** for Brent Crude Oil. This is a statistical anomaly; typically, equities and commodities exhibit lower correlation.

* **Interpretation:** The global equity market is currently trading as a levered derivative of Energy prices.
* **The Signal:** Our **Rolling Absorption Ratio (60-Day Log Returns)** identified a critical turning point. After a period of decoupling in Q3 2025 (where idiosyncratic stock picking worked), the system has re-synchronized.
* **Current State:** The Absorption Ratio is rising, signaling that systemic fragility is returning.

<img width="515" height="331" alt="image" src="https://github.com/user-attachments/assets/d57f2ed9-2781-44b2-a679-d3b0aaf0b18b" />


---

<img width="495" height="432" alt="image" src="https://github.com/user-attachments/assets/2be82b69-98c1-44be-a797-50681f2cf952" />


## 3. The Micro Structure: The "Nervous System" of the S&P 500
Moving from the macro view to the micro view, we mapped the S&P 500 correlation network using **PageRank (Eigenvector Centrality)**. This algorithm identifies which stocks are the "transmission hubs" of risk.

### Insight A: The Credit Dependency
While media attention focuses on "Magnificent 7" AI stocks, the mathematical center of the S&P 500 is **Visa (V)** and **Mastercard (MA)**.
* **Implication:** The market structure is chemically dependent on **Consumer Credit Velocity**. A shock to payment processors will propagate faster and wider through the network than a shock to the AI vertical.

### Insight B: The Utility/Tech Merger
We observed a **96% correlation** between the Utilities and Technology sectors.
* **Implication:** Utilities have mathematically transitioned from "Defensive Hedges" to "AI Power Proxies." Portfolios holding Utilities as a safety trade are inadvertently doubling down on Tech Beta.

---

<img width="700" height="140" alt="image" src="https://github.com/user-attachments/assets/42a5758b-6c26-4b79-948f-d4b916b7bb97" />


## 4. The Global Myth: There is No Decoupling
A common thesis in 2025 is that China is insulated by state policy or that Europe is distinct due to luxury/industrials. We tested this by calculating the **Cumulative PageRank** of the "Energy Cluster" (Commodities + Majors + Drillers) for each region.

The results show massive convergence:

| Region | Energy Cluster Influence | Dominant Player | Risk Profile |
| :--- | :--- | :--- | :--- |
| **China (Shanghai)** | **45.4%** | PetroChina | **High.** Index behaves as an Energy Proxy despite State Policy. |
| **Europe (Stoxx)** | **41.9%** | Eni SpA | **High.** Levered play on global input costs. |
| **Japan (Nikkei)** | **39.9%** | ENEOS Holdings | **High.** Driven by Refiner margins and import costs. |

**Conclusion:** A global portfolio allocated across the US, Europe, and China effectively holds a massive, unhedged short position on Oil volatility.

---

<img width="495" height="254" alt="image" src="https://github.com/user-attachments/assets/b650a5dc-febe-4c3b-a0c3-3fc280d8325d" />


## 5. Validation: The "Volatility Cluster" (November 2025)
The robustness of this model was validated by the violent price action of late 2025.

**The Event:**
In November, betting markets surged to price an **81% probability of rate cuts**. Despite this, AI/Big Tech stocks suffered a **~30% drawdown**, followed immediately by a sharp **5-day recovery**.

**The Model Validation:**
Crucially, our **Rolling Absorption Ratio** spiked during both the crash *and* the recovery.
* **The "Whiplash" Signal:** The market exhibited extreme bi-directional volatility.
* **Why this matters:** In a healthy market, a recovery is usually driven by specific earnings (Idiosyncratic). However, the rising Absorption Ratio during the bounce indicates that the recovery was **Systemic**. Capital is sloshing violently in and out of the sector based entirely on macro liquidity flows.
* **Conclusion:** The recent 5-day recovery is not a return to stability; it is a symptom of **Fragility**. The market has entered a regime of "Volatility Clustering," where asset prices are no longer anchoring to fundamentals but are reacting with extreme sensitivity (High Beta) to daily shifts in the bond market.

---

## 6. Investment Conclusion
The data suggests that the window for idiosyncratic Alpha (Stock Picking) is closing. The market has reorganized around two systemic poles: **Energy Input Costs** and **Interest Rate Sensitivity**.

**Actionable Insights:**
1.  **Avoid False Diversification:** Owning Europe and Japan does not hedge US Energy risk; they are mathematically identical trades.
2.  **Monitor the Absorption Ratio:** As long as this metric is rising, increase cash or uncorrelated hedges (e.g., Volatility).
3.  **Respect the Bond Yield:** The equity market is currently a function of the 10-Year Treasury. Until the "Duration Trap" resolves, Tech volatility will remain elevated.

---

### *Technical Appendix*
* **Data Source:** Yahoo Finance API (Daily Adjusted Close, Log-Returns).
* **Algorithms:** Principal Component Analysis (SVD), PageRank ($d=0.85$).
* **Codebase:** Available in the root directory of this repository.
