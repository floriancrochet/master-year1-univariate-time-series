# ARMA Process Simulation and Stationarity Analysis  
*Analyze ARMA process stationarity and autocorrelation patterns using R.*

[**Stochastic Processes Report**](https://drive.google.com/file/d/1ermB-n0d533Lh_V_2GMQBygR_mn3Ufyp/view?usp=drive_link)

---

## 🎯 Overview
The ultimate goal of this project is to systematically explore the theoretical stationarity boundaries and autocorrelation structures of simulated stochastic processes.

**Objectives**
- Express ARMA processes using the lag operator L and determine their characteristic equations
- Assess weak stationarity conditions for each process
- Simulate and visualize AR, MA, and ARMA processes to analyze ACF and PACF patterns
- Ensure clarity, reproducibility, and analytical precision in time series modeling

---

## 🗄️ Data
- **Target Variable:** Simulated AR, MA, and ARMA processes
- **Data Availability:** Generated in-script via `rnorm()`

---

## 🧠 Methodology
- **Theoretical Approach:** Stochastic process simulation and characteristic root analysis
- **Mathematical Framework:** Linear difference equations and lag operators
- **Evaluation Strategy:** Stationarity verification via polynomial roots and visual inspection of ACF/PACF

---

## ⚙️ Features
- **Analyze Stationarity:** Analyze ARMA(p,q) stationarity using characteristic roots
- **Simulate Processes:** Simulate stochastic processes with controlled random seeds for reproducibility
- **Generate Plots:** Generate ACF and PACF plots automatically
- **Utilize Libraries:** Use ggplot2 and forecast for high-quality visualizations
- **Maintain Structure:** Maintain consistent structure across exercises for methodological transparency

---

## 🧰 Tech Stack
- **Language:** R
- **Numerical Computing & Data Manipulation:** purrr
- **Time Series Analysis:** tseries, forecast, FinTS, TSA
- **Econometrics & Statistical Inference:** Metrics
- **Data Visualization:** ggplot2

---

## 📦 Installation
Clone the repository and install dependencies:

```bash
git clone https://github.com/floriancrochet/master-year1-univariate-time-series.git
cd master-year1-univariate-time-series/stochastic_processes_analysis
Rscript -e 'install.packages(c("tseries", "forecast", "FinTS", "Metrics", "TSA", "ggplot2", "purrr"))'
```

---

## 💻 Usage Example

### Reproducing the Analysis / Execution Pipeline
```r
rmarkdown::render("stochastic_processes_project.qmd", output_format = "pdf")
```

---

## 📂 Project Structure

```text
stochastic_processes_analysis/
│
├── report/                           # Rendered analysis report
├── stochastic_processes_project.qmd  # Main source code
└── README.md
```

---

## 📈 Results

### Performance Metrics
*(This project focuses on theoretical simulations and properties; no predictive performance metrics are evaluated).*

### Key Findings
- **Verified Stationarity:** Stationarity is verified through polynomial roots for MA(1), MA(2), AR(1), AR(2), ARMA(1,1), ARMA(3,2).
- **Confirmed Expectations:** ACF and PACF shapes confirm theoretical expectations for all simulated processes.
- **AR Patterns:** AR processes exhibit an exponentially decaying ACF.
- **MA Patterns:** MA processes exhibit an ACF that cuts off after lag q.
- **ARMA Patterns:** ARMA processes exhibit mixed exponential patterns in their ACF and PACF.

---

## 📚 References
- Hamilton, *Time Series Analysis*  
- Hyndman & Athanasopoulos, *Forecasting: Principles and Practice*  
- Sévi, B. (2024). *Support de cours – Séries temporelles univariées (M1 ECAP)*
- Wooldridge, *Introductory Econometrics: A Modern Approach*  

---

## 📜 License
This project is released under the MIT License.  
© 2025 Djayan Daëron and Florian Crochet

---

## 👤 Authors
**Djayan Daëron**  
[GitHub Profile](https://github.com/Djayan-D)  

**Florian Crochet**  
[GitHub Profile](https://github.com/floriancrochet)

*Master 1 – Econometrics & Statistics, Applied Econometrics Track*  

---

## 🤝 Acknowledgments
This work was conducted as part of the Univariate Time Series course, supervised by Benoît Sévi.
