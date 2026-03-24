# 🍔 A/B Testing & ANOVA Analysis for Fast Food Marketing Campaign

![Python](https://img.shields.io/badge/Python-3.9-blue)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
![Focus](https://img.shields.io/badge/Domain-Marketing%20Analytics-purple)
![Tech](https://img.shields.io/badge/Tech-Statistics%20%7C%20A%2FB%20Testing-blue)

---

## 📌 Project Overview  
This project evaluates the effectiveness of multiple marketing campaigns for a fast food chain using **A/B testing and statistical hypothesis testing (ANOVA & non-parametric tests)**.

The goal is to determine whether differences in campaign performance are **statistically significant**, enabling better marketing budget allocation and ROI optimization.

---

## 🎯 Business Problem  
Marketing teams often rely on average sales metrics, which can be misleading.

👉 **Key Question:**  
Which campaign truly drives higher sales, and are these differences statistically significant?

---

## 📊 Dataset  
- **File:** `WA_Marketing-Campaign.csv`  
- **Size:** 548 observations across 3 campaign types  
- Key features:
  - Promotion (Campaign Type: 1, 2, 3)
  - SalesInThousands (Target variable)
  - MarketSize (Small, Medium, Large)
  - AgeOfStore, LocationID, Week  

---

## 🛠️ Tech Stack  
- **Python:** Pandas, NumPy  
- **Statistical Testing:** SciPy, Statsmodels  
- **Visualization:** Matplotlib, Seaborn  
- **Notebook:** Jupyter  

---

## 🔍 Methodology  

### 1. Data Cleaning & Preparation  
- Verified no missing values  
- Checked data types and distributions  
- Removed inconsistencies and validated dataset  

---

### 2. Exploratory Data Analysis (EDA)  
- Compared average sales across campaigns  
- Visualized distributions using boxplots and bar charts  
- Identified outliers across market size and store age  

---

### 3. Assumption Testing  

Before ANOVA, key assumptions were tested:

- **Normality (Shapiro-Wilk Test):**
  - p-values ≈ `1e-08` → Data **not normally distributed**

- **Homogeneity of Variance (Levene Test):**
  - p-value = **0.2817** → Variances are equal ✅  

---

### 4. Statistical Testing  

Since normality was violated, a **non-parametric alternative (Kruskal-Wallis Test)** was used:

- **Kruskal-Wallis Statistic:** `53.29`  
- **P-Value:** `2.67e-12`

---

## 📈 Key Results  

### ✅ Hypothesis Decision  
- p-value << 0.05  
👉 Reject the null hypothesis  

✔️ There is a **statistically significant difference** between campaign performances  

---

### 🔍 Post-Hoc Analysis (Pairwise Comparisons)

| Campaign Comparison | P-Value | Insight |
|--------------------|--------|--------|
| Campaign 1 vs 2 | 6.46e-12 | Significant difference |
| Campaign 2 vs 3 | 7.08e-07 | Significant difference |
| Campaign 1 vs 3 | 0.145 | Not significant |

---

### 🏆 Business Insights  

- **Campaign 2 performs significantly differently (and likely strongest/weakest depending on mean)**
- **Campaign 1 and 3 show similar performance**
- Campaign 2 is the **key differentiator in marketing strategy**

---

## 📊 Additional Insights  

- Average sales: **~53.47K per store**  
- Outliers more frequent in **younger stores (0–10 years)**  
- Market size shows variation but not the primary driver compared to promotion  

---

## 💡 Business Impact  

- 📈 Enables **data-driven campaign selection**  
- 🎯 Identifies which campaigns to **scale or eliminate**  
- 💰 Optimizes **marketing spend allocation**  
- 🔁 Establishes a **repeatable A/B testing framework**  

---
