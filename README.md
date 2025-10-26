# **Compositional Data Analysis (CoDA)**  
**Author:** Kushal Kharel

**Date:** October 25, 2025  

---

## **Abstract**
This project demonstrates a rigorous, mathematically-grounded approach to analyzing **Compositional Data (CoDa)** using principles from **Aitchison Geometry**

---

## **Project Goal**
The primary goal is to show and build a robust and statistically valid **predictive model** for a target variable (e.g., a percentage of people working from home or another relative measure) using a set of predictor variables that are **compositional** (i.e., they represent parts of a whole, such as time spent in various locations or modes of transportation).

---

## **The Core Problem: Why Standard Statistics Fails**
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

## **5. Business Applications and Recommendations**

---

### **Business Value**

The analysis of **commute mode compositions** provides actionable intelligence for organizations focused on **urban mobility**, **sustainability**, and **market penetration**.

#### **Public Transit Agencies (PTA)**  
- **Optimization:** Use predicted mode shares to strategically allocate public transit resources (buses, trains) to Census Tracts where the `percent_public` component is projected to grow (*high-propensity areas*).  
- **New Route Planning:** Identify high-density worker areas with low `percent_public` to propose new transit routes or last-mile services.

#### **Micromobility Companies (Bikes/Scooters)**  
- **Targeting:** Identify Tracts with high `percent_walk` or high `percent_bicycle` potential (e.g., high population density but low vehicle ownership rates) to deploy **bike/scooter-sharing fleets**.

#### **Government & Urban Planning**  
- **Infrastructure Investment:** Justify investments in **bike lanes**, **pedestrian infrastructure**, or **HOV lanes** by identifying Tracts with the highest potential return on investment — i.e., areas where a small infrastructure change could shift a large share from `percent_own_vehicle_alone` to `percent_bicycle` or `percent_carpool`.

---

### **Recommendations**

#### **Feature Augmentation (ML Recommendation)**  
Integrate external data to improve predictive power.  
Key features to add for each Census Tract include:

| **Category** | **Example Features** |
|---------------|----------------------|
| **Socioeconomic** | Median household income, poverty rate |
| **Demographic** | Population density, age distribution |
| **Infrastructure** | Transit stop density, miles of bike lanes, average commute time |

---

#### **Predictive Scenario Analysis (Business Recommendation)**  
Develop a **simulation capability** to test policy interventions.  
For example:
- Predict the change in the full 7-part composition vector **$\mathbf{x}$** if a new transit line is introduced (modeled as a **covariate shift**).  
- Simulate the impact if a **Work From Home (WFH)** mandate is lifted, observing how the commute composition adjusts.

---

#### **Focus on Log-Ratios (Statistical Recommendation)**  
The report should pivot from analyzing **raw percentages** to analyzing **ratios** — e.g.:

$$
\text{Efficiency Ratio} = \frac{\text{Drove Alone}}{\text{Active Modes (Walk + Bicycle)}}
$$

This ratio serves as the true metric of **transportation efficiency** and **sustainability progress**, aligning with principles of **Compositional Data Analysis (CoDA)** and **Aitchison Geometry**.

---

**Summary:**  
These business applications demonstrate how compositional regression insights can guide **policy**, **investment**, and **market strategy**—bridging the gap between statistical rigor and actionable decision-making.


## **References**
- Aitchison, J. (1986). *The Statistical Analysis of Compositional Data.* Chapman and Hall.  
- Pawlowsky-Glahn, V., Egozcue, J. J., & Tolosana-Delgado, R. (2015). *Modeling and Analysis of Compositional Data.* Wiley.  
- Quinn, T. P., & Erb, I. (2020). *Using Compositional Data Analysis to Understand Microbiome Data.* PLOS Computational Biology.

---

## **Keywords**
`Compositional Data` · `Aitchison Geometry` · `ILR Transform` · `Regression` · `ElasticNet` · `DOT Analysis` · `CoDA`· `XgBoost`· `Linear Regression`
