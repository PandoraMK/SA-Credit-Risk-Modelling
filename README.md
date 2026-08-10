# South African Retail Credit Risk & Default Probability Pipeline

![Python](https://img.shields.io/badge/Python-3.11-blue.svg)
![Domain](https://img.shields.io/badge/Domain-Credit%20Risk%20%26%20Retail%20Finance-green)
![Toolkit](https://img.shields.io/badge/Toolkit-Pandas%20%7C%20NumPy%20%7C%20Scikit--Learn%20%7C%20SHAP-orange)

## Executive Summary
This project simulates an end-to-end quantitative credit risk scoring engine tailored to the South African retail credit landscape. Using synthetic demographic and financial data calibrated against TransUnion credit score bounds, South African National Credit Act (NCA) Debt-to-Income (DTI) metrics, and SASSA grant indicators, this pipeline models non-performing loans (NPLs) and assesses applicant default probabilities using logistic log-odds risk modelling and SHAP (SHapley Additive exPlanations) for model explainability.

---

## Key Business Outcomes & Capabilities

* **Credit Risk Modeling:** Formulated default probability thresholds by transforming multi-variable financial profiles (Bureau Score, DTI, Income) into baseline log-odds equations.
* **South African Economic Context Integration:** Modeled structural market dynamics including SASSA grant receipt floor adjustments and regional/provincial demographic distribution weighting.
* **Portfolio Health Metrics:** Tracked Non-Performing Loan (NPL) ratios across a simulated portfolio of 10,000 retail credit applicants (achieving an unadjusted baseline NPL ratio of ~16.96%).
* **Model Explainability & Auditing:** Integrated SHAP values to explain individual feature attribution (Credit Score vs. DTI weighting) to ensure regulatory transparency and compliance.

---

## Technical Stack & Methodologies

| Domain | Tools / Techniques Applied |
| :--- | :--- |
| **Data Generation & Cleaning** | Python (`pandas`, `numpy`), Log-Normal & Beta distributions |
| **Statistical Modeling** | Logistic Regression, Bernoulli trials, Log-Odds risk calibration |
| **Model Explainability** | SHAP (`shap`), Feature Importance Attribution |
| **Data Visualization** | `matplotlib`, `seaborn`, PowerBI integration ready |

---

## Data Pipeline Architecture

1. **Demographic & Income Calibration:** Generates synthetic applicants with realistic income distributions ($\mu=\text{R}10,000$) and income-restricted grant distributions.
2. **Credit Bureau Score Simulation:** Bounded to South African credit bureau ranges ($300 - 850$), factoring in employment stability penalties and score noise.
3. **Target Variable Formulation:**
   $$\text{Log-Odds} = \beta_0 + \beta_1 \cdot \text{DTI}_{\text{norm}} - \beta_2 \cdot \text{Credit}_{\text{norm}} - \beta_3 \cdot \text{Income}_{\text{norm}} + \text{Risk Adjustments}$$
4. **NPL Simulation:** Evaluates individual binomial default trials to establish portfolio default behavior under stress test conditions.

---

## How to Run

1. Clone the repository:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/SA-Credit-Risk-Modelling.git](https://github.com/YOUR_USERNAME/SA-Credit-Risk-Modelling.git)
   cd SA-Credit-Risk-Modelling