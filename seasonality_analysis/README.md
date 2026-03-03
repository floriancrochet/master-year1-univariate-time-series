# Seasonal Time Series Modeling  
*Simulate, estimate, and evaluate SARMA and SARIMA models for seasonal time series.*

[**Seasonality Modeling Report**](https://drive.google.com/file/d/1NW7GhvEW0F0v9NsUJB1jogwmfjpTEsls/view?usp=drive_link)

---

## 🎯 Overview
The ultimate goal of this project is to model complex seasonal dynamics in economic series using advanced seasonal forecasting architectures.

**Objectives**
- Simulate and analyze seasonal ARMA models with different periodicities
- Fit SARIMA models and evaluate residual diagnostics
- Apply seasonal time series analysis to real economic data
- Compare alternative model specifications and validate via ACF/PACF and Ljung-Box tests

---

## 🗄️ Data
- **Source:** Proprietary datasets (`fr_gas_consumption_monthly.RData`, `tls_monthly_passengers.rda`)
- **Target Variable 1:** French natural gas consumption (2008–2024)
- **Target Variable 2:** Toulouse-Blagnac airport traffic (1993–2008)
- **Frequency:** Monthly
- **Data Availability:** Provided in `data/`

---

## 🧠 Methodology
- **Theoretical Approach:** Seasonal Autoregressive Moving Average (SARMA / SARIMA) modeling
- **Mathematical Framework:** Box-Jenkins approach with seasonal differencing
- **Evaluation Strategy:** Information criteria (AIC/BIC) and residual analysis (ACF/PACF, Ljung-Box tests)

---

## ⚙️ Features
- **Implement Formulations:** Implement SARMA(p,q)(P,Q)[s] and equivalent ARMA(p,q) formulations
- **Utilize Libraries:** Use `astsa`, `forecast`, and `tidyverse` for simulation and model estimation
- **Perform Diagnostics:** Leverage ACF, PACF, and white-noise testing diagnostic tools
- **Conduct Analysis:** Compare models based on AIC/BIC and residual structure
- **Demonstrate Application:** Deliver real-world case studies demonstrating seasonality and trend modeling

---

## 🧰 Tech Stack
- **Language:** R
- **Numerical Computing & Data Manipulation:** tidyverse
- **Time Series Analysis:** astsa, forecast

---

## 📦 Installation
Clone the repository and install dependencies:

```bash
git clone https://github.com/floriancrochet/master-year1-univariate-time-series.git
cd master-year1-univariate-time-series/seasonality_analysis
Rscript -e 'install.packages(c("astsa", "forecast", "tidyverse"))'
```

---

## 💻 Usage Example

### Reproducing the Analysis / Execution Pipeline
```r
rmarkdown::render("seasonality_project.qmd", output_format = "pdf")
```

---

## 📂 Project Structure

```text
seasonality_analysis/
│
├── data/                    # Gas consumption and airport traffic datasets
├── report/                  # Rendered analysis report
├── seasonality_project.qmd  # Main source code
└── README.md
```

---

## 📈 Results

### Performance Metrics
| Dataset | Best Model | Validation Method |
|---------|-----------|-------------------|
| Gas Consumption | SARIMA(2,0,0)(0,2,4)[12] | Lowest AIC/BIC, Box-Ljung (p > 0.05) |
| Toulouse Airport | SARIMA(3,0,2)(1,1,1)[12] | Residual Diagnostics |
| Simulated Data | SARMA(1,2)(1,1)[4] | Residual Diagnostics |

### Key Findings
- **Simulations:** SARMA(1,2)(1,1)[4], SARMA(1,1)(1,1)[6], and SARMA(2,0)(0,1)[12] were simulated successfully.
- **Equivalent Forms:** Equivalent non-seasonal ARMA forms were derived, demonstrating theoretical equivalence.
- **Residual Behavior:** Residual diagnostics confirmed white-noise behavior in all final models.
- **Gas Seasonality:** French gas consumption exhibited strong annual seasonality with no trend.
- **Airport Trend:** Toulouse airport traffic showed a trend break in 2001 due to external shocks (9/11), requiring separated modeling.

---

## 📚 References
- Hamilton, *Time Series Analysis*  
- Hyndman & Athanasopoulos, *Forecasting: Principles and Practice*  
- Sévi, B. (2024). *Support de cours – Séries temporelles univariées (M1 ECAP)*
- Wooldridge, *Introductory Econometrics: A Modern Approach*  

---

## 📜 License
This project is released under the MIT License.  
© 2025 Isaline Hervé and Florian Crochet

---

## 👤 Authors
**Isaline Hervé**  
[GitHub Profile](https://github.com/Isahrv)  

**Florian Crochet**  
[GitHub Profile](https://github.com/floriancrochet)

*Master 1 – Econometrics & Statistics, Applied Econometrics Track*  

---

## 🤝 Acknowledgments
This work was conducted as part of the Univariate Time Series course, supervised by Benoît Sévi.
