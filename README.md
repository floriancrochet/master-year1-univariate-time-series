# Univariate Time Series Projects
*Apply econometric analysis, simulation, and forecasting methods to univariate time series.*

| Topic | Description |
|-------|-------------|
| [**ARMA Modeling**](https://drive.google.com/file/d/1f8RKfl2IlKWku6SDho6zXx6anQDJXRU7/view?usp=drive_link) | Estimate and compare AR and ARMA models on CAC40 returns using OLS and maximum likelihood, with model selection based on AIC/BIC and diagnostic validation via Ljung-Box and Bartlett tests |
| [**Forecast Evaluation**](https://drive.google.com/file/d/1ALjuejyp1zKzP5QCd0AS1U_dGtCqBv3R/view?usp=drive_link) | Evaluate AR(1) forecasting models for wheat futures returns via rolling-windows, benchmarking against random walk models using Mincer-Zarnowitz and Diebold-Mariano tests |
| [**Unit Root Analysis**](https://drive.google.com/file/d/1QmdBvLZ--e_MzTy0FGoOjPMDLxj6cd3l/view?usp=drive_link) | Explore stochastic trends, unit roots, and spurious regressions via Monte Carlo simulations, and analyze U.S. GDP data using Dickey-Fuller and KPSS stationarity tests |
| [**Seasonality Modeling**](https://drive.google.com/file/d/1NW7GhvEW0F0v9NsUJB1jogwmfjpTEsls/view?usp=drive_link) | Simulate and estimate SARMA/SARIMA models applied to gas consumption and airport traffic data, comparing specifications based on residual diagnostics and information criteria |
| [**Stochastic Processes**](https://drive.google.com/file/d/1ermB-n0d533Lh_V_2GMQBygR_mn3Ufyp/view?usp=drive_link) | Analyze and simulate AR, MA, and ARMA processes, emphasizing polynomial stationarity conditions, characteristic roots, and ACF/PACF structural interpretations |

---

## 🎯 Overview
The ultimate goal of this repository is to showcase applied econometric methodologies and forecasting techniques on univariate time series through a collection of distinct analytical projects.

**Objectives**
- Model and analyze financial and economic univariate time series using ARMA-family models
- Simulate stochastic processes to assess trend, stationarity conditions, and spurious regressions
- Evaluate rolling-window forecasts using formal econometric tests
- Compare competing model specifications, including seasonal structures, using information criteria and diagnostics

---

## 🗄️ Data
- **Source:** Proprietary datasets (CAC40, U.S. GDP, gas consumption, airport traffic) and simulated data
- **Target Variable:** Financial returns, macroeconomic indicators, and simulated stochastic processes
- **Data Availability:** Provided in `data/` and generated in-script

---

## 🧠 Methodology
- **Theoretical Approach:** Box-Jenkins ARMA modeling, seasonal differencing, and stochastic trend analysis
- **Mathematical Framework:** Maximum Likelihood Estimation, Ordinary Least Squares, and Monte Carlo simulations
- **Evaluation Strategy:** Information criteria (AIC, BIC), residual diagnostics, Dickey-Fuller tests, and Diebold-Mariano tests

---

## ⚙️ Features
- **Estimate Models:** Estimate and compare AR and ARMA models using OLS and Maximum Likelihood
- **Model Seasonality:** Implement seasonal modeling with SARMA and SARIMA structures
- **Simulate Processes:** Conduct Monte Carlo simulations of stochastic processes and spurious regressions
- **Test Stationarity:** Perform stationarity testing via ADF, KPSS, and Dickey-Fuller methodologies
- **Evaluate Forecasts:** Implement rolling-window forecasting and evaluate using Mincer-Zarnowitz and Diebold-Mariano tests
- **Assess Diagnostics:** Conduct residual diagnostics using ACF, PACF, and Ljung-Box tests
- **Visualize Patterns:** Generate visualizations of trends, seasonality, and autocorrelation structures

---

## 🧰 Tech Stack
- **Language:** R
- **Numerical Computing & Data Manipulation:** tidyverse, openxlsx, readxl, purrr
- **Time Series Analysis:** forecast, tseries, urca, astsa, FinTS, TSA
- **Econometrics & Statistical Inference:** lmtest, sandwich, Metrics
- **Data Visualization:** ggplot2, gridExtra

---

## 📦 Installation
Clone the repository and install dependencies:

```bash
git clone https://github.com/floriancrochet/master-year1-univariate-time-series.git
cd master-year1-univariate-time-series
Rscript -e 'install.packages(c("tidyverse", "forecast", "tseries", "urca", "astsa", "ggplot2", "FinTS", "Metrics", "TSA", "purrr", "openxlsx", "readxl", "lmtest", "sandwich", "gridExtra"))'
```

---

## 💻 Usage Example

### Reproducing the Analysis / Execution Pipeline
```r
rmarkdown::render("arma_modeling/arma_modeling_project.qmd", output_format = "pdf")
rmarkdown::render("forecast_model_evaluation/forecast_evaluation_project.qmd", output_format = "pdf")
rmarkdown::render("nonstationarity_and_unit_roots/unit_roots_project.qmd", output_format = "pdf")
rmarkdown::render("seasonality_analysis/seasonality_project.qmd", output_format = "pdf")
rmarkdown::render("stochastic_processes_analysis/stochastic_processes_project.qmd", output_format = "pdf")
```

---

## 📂 Project Structure

```text
master-year1-univariate-time-series/
│
├── arma_modeling/                              # ARMA modeling of CAC40 returns
├── forecast_model_evaluation/                  # Rolling forecasts for wheat futures
├── nonstationarity_and_unit_roots/             # Unit root analysis and simulated trends
├── seasonality_analysis/                       # SARIMA modeling for gas consumption
├── stochastic_processes_analysis/              # Analytical study of ARMA processes
├── .gitignore
├── LICENSE
├── README.md
└── master-year1-univariate-time-series.Rproj
```

---

## 📈 Results

### Performance Metrics
*(No unified predictive performance metrics are formulated at the repository root; see sub-project reports for specific evaluations).*

### Key Findings
- **Model Selection:** AR(1) consistently outperforms higher-order AR models in CAC40 data, with AIC favoring ARMA(1,0).
- **Unit Roots:** Unit root presence is confirmed in the U.S. GDP series, highlighting trend non-stationarity.
- **Spurious Regressions:** Simulations of spurious regressions demonstrate rejection rates above 80%.
- **Seasonal Improvements:** Seasonal models significantly improve forecasting accuracy for gas consumption and airport traffic.
- **Forecasting Performance:** Rolling AR(1) models with 3-year estimation windows achieve the best predictive performance.
- **Benchmark Rejection:** Random walk forecasting benchmarks are systematically rejected across evaluations.
- **Stationarity Verification:** Polynomial root analysis confirms stationarity conditions for all simulated AR, MA, and ARMA processes.

---

## 📚 References
- Hamilton, *Time Series Analysis*
- Hyndman & Athanasopoulos, *Forecasting: Principles and Practice*
- Sévi, B. (2024). *Support de cours – Séries temporelles univariées (M1 ECAP)*
- Wooldridge, *Introductory Econometrics: A Modern Approach*

---

## 📜 License
This project is released under the MIT License.  
© 2025 Djayan Daëron, Arthur Ernoult de La Provôté, Isaline Hervé, Rémi Houssais, Achille Marteret, and Florian Crochet

---

## 👤 Authors
**Djayan Daëron**  
[GitHub Profile](https://github.com/Djayan-D)

**Arthur Ernoult de La Provôté**  
[GitHub Profile](https://github.com/ArthurEDLP)

**Isaline Hervé**  
[GitHub Profile](https://github.com/Isahrv)

**Rémi Houssais**  
[GitHub Profile](https://github.com/Remi-Houssais)

**Achille Marteret**  
[GitHub Profile](https://github.com/Achille-Marteret)

**Florian Crochet**  
[GitHub Profile](https://github.com/floriancrochet)

*Master 1 – Econometrics & Statistics, Applied Econometrics Track*

---

## 🤝 Acknowledgments
This work was conducted as part of the Univariate Time Series course, supervised by Benoît Sévi.
