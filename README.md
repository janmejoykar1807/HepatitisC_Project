# Hepatitis C Prediction Project

A statistical analysis and machine learning project using a real-world Hepatitis C dataset. The project applies hypothesis testing, probability analysis, and logistic regression to understand key blood markers in liver disease.

---

## 📋 Project Overview

This project uses a dataset of 615 blood donors to analyze clinical markers associated with Hepatitis C. It was designed as an applied statistics project to answer specific clinical questions using inferential statistics and predictive modeling.

---

## ❓ Research Questions

1. What is the probability of **Albumin (ALB)** being more than 30 mg/L?
2. Is the **mean of Alkaline Phosphatase (ALP)** greater than the **mean of Protein**? *(α = 0.075)*
3. Is the **mean of Cholesterol (CHOL)** greater than the **mean of Alanine Transaminase (ALT)**? *(α = 0.05)*
4. Are the test statistics for **CHOL and ALP** within the not-reject region?
5. Run a **logistic regression** on the dataset and report confidence intervals.

---

## 📊 Key Findings

- **Q1 — Albumin Probability:** Only 24 out of 615 donors had ALB < 30 mg/L. The probability of ALB > 30 mg/L is approximately **78.23%**, suggesting most donors have healthy albumin levels.
- **Q2 — ALP vs. Protein (z-test):** With z = −3.459 and a critical value of 1.440 at α = 0.075, the null hypothesis is **rejected**.
- **Q3 — CHOL vs. ALT (z-test):** With z = −22.43 and a critical value of 1.645 at α = 0.05, the null hypothesis is **rejected**.
- **Q4 — Hypothesis Summary:** Both CHOL and ALP test statistics fall outside the non-rejection region, confirming predominantly healthy donors.
- **Q5 — Logistic Regression:** See `ProjectPY.ipynb` (Python) and `Project 1.Rmd` (R) for full results with confidence intervals.

---

## 📁 Repository Structure

| File | Description |
|------|-------------|
| `HepatitisCdata.csv` | Raw dataset (615 blood donor records) |
| `ProjectPY.ipynb` | Python analysis: probability, z-tests, logistic regression |
| `Project 1.Rmd` | R analysis: confidence intervals and logistic regression |
| `Final Project.docx` | Written report with full findings |

---

## 🛠️ Technologies Used

- **Python** — `pandas`, `numpy`, `scipy`, `statsmodels`, `sklearn`
- **R** — `glm()`, `confint()`, base statistics
- Jupyter Notebook & R Markdown

---

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/janmejoykar1807/HepatitisC_Project.git
   ```

2. Open `ProjectPY.ipynb` in Jupyter Notebook for the Python analysis.
3. Open `Project 1.Rmd` in RStudio for the R analysis.

---

## 👤 Author

**Janmejoy Kar**
Data Science learner — applying Python, R, and SQL for data analysis and predictive modeling.
[GitHub Profile](https://github.com/janmejoykar1807)
