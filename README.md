# 🌌 Exoplanet Detection Using Kepler Space Telescope Data  
### *A Research and AI-based Project by Team Vizards*  
**NASA Space Apps Challenge 2025**

---

## 🌟 Overview  

The search for exoplanets — planets orbiting stars beyond our solar system — is one of NASA’s most ambitious missions. The **Kepler Space Telescope** gathered light data from thousands of stars to detect tiny dips in brightness caused by potential planets transiting in front of them.  

Our project, developed by **Team Vizards**, leverages **machine learning** and **astrophysical insights** to assist in identifying and classifying these potential exoplanets.  
We use the **Kepler dataset** to train an AI model that distinguishes **confirmed planets** from **false positives** or **stellar anomalies**, helping NASA scientists process vast amounts of astronomical data more efficiently.

---

## 🧠 Project Objective  

The main objective of this project is to build a **predictive machine learning model** that can:  
- Automatically classify celestial bodies observed by Kepler as **exoplanets or not**.  
- Improve **accuracy and consistency** in planet detection.  
- Provide NASA with a **supportive analytical tool** that reduces manual verification time.  

---

## 🧩 Dataset Details  

- **Source:** [NASA Exoplanet Archive (Kepler Data)](https://exoplanetarchive.ipac.caltech.edu/)  
- **Dataset Size:** ~9,000 entries  
- **Type:** Tabular, structured dataset  
- **Purpose:** To identify and categorize potential exoplanets based on observed stellar parameters.  

**Key Features:**
| Feature | Description |
|:--|:--|
| `kepid` | Unique Kepler ID for each star |
| `kepoi_name` | Kepler Object of Interest (KOI) identifier |
| `koi_disposition` | Final classification — Confirmed, Candidate, or False Positive |
| `koi_score` | Confidence level of the planetary detection |
| `koi_period` | Orbital period of the candidate planet |
| `koi_prad` | Estimated planetary radius (in Earth radii) |
| `koi_fpflag_nt`, `koi_fpflag_ec` | False positive indicators |
| `koi_depth` | Transit depth — how much brightness was blocked |
| `koi_duration` | Duration of the transit event |

---

## 🧹 Data Cleaning and Preparation  

To ensure high-quality input data, we performed the following steps:  
1. **Removed missing or null values** to maintain data consistency.  
2. **Selected relevant astrophysical parameters** for model training.  
3. **Encoded** categorical variables (such as disposition) into numerical form.  
4. **Scaled numeric features** using `StandardScaler` for balanced input magnitudes.  
5. **Split the dataset** into training and testing sets for unbiased evaluation.  

These steps allowed our AI model to focus on meaningful astrophysical features and avoid noisy or incomplete data.

---

## ⚙️ Tools, Technologies, and Libraries  

| Category | Tools / Languages |
|:--|:--|
| **Programming Language** | Python |
| **Libraries Used** | Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn |
| **Data Visualization** | Seaborn Heatmaps, Matplotlib Charts |
| **Data Preprocessing** | Pandas (for cleaning and selection) |
| **Machine Learning Model** | Random Forest Classifier |
| **Development Environment** | Jupyter Notebook / Google Colab |
| **Version Control** | Git & GitHub |

---

## 🧬 Model and Methodology  

We implemented a **Random Forest Classifier**, an ensemble-based algorithm that combines multiple decision trees for more accurate predictions.  

### Why Random Forest?
- Performs well on large and complex datasets.  
- Automatically handles feature interactions.  
- Resistant to overfitting and noisy data.  
- Provides **feature importance** metrics to identify the most impactful astrophysical parameters.

The model predicts whether each observation corresponds to a **confirmed planet** or a **false positive**, based on input parameters such as orbital period, radius, and light curve characteristics.

---

## 📊 Results and Performance  

After training and evaluation, our model achieved:  
- **Accuracy:** ~94%  
- **High Precision and Recall:** Balanced across both classes (planet vs non-planet).  
- **Confusion Matrix Visualization:** Demonstrates effective differentiation between confirmed and false-positive signals.  

This accuracy level indicates that our model can reliably assist NASA scientists in identifying real exoplanets with high confidence.

---

## 🔭 Role of Physics in the Project  

Physics plays a crucial role in both the dataset interpretation and feature engineering:  
- **Transit Photometry:** Understanding how a planet’s orbit causes measurable brightness dips.  
- **Orbital Mechanics:** Using period and radius to understand gravitational relationships.  
- **Luminosity and Stellar Flux:** Relating energy output variations to planetary transits.  
- **Signal-to-Noise Ratio:** Distinguishing genuine planetary signals from background noise.  

By combining physics with AI, we bridge the gap between raw data and scientific discovery.

---

## 🚀 How This Project Helps NASA  

1. **Accelerates Exoplanet Discovery:** Reduces manual effort by automating classification tasks.  
2. **Improves Mission Efficiency:** Helps scientists focus on promising candidates rather than filtering massive datasets manually.  
3. **Supports Future Missions:** The approach can be adapted for datasets from **TESS**, **JWST**, and other telescopes.  
4. **Enhances Data Reliability:** Minimizes human bias and standardizes the identification process.  
5. **Fosters Human-AI Collaboration:** Demonstrates how AI can complement astrophysics research for scalable space exploration.

---

## 🌍 Real-World Impact  

This project goes beyond coding — it demonstrates how **artificial intelligence can empower scientific discovery**.  
By applying machine learning to astrophysical data, we open new possibilities for identifying habitable planets and understanding the formation of planetary systems.  

The results not only assist NASA but also contribute to humanity’s collective understanding of the cosmos — answering the age-old question:  
**“Are we alone in the universe?”**

---

## 🔮 Future Works  

While our current model achieves strong results, we envision several future enhancements:  

1. **Deep Learning Integration:**  
   Implement Convolutional Neural Networks (CNNs) to analyze raw **light curve data** directly, improving pattern recognition and detection sensitivity.  

2. **Cross-Mission Generalization:**  
   Adapt our AI framework to data from **TESS**, **JWST**, and upcoming missions to expand planetary discovery capabilities.  

3. **Real-Time Planet Detection System:**  
   Develop a real-time analysis pipeline capable of processing new telescope observations as they arrive, supporting ongoing missions dynamically.  

4. **Explainable AI Models:**  
   Introduce explainable AI (XAI) techniques to make predictions more transparent for scientists and validate results with physical reasoning.  

5. **Astrophysical Visualization Platform:**  
   Create a user-friendly dashboard for researchers to visualize and interact with planetary candidates, light curves, and AI predictions.  

6. **Collaboration with Astrophysicists:**  
   Work alongside domain experts to refine model parameters and ensure physical accuracy in predictions.  

---

## 🏁 Conclusion  

Our project represents a synergy of **AI and astrophysics**, transforming raw telescope data into scientific insight.  
Through this collaboration between data science and physics, **Team Vizards** contributes to NASA’s goal of expanding human knowledge about distant worlds.  

> *“Every data point in the sky tells a story — AI helps us read it faster.”* 🌠  
