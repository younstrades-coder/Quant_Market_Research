# The Geometry of Risk: A Spectral Decomposition of Global Markets
### *Mapping Systemic Fragility via Eigen-Centrality and Rolling Absorption Ratios*

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Finance](https://img.shields.io/badge/Domain-Quant%20Finance-green)
![Math](https://img.shields.io/badge/Math-Linear%20Algebra%20%7C%20Graph%20Theory-orange)
![Status](https://img.shields.io/badge/Status-Research%20Complete-brightgreen)

## 📉 Executive Summary
Modern Portfolio Theory (MPT) relies on the assumption of structural diversification. However, in "supply-side" macro regimes, asset correlations often converge, rendering traditional diversification ineffective. 

This research project applies **Linear Algebra (Eigen-Decomposition)** and **Network Theory (PageRank)** to decode the hidden market structure of the 2024-2025 macro regime. By moving beyond static correlation matrices to dynamic **Spectral Decomposition**, this study identifies a fundamental **Regime Shift**: the transition from an idiosyncratic "Stock Picker's Market" to a unified **"Petro-Economy"** driven by energy input costs and interest rate sensitivity.

---

## 🧠 Theoretical Framework & Skills Applied

This project synthesizes concepts from advanced mathematics, macroeconomics, and quantitative finance.

### 1. Mathematical & Computational
* **Principal Component Analysis (PCA):** utilized `Singular Value Decomposition (SVD)` to isolate latent market drivers.
    * *Application:* Calculated "Global Beta" by extracting the First Principal Component (PC1) from a multi-asset covariance matrix.
* **Graph Theory & Centrality:** modeled the S&P 500 as a weighted undirected graph.
    * *Application:* Applied **PageRank (Eigenvector Centrality)** to identify transmission nodes ("Systemic Hubs") within the correlation network.
    * *Application:* Constructed **Minimum Spanning Trees (MST)** to visualize the "backbone" of market structure, filtering out noise.
* **Rolling Window Statistics:** Implemented custom rolling PCA algorithms to generate time-series signals for systemic risk.

### 2. Financial & Economic
* **Systemic Risk Modeling:** Implemented the **Absorption Ratio** (Kritzman et al.) to quantify market fragility.
* **Regime Identification:** Diagnosed the shift from "Demand-Pull" (Growth) to "Supply-Push" (Cost) inflation regimes.
* **Asset Pricing Theory:** Analyzed "Duration Risk" in equities, modeling Big Tech as long-duration bond proxies sensitive to the 10-Year Treasury Yield.
* **Cross-Asset Correlation:** Mapped the transmission mechanism between Commodities (Brent Crude), Sovereign Bonds (US 10Y), and Global Equities.

---

## 🛠 Methodology & Research Pipeline

The analysis follows a strict Top-Down quantitative workflow:

### Phase 1: The Macro Layer (Global Beta)
* **Input:** Log-returns of major indices (SPX, STOXX50, N225, SHCOMP), Commodities (Oil, Gold), and Rates (TNX).
* **Technique:** Spectral Decomposition of the Global Correlation Matrix.
* **Finding:** **Brent Crude Oil** emerged as the dominant factor loading (**0.88**) on PC1.
* **Signal:** The **Rolling Absorption Ratio (60-Day)** identified a "V-Shaped" recovery in systemic risk, signaling a re-coupling of global assets around energy prices in Q4 2025.

### Phase 2: The Meso Layer (Sector Rotation)
* **Input:** Top 100 constituents of the S&P 500.
* **Technique:** 3D PCA Scatter Plots.
* **Finding:** A structural merger of **Utilities** and **Technology** sectors (**96% correlation**).
* **Insight:** Utilities have transitioned from "Defensive Hedges" to "AI Power Proxies," effectively increasing the aggressive beta of standard diversified portfolios.

### Phase 3: The Micro Layer (Systemic Nodes)
* **Input:** Adjacency matrix of S&P 500 constituents (Threshold > 0.7).
* **Technique:** Google PageRank Algorithm ($d=0.85$).
* **Finding:** While media focus remains on "Mag 7" Tech stocks, the mathematical "Center of Gravity" is **Visa (V)** and **Mastercard (MA)**.
* **Implication:** The US market structure is chemically dependent on **Consumer Credit Velocity**. Shocks to the payment rail system propagate faster and wider than idiosyncratic tech volatility.

### Phase 4: The Global "Petro-Sensitivity" Test
* **Input:** Cumulative PageRank scoring of Energy Clusters across Europe, Japan, and China.
* **Finding:** Global markets exhibit "Convergent Fragility." Despite geopolitical differences, all major regions show >40% structural sensitivity to the Energy complex.

| Region | Energy Cluster Influence | Dominant Player | Risk Profile |
| :--- | :--- | :--- | :--- |
| **China (Shanghai)** | **45.4%** | PetroChina | **High.** Index behaves as an Energy Proxy despite State Policy buffers. |
| **Europe (Stoxx)** | **41.9%** | Eni SpA | **High.** Levered play on global input costs. |
| **Japan (Nikkei)** | **39.9%** | ENEOS Holdings | **High.** Driven by Refiner margins and import costs. |

---

## 🚦 Scenario Analysis & Validation

The project validates the "Fragility" thesis by reconciling mathematical signals with recent price action:

* **The Signal:** The Absorption Ratio spiked in late Q4 2025, while Rate Cut probabilities collapsed (<40%).
* **The Price Action:** Big Tech suffered a ~30% drawdown while the broader index remained resilient.
* **The Conclusion:** The market is caught in a **"Duration Trap."** With the "Fed Put" removed, capital crowded into "Bond Proxies" (Cash-Rich Tech), creating extreme concentration. The subsequent drawdown validates the model's signal that **Liquidity Stress** had returned, forcing a mechanical de-leveraging of long-duration assets.

---

## 💻 Tech Stack

* **Data Acquisition:** `yfinance` (Yahoo Finance API)
* **Data Processing:** `pandas`, `numpy` (Log-return normalization, Rolling Windows)
* **Linear Algebra:** `scikit-learn` (PCA), `numpy.linalg` (SVD, Eigenvalues)
* **Network Analysis:** `networkx` (Graph construction, PageRank, Minimum Spanning Trees)
* **Visualization:** `matplotlib`, `seaborn` (Heatmaps, 3D Plots, Time-Series Analysis)

## 🚀 How to Run

1.  Clone the repository:
    ```bash
    git clone [https://github.com/yourusername/geometry-of-risk.git](https://github.com/yourusername/geometry-of-risk.git)
    ```
2.  Install dependencies:
    ```bash
    pip install pandas numpy yfinance scikit-learn networkx matplotlib seaborn
    ```
3.  Run the Jupyter Notebook:
    ```bash
    jupyter notebook geometry_of_risk.ipynb
    ```

---

## 📜 Disclaimer
*This project is for educational and research purposes only. It demonstrates the application of quantitative methods to financial data and does not constitute investment advice.*
