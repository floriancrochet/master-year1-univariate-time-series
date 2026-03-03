# Time Series Forecasting Models Evaluation  
*Evaluate AR(1) forecasting models using rolling windows for wheat futures returns.*

[**Forecast Evaluation Report**](https://drive.google.com/file/d/1ALjuejyp1zKzP5QCd0AS1U_dGtCqBv3R/view?usp=drive_link) 

---

## 🎯 Overview
The ultimate goal of this project is to rigorously evaluate the predictive accuracy of autoregressive models against random walk benchmarks for financial futures.

**Objectives**
- Model financial returns using autoregressive (AR) processes
- Generate and compare 1-day and 5-day forecasts using rolling estimation windows
- Evaluate model accuracy via Mincer-Zarnowitz and Diebold-Mariano tests
- Compare alternative forecasting approaches with a random walk benchmark

---

## 🗄️ Data
- **Source:** Proprietary dataset (`wheat_futures_returns_2006_2022.xlsx`)
- **Target Variable:** Wheat futures returns (`return`)
- **Time Period / Size:** 2006–2022 (daily frequency)
- **Data Availability:** Provided in `data/`

---

## 🧠 Methodology
- **Theoretical Approach:** Autoregressive modeling (AR) and random walk benchmarking
- **Mathematical Framework:** Rolling-window estimation and forecast evaluation
- **Evaluation Strategy:** Mincer-Zarnowitz (unbiasedness) and Diebold-Mariano (MSE, MAD, Quad-Quad loss) tests

---

## ⚙️ Features
- **Process Data:** Preprocess and visualize daily wheat futures returns from 2006 to 2022
- **Estimate Models:** Specify and estimate AR(1) and random walk baseline models
- **Generate Forecasts:** Compute 1-day and 5-day ahead forecasts using 10-year and 3-year rolling windows
- **Evaluate Accuracy:** Implement Mincer-Zarnowitz and Diebold-Mariano statistical tests on forecast errors

---

## 🧰 Tech Stack
- **Language:** R
- **Numerical Computing & Data Manipulation:** tidyverse, readxl
- **Time Series Analysis:** tseries, forecast
- **Econometrics & Statistical Inference:** lmtest, sandwich
- **Data Visualization:** gridExtra

---

## 📦 Installation
Clone the repository and install dependencies:

```bash
git clone https://github.com/floriancrochet/master-year1-univariate-time-series.git
cd master-year1-univariate-time-series/forecast_model_evaluation
Rscript -e 'install.packages(c("tidyverse", "readxl", "tseries", "forecast", "lmtest", "sandwich", "gridExtra"))'
```

---

## 💻 Usage Example

### Reproducing the Analysis / Execution Pipeline
```r
rmarkdown::render("forecast_evaluation_project.qmd", output_format = "pdf")
```

---

## 📂 Project Structure

```text
forecast_model_evaluation/
│
├── data/                             # Wheat futures data (2006–2022)
├── report/                           # Compiled analysis report
├── forecast_evaluation_project.qmd   # Main source code for forecast evaluation
└── README.md
```

---

## 📈 Results

### Performance Metrics
| Model | Diebold-Mariano vs Baseline | Mincer-Zarnowitz Unbiasedness |
|-------|------------------------------|-----------------------------|
| A10_1 | Outperforms Random Walk | Unbiased |
| A3_1 | Outperforms Random Walk | Unbiased |
| A3_5 | Outperforms Random Walk | Unbiased |

### Key Findings
- **Stationarity:** The ADF test confirms the stationarity of the return series.
- **Model Selection:** The AR(1) model was selected based on ACF and PACF analysis.
- **Forecast Unbiasedness:** Mincer-Zarnowitz test results show that A10_1, A3_1, and A3_5 forecasts are unbiased.
- **Predictive Superiority:** Diebold-Mariano test results demonstrate that the AR(1) models consistently outperform the random walk benchmark, with A3_1 slightly outperforming A10_1.

---

## 📚 References
- Hamilton, *Time Series Analysis*  
- Hyndman & Athanasopoulos, *Forecasting: Principles and Practice*  
- Sévi, B. (2024). *Support de cours – Séries temporelles univariées (M1 ECAP)*
- Wooldridge, *Introductory Econometrics: A Modern Approach*  

---

## 📜 License
This project is released under the MIT License.  
© 2025 Rémi Houssais and Florian Crochet

---

## 👤 Authors
**Rémi Houssais**  
[GitHub Profile](https://github.com/Remi-Houssais)

**Florian Crochet**  
[GitHub Profile](https://github.com/floriancrochet)

*Master 1 – Econometrics & Statistics, Applied Econometrics Track* 

---

## 🤝 Acknowledgments
This work was conducted as part of the Univariate Time Series course, supervised by Benoît Sévi.
