#  Sowing Success: Predicting Optimal Crops Based on Soil Composition

**Author:** Alvaro Mejia 
**Region of Study:** Rural Santander, Colombia  
**Project Type:** Advanced Machine Learning & Agronomic Analytics  
**Keywords:** Random Forest, Soil Nutrients, Precision Agriculture, Feature Importance, GIS Mapping  

---

##  Project Overview

This project explores how **Machine Learning** can help farmers in *rural Santander, Colombia*, select the **optimal crop** for their land based on soil nutrient composition.  
By analyzing **Nitrogen (N)**, **Phosphorus (P)**, **Potassium (K)**, and **pH**, the model identifies the most influential feature for predicting crop suitability.

> The primary goal is to determine which single soil component provides the **highest predictive power** for crop classification — enabling data-driven agricultural decision-making under resource constraints.

---

##  Context

Agriculture in Santander's rural zones (e.g., Vélez, Socorro, San Gil) depends heavily on the fertility of the soil and the accurate measurement of its nutrients.  
However, **soil testing** can be costly and time-consuming, often forcing farmers to measure only a few components.  

By applying **supervised machine learning**, this project offers a scientific approach to prioritizing which soil metrics (e.g., N, P, K, or pH) should be measured first to predict the best crop yield potential.

---

##  Data Description

Dataset: `soil_measures.csv`

| Feature | Description |
|----------|--------------|
| `N` | Nitrogen content ratio in the soil |
| `P` | Phosphorus content ratio in the soil |
| `K` | Potassium content ratio in the soil |
| `ph` | Soil pH value |
| `crop` | Target variable indicating the most suitable crop |

> Synthetic geospatial coordinates (`latitude`, `longitude`) were added to visualize the nutrient distribution across rural Santander.

---

##  Methodology

1. **Data Exploration and Cleaning**  
   - Descriptive statistics, missing value analysis, and target distribution.  
2. **Train-Test Split**  
   - Dataset divided into 80% training and 20% testing sets with stratified sampling.  
3. **Modeling Approach**  
   - **Random Forest Classifier** selected due to its robustness in handling multiclass classification and nonlinear relationships.  
4. **Feature Evaluation**  
   - Each soil feature trained individually; accuracy scores compared to determine the best predictive variable.  
5. **Visualization**  
   - Feature ranking via bar chart.  
   - Geographic mapping using *GeoPandas* and *Folium* for potassium concentration zones.

---

## Key Results

| Feature | Accuracy |
|----------|-----------|
| **K (Potassium)** | **0.31** |
| P (Phosphorus) | 0.21 |
| N (Nitrogen) | 0.15 |
| pH | 0.14 |

**Conclusion:**  
Potassium (*K*) is the **most predictive soil nutrient** for determining optimal crop selection in rural Santander.  

> Soils rich in potassium tend to support crops such as rice, sugarcane, and maize, which require efficient nutrient and water regulation mechanisms.

---

##  Geospatial Insight

A simulated **GIS visualization** demonstrates the spatial distribution of potassium levels across sample locations in Santander.  
High-potassium zones (orange markers) indicate areas where potassium concentration exceeds the median — potentially ideal for potassium-demanding crops.

---

##  Professional Insights and Recommendations

1. **Agronomic Perspective**
   - Potassium significantly affects plant *photosynthesis*, *enzyme activation*, and *water regulation*.  
   - Farmers should prioritize **K measurement** when facing testing budget limitations.  

2. **Data Science Perspective**
   - Integrate **temporal and climatic features** to enhance predictive generalization.  
   - Implement **Gradient Boosting** or **XGBoost** for ensemble-level improvement.  
   - Use **cross-validation** and **feature permutation importance** for robustness validation.  

3. **Deployment Suggestion**
   - Transform the model into a **decision-support web app** for farmers, allowing them to input soil data and receive crop recommendations.

---

##  Technical Stack

| Category | Tools / Libraries |
|-----------|-------------------|
| Language | Python 3.10+ |
| Data Analysis | Pandas, NumPy |
| Machine Learning | Scikit-learn (RandomForestClassifier) |
| Visualization | Matplotlib, Seaborn |
| Geospatial Analysis | GeoPandas, Folium |
| Documentation | Jupyter Notebook, Markdown |

---

##  References

- Breiman, L. (2001). *Random Forests.* Machine Learning, 45(1), 5–32.  
- Pedregosa et al. (2011). *Scikit-learn: Machine Learning in Python.* Journal of Machine Learning Research.  
- FAO (2023). *Soil Nutrient Management for Sustainable Agriculture.*  
- IGAC (Colombia). *Soil and Land Use Reports for Santander Department.*

---

##  Authors and Attribution

**Prepared by:**  
*Data Science SackoData — Advanced Agronomic Analytics Unit*  
**Location:** Bucaramanga, Santander, Colombia  

 **Contact:** alvaro.mejia.r45@gmail.com


---
