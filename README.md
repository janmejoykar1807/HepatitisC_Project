# 🩺 Hepatitis C Prediction — Statistical Inference & Logistic Regression

> **Can biomarkers in blood donor data predict Hepatitis C risk?**
> This project applies hypothesis testing, statistical inference, and logistic regression to answer exactly that — using a real clinical dataset of 615 blood donors.

---

## 📌 Project Overview

Hepatitis C is a liver disease caused by the Hepatitis C virus (HCV), and early detection through blood biomarker analysis is critical for timely treatment. This project frames **five analytical questions** around a real-world clinical dataset and answers each one using rigorous statistical methods — implemented in both **Python** and **R**.

The analysis covers probability estimation, two-sample hypothesis testing, z-tests, and logistic regression with confidence intervals — demonstrating an end-to-end statistical modeling workflow.

---

## 📂 Repository Structure

```
HepatitisC_Project/
│
├── HepatitisCdata.csv          # Clinical dataset (615 blood donor records)
├── ProjectPY.ipynb             # Python analysis: probability, hypothesis tests, logistic regression
├── Project 1.Rmd               # R analysis: logistic regression + confidence intervals
├── Final Project.docx          # Written report with full findings and interpretation
└── README.md
```

---

## 🔬 Dataset

| Feature | Description |
|--------|-------------|
| **ALB** | Albumin (g/L) — liver protein marker |
| **ALP** | Alkaline Phosphatase — enzyme linked to liver/bone disease |
| **ALT** | Alanine Transaminase — liver enzyme, elevated in liver damage |
| **CHOL** | Cholesterol level |
| **Protein** | Total blood protein |
| **Category** | Blood donor vs. Hepatitis C patient |

- **Records:** 615 blood donors
- **Source:** Real-world clinical data

---

## ❓ Research Questions & Findings

### Q1 — Probability Estimation
**What is the probability that a donor has Albumin (ALB) > 30 mg/L?**

Using z-score normalization:

```
Z = (30 – 41.62) / 14.9 = –0.78
P(ALB > 30) = 1 – P(Z < –0.78) = 1 – 0.2177 = 0.7823
```

**Finding:** ~78.2% of donors have albumin above 30 mg/L — indicating a predominantly healthy donor pool. Only 24 out of 615 donors fell below the threshold.

---

### Q2 — Two-Sample Hypothesis Test (ALP vs. Protein)
**H₀:** Mean ALP ≥ Mean Protein
**Hₐ:** Mean Protein > Mean ALP  *(α = 0.075)*

```
Z = (68.28 – 72.04) / √(26.03²/597 + 5.4²/615) = –3.459
Critical value at α = 0.075: –1.440
```

**Result:** Reject H₀. Protein mean significantly exceeds ALP, indicating healthy liver function in the donor population.

---

### Q3 — Two-Sample Hypothesis Test (CHOL vs. ALT)
**H₀:** Mean CHOL ≥ Mean ALT
**Hₐ:** Mean ALT > Mean CHOL  *(α = 0.05)*

```
Z = (5.37 – 28.45) / √(1.13²/605 + 25.47²/614) = –22.43
Critical value at α = 0.05: –1.645
```

**Result:** Reject H₀. Elevated ALT relative to CHOL indicates liver enzyme activity consistent with early disease risk in a subset of donors.

---

### Q4 — Hypothesis Synthesis
Combined interpretation of Q2 & Q3 confirms that the majority of the dataset consists of **healthy blood donors**, with biomarker levels outside the disease-risk zone for most individuals.

---

### Q5 — Logistic Regression & Confidence Intervals
Full logistic regression model implemented in **R** (`Project 1.Rmd`) predicting Hepatitis C disease status from biomarker features, including:
- Model coefficients and odds ratios
- Confidence intervals for each predictor
- Model evaluation metrics

---

## 🛠️ Tech Stack

| Tool | Usage |
|------|-------|
| **Python** (Pandas, NumPy, SciPy, Scikit-Learn) | Probability estimation, hypothesis testing, logistic regression |
| **R** (glm, stats) | Logistic regression, confidence intervals |
| **Jupyter Notebook** | Python interactive analysis |
| **R Markdown** | R reproducible report |

---

## 💡 Key Skills Demonstrated

- ✅ Probability estimation using z-score normalization
- ✅ One-sample and two-sample z-tests
- ✅ Null hypothesis significance testing (NHST) with custom α levels
- ✅ Logistic regression with confidence interval interpretation
- ✅ Bilingual statistical analysis: Python **and** R
- ✅ Clinical data interpretation and storytelling

---

## 🚀 How to Run

**Python:**
```bash
pip install pandas numpy scipy scikit-learn matplotlib jupyter
jupyter notebook ProjectPY.ipynb
```

**R:**
Open `Project 1.Rmd` in RStudio and click **Knit** to generate the full report.

---

## 📬 Author

**Janmejoy Kar** — Data Scientist | [LinkedIn](https://www.linkedin.com/in/janmejoy-kar-849756196/) | [GitHub](https://github.com/janmejoykar1807)
