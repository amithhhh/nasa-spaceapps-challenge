# 🪐 Exoplanet Detection Using Kepler Space Telescope Data  
### *A Machine Learning Project by Team Vizards*  
**NASA Space Apps Challenge 2025**

---

## 🌟 Overview  

The **Kepler Space Telescope** mission by NASA was designed to discover Earth-sized exoplanets orbiting distant stars. It generated a massive dataset containing information about planetary candidates, false positives, and confirmed planets.  

Our team, **Vizards**, developed a **machine learning model** that analyzes this Kepler dataset to predict whether a given celestial object is a **planet or not**.  
This project demonstrates how artificial intelligence can support astronomical research and accelerate the discovery of new worlds beyond our solar system.  

---

## 🚀 Problem Statement  

The identification of exoplanets involves analyzing thousands of signals that could be due to planets, stars, or other celestial bodies.  
Manual verification is time-consuming and prone to human error.  

Our goal is to:  
- Build a **data-driven classification model** to identify potential exoplanets.  
- Reduce **false positives** using machine learning.  
- Assist astronomers in **prioritizing candidates** for further study.  

---

## 🧠 Objective  

To create a **predictive ML model** that classifies each observation in the Kepler dataset as either a **confirmed planet** or a **false positive**, based on multiple features like orbital period, planet radius, depth, and confidence score.  

---

## 🧩 Dataset  

- **Source:** [NASA Exoplanet Archive (Kepler Data)](https://exoplanetarchive.ipac.caltech.edu/)  
- **Size:** ~9,000+ entries  
- **Key Attributes:**  
  - `koi_disposition` – Final planet disposition (Confirmed, Candidate, or False Positive)  
  - `koi_score` – Model confidence score  
  - `koi_period`, `koi_depth`, `koi_prad` – Orbital and physical properties  
  - `koi_fpflag_nt`, `koi_fpflag_ec` – False positive indicators  

---

## 🧹 Data Cleaning & Preprocessing  

1. **Dropped missing values** using `dropna()` to ensure clean input data.  
2. **Selected relevant columns** contributing to classification.  
3. **Encoded** `koi_disposition` → Binary target (`Planet=1`, `Not Planet=0`).  
4. **Scaled** numeric features using `StandardScaler` to normalize feature ranges.  
5. **Split dataset** into 80% training and 20% testing data.  

---

## ⚙️ Model Building  

- **Algorithm Used:** Random Forest Classifier  
- **Why Random Forest?**  
  - Handles large feature sets efficiently.  
  - Resistant to overfitting.  
  - Provides feature importance insights.  

```python
from sklearn.ensemble import RandomForestClassifier
model = RandomForestClassifier(random_state=42)
model.fit(X_train_scaled, Y_train)
Y_pred = model.predict(X_test_scaled)
