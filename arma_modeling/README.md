# ARMA Modeling  
*Analyze and forecast financial time series using autoregressive and moving average models.*

[**ARMA Modeling Report**](https://drive.google.com/file/d/1f8RKfl2IlKWku6SDho6zXx6anQDJXRU7/view?usp=drive_link)

---

## 🎯 Overview
The ultimate goal of this project is to model financial return dynamics by identifying the optimal autoregressive moving average specification.

**Objectives**
- Estimate autoregressive models via OLS and maximum likelihood
- Compare model performance systematically using AIC and BIC
- Identify the optimal ARMA specification for financial return series
- Conduct residual diagnostics to validate model adequacy

---

## 🗄️ Data
- **Source:** Proprietary dataset (`CAC40_2010_2023.csv`)
- **Target Variable:** CAC40 index returns (`Rendement_t`)
- **Key Predictors / Features:** Lagged returns (`Rendement_t_1`, `Rendement_t_2`)
- **Preprocessing:** Computed logarithmic returns and first differences to achieve stationarity
- **Data Availability:** Provided in `data/`

---

## 🧠 Methodology
- **Theoretical Approach:** Box-Jenkins ARMA modeling framework
- **Mathematical Framework:** Ordinary Least Squares (OLS) and Maximum Likelihood Estimation (ARIMA)
- **Evaluation Strategy:** Information criteria comparison (AIC, BIC) and residual testing

---

## ⚙️ Features
- **Estimate Models:** Compute AR(1) and AR(2) models via regression and maximum likelihood functions
- **Compare Criteria:** Automate ARMA model selection based on AIC and BIC minimization
- **Visualize Autocorrelation:** Plot returns, ACF, and PACF to assess stationarity
- **Assess Diagnostics:** Conduct statistical tests on residuals to confirm model specification

---

## 🧰 Tech Stack
- **Language:** R
- **Numerical Computing & Data Manipulation:** tidyverse
- **Time Series Analysis:** forecast
- **Econometrics & Statistical Inference:** lmtest
- **Data Visualization:** ggplot2

---

## 📦 Installation
Clone the repository and install dependencies:

```bash
git clone https://github.com/floriancrochet/master-year1-univariate-time-series.git
cd master-year1-univariate-time-series/arma_modeling
Rscript -e 'install.packages(c("tidyverse", "forecast"))'
```

---

## 💻 Usage Example

### Reproducing the Analysis / Execution Pipeline
```r
rmarkdown::render("arma_modeling_project.qmd", output_format = "pdf")
```

---

## 📂 Project Structure

```text
arma_modeling/
│
├── data/                      # Raw CAC40 dataset
├── report/                    # Compiled analysis report
├── arma_modeling_project.qmd  # Source code for ARMA modeling
└── README.md
```

---

## 📈 Results

### Performance Metrics
| Model | AIC | BIC |
|-------|-----|-----|
| AR(2) | -2870.45 | -2852.36 |
| ARMA(1,0) | **-2872.37** | **-2858.80** |

### Key Findings
- **Model Selection:** The AIC criterion identified ARMA(1,0) as the optimal model, while BIC favored ARMA(0,0).
- **Diagnostic Validation:** Ljung-Box and Bartlett tests demonstrated that the ARMA(1,0) model was well-specified.
- **OLS Significance:** OLS estimation confirmed the statistical significance of the AR(1) autoregressive coefficient.

---

## 📚 References
- Hamilton, *Time Series Analysis*  
- Hyndman & Athanasopoulos, *Forecasting: Principles and Practice*  
- Sévi, B. (2024). *Support de cours – Séries temporelles univariées (M1 ECAP)*  
- Wooldridge, *Introductory Econometrics: A Modern Approach*  

---

## 📜 License
This project is released under the MIT License.  
© 2025 Arthur Ernoult de La Provôté and Florian Crochet 

---

## 👤 Authors
**Arthur Ernoult de La Provôté**  
[GitHub Profile](https://github.com/ArthurEDLP)  

**Florian Crochet**  
[GitHub Profile](https://github.com/floriancrochet)

*Master 1 – Econometrics & Statistics, Applied Econometrics Track*

---

## 🤝 Acknowledgments
This work was conducted as part of the Univariate Time Series course, supervised by Benoît Sévi.
