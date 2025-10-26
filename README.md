# **Compositional Data Analysis (CoDA)**  
**Author:** Kushal Kharel

**Date:** October 25, 2025  

---

## **Abstract**
This project demonstrates a rigorous, mathematically-grounded approach to analyzing **Compositional Data (CoDa)** using principles from **Aitchison Geometry**

---

## **1. Project Goal**
The primary goal is to show and build a robust and statistically valid **predictive model** for a target variable (e.g., a percentage of people working from home or another relative measure) using a set of predictor variables that are **compositional** (i.e., they represent parts of a whole, such as time spent in various locations or modes of transportation).

---

## **2. The Core Problem: Why Standard Statistics Fails**
Standard statistical and machine learning models (e.g., mean, correlation, linear regression) assume the data lives in an unconstrained **Euclidean space**.  
However, compositional data, where all parts must sum to a constant (e.g., 100%), lives on a constrained surface called the **simplex**:

### The Problems:
- **Constraint:** Any operation on the simplex is *closed* and violates independence assumptions.  
- **Result:** Distances, averages, and correlations calculated using standard methods on raw percentages are **statistically meaningless and misleading**.

**Solution:** Transform the data out of the simplex before applying standard statistics.

---
- **Interpretability (Area for Improvement):**  
  Coefficients trained on ILR balances must be **back-transformed**.  
  Interpreting results in terms of *ratios* of the original compositional parts (the “relative effect”) is essential for actionable insights.
---

## **References**
- Aitchison, J. (1986). *The Statistical Analysis of Compositional Data.* Chapman and Hall.  
- Pawlowsky-Glahn, V., Egozcue, J. J., & Tolosana-Delgado, R. (2015). *Modeling and Analysis of Compositional Data.* Wiley.  
- Quinn, T. P., & Erb, I. (2020). *Using Compositional Data Analysis to Understand Microbiome Data.* PLOS Computational Biology.

---

## **Keywords**
`Compositional Data` · `Aitchison Geometry` · `ILR Transform` · `Regression` · `ElasticNet` · `DOT Analysis` · `CoDA`· `XgBoost`· `Linear Regression`
