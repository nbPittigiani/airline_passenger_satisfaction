# Airline Passenger Satisfaction Analysis ✈️

## 📌 Project Overview

This project aims to analyze the key drivers of airline passenger satisfaction using a data-driven approach. Instead of relying solely on black-box predictions, the analysis first focuses on understanding the **latent structure** of the data through Unsupervised Learning.

The project is divided into two phases:

* **Part 1: Unsupervised Learning, Factor Analysis & Ranking (Current Focus)**
* **Part 2:** Predictive Modeling & Classification (Coming Soon)

## 💼 Business Problem

Airline datasets often suffer from the **"Curse of Dimensionality"** and high multicollinearity. Passengers rate multiple aspects of the flight (food, wifi, seat comfort, legroom, etc.), which are naturally correlated.

The goal of this phase is to:

1. Reduce dimensionality without losing critical information.
2. Identify the underlying "Constructs" of satisfaction (e.g., Comfort vs. Logistics).
3. Create a synthetic **Global Quality Ranking** to score passengers' experiences mathematically.

## 🔍 Part 1: Exploratory & Factor Analysis (PCA)

In this first notebook, we performed a deep dive into the dataset structure using **Factor Analysis (PCA Method)**.

### Key Steps:

1. **Data Preprocessing:** Cleaning, encoding categorical variables, and standardizing metrics ().
2. **Suitability Tests:** Validated PCA applicability using **Bartlett’s Test of Sphericity** and **KMO (Kaiser-Meyer-Olkin)**.
3. **Factor Extraction:**
* Applied the **Kaiser Criterion** (Eigenvalues > 1).
* Extracted **6 Latent Factors** that explain the majority of the variance.
* Used **Varimax Rotation** to interpret the factors (e.g., *In-flight Experience*, *Digital Logistics*, *Flight Delays*).


4. **Refinement:** Iteratively removed variables with low communality (< 0.5) to reduce noise.

### 🏆 The Global Ranking

A unique feature of this analysis is the creation of a **Weighted Global Ranking**.
We calculated a composite score for each passenger based on their factor scores weighted by the variance explained by each factor.

**Validation:**
Even without training a supervised model, the Unsupervised Ranking successfully discriminated between the classes:

* **Satisfied** passengers had consistently positive ranking scores.
* **Neutral/Dissatisfied** passengers had consistently negative ranking scores.

## 🛠️ Tech Stack

* **Python**
* **Pandas & NumPy:** Data Manipulation
* **Matplotlib & Seaborn:** Visualization
* **FactorAnalyzer & Scikit-learn:** Dimensionality Reduction (PCA/FA)

## 🚀 Roadmap

* [x] **Part 1:** Data Cleaning, Factor Analysis, and Ranking Creation.
* [ ] **Part 2:** Predictive Modeling. We will use the 6 extracted factors (instead of the 20+ original features) to train Machine Learning models (Random Forest, Logistic Regression) to predict passenger satisfaction with high efficiency.

---

*Author: Breno Pittigliani*
