# Analysis of Non-Stationarity and Unit Roots  
*Analyze time series stationarity, stochastic trends, and spurious regression using R.*

[**Unit Roots Analysis Report**](https://drive.google.com/file/d/1QmdBvLZ--e_MzTy0FGoOjPMDLxj6cd3l/view?usp=drive_link)

---

## 🎯 Overview
**Objectives**
- Understand the difference between deterministic and stochastic trends
- Illustrate permanent vs. transitory shocks in AR(1) processes
- Detect spurious regressions in non-stationary data
- Estimate and interpret Dickey-Fuller and KPSS tests
- Apply the methodology to real economic data

---

## 🗄️ Data
- **Source:** Proprietary dataset (`GDP_US_1990_2023.RData`)
- **Time Period / Size:** 1990–2023 
- **Target Variable:** U.S. GDP
- **Data Availability:** Provided in `data/`

---

## 🧠 Methodology
- **Theoretical Approach:** Monte Carlo simulations and spurious regression analysis
- **Mathematical Framework:** Autoregressive modeling (AR) and Dickey-Fuller distributions
- **Evaluation Strategy:** Stationarity testing (Dickey-Fuller, KPSS) and critical value estimation

---

## ⚙️ Features
- **Simulate Processes:** Simulate AR(1) processes with and without unit roots
- **Compare Trends:** Visually compare deterministic (TS) vs. stochastic (DS) trends
- **Estimate Values:** Compute critical values for the Dickey-Fuller test via Monte Carlo estimation
- **Analyze Empirically:** Conduct empirical analysis of the U.S. GDP series (1990–2023)
- **Identify Spuriousness:** Detect spurious regressions through large-scale simulations

---

## 🧰 Tech Stack
- **Language:** R
- **Data Manipulation:** tidyverse, openxlsx
- **Modeling / ML:** urca, forecast, tseries

---

## 📦 Installation
Clone the repository and install dependencies:

```bash
git clone https://github.com/floriancrochet/master-year1-univariate-time-series.git
cd master-year1-univariate-time-series/nonstationarity_and_unit_roots
Rscript -e 'install.packages(c("tidyverse", "openxlsx", "urca", "forecast", "tseries"))'
```

---

## 💻 Usage Example

### Reproducing the Analysis / Execution Pipeline
```r
rmarkdown::render("unit_roots_project.qmd", output_format = "pdf")

simulate_ar1(phi = 0.9, choc_value = 20, choc_time = 100, n = 200)
```

---

## 📂 Project Structure

```text
nonstationarity_and_unit_roots/
│
├── data/                    # U.S. GDP dataset (1990–2023)
├── report/                  # Rendered analysis report
├── unit_roots_project.qmd   # Main source code
└── README.md
```

---

## 📈 Results

### Key Findings
- **Transitory Shocks:** For ϕ < 1, shocks are transitory and the process returns to its mean
- **Permanent Shocks:** For ϕ = 1, shocks have permanent effects, confirming a random walk behavior
- **Spurious Regression:** Tests show rejection rates far above 5% (≈83-88%), highlighting false correlations
- **Monte Carlo Precision:** The simulation of Dickey-Fuller statistics accurately reproduces theoretical critical values
- **Empirical Stationarity:** The U.S. GDP (1990-2023) exhibits a non-stationary trend, with unit root confirmed by Dickey-Fuller and contradicted by KPSS tests

---

## 📚 References
- Hyndman & Athanasopoulos, *Forecasting: Principles and Practice*  
- Hamilton, *Time Series Analysis*  
- Wooldridge, *Introductory Econometrics: A Modern Approach*  
- Sévi, B. (2024). *Support de cours – Séries temporelles univariées (M1 ECAP)*

---

## 📜 License
This project is released under the MIT License.  
© 2025 Achille Marteret and Florian Crochet

---

## 👤 Authors
**Achille Marteret**  
[GitHub Profile](https://github.com/Achille-Marteret) 

**Florian Crochet**  
[GitHub Profile](https://github.com/floriancrochet)

*Master 1 – Econometrics & Statistics, Applied Econometrics Track* 

---

## 🤝 Acknowledgments
This work was conducted as part of the Univariate Time Series course, supervised by Benoît Sévi.
