# Data-Driven Identification of Optimal Urban Tree Planting Sites 
---

> 📄 Full write-up: see [docs/Report.pdf](https://tarungangadhar.github.io/tree-planting-sites-website/)

> Project Website: https://tarungangadhar.github.io/hybrid-pruning-3dgs-website/

---

## Abstract
Urban tree plantation is essential to mitigate environmental challenges such as air pollution, stormwater runoff, and the urban heat island effect. This project identifies **optimal planting sites** within the City of Buffalo using the **Bureau of Forestry Tree Inventory dataset (133,000+ records)**. We performed **exploratory data analysis (EDA)**, **clustering (K-Means)**, **regression**, and **decision tree classification**, combined with **geospatial visualization (Folium, Heatmaps)**, to guide city planners in prioritizing zones for new plantations

---

## Methodology
- **Phase 1:** Data cleaning, outlier removal, EDA (DBH, eco-benefits, CO₂ sequestration).
- **Phase 2:**  
  - **K-Means clustering** → Identify low-benefit clusters.  
  - **Regression** → Predict eco-benefits from DBH & stormwater benefits.  
  - **Decision Tree Classification** → Label sites as High / Medium / Low benefit.  
  - **MapReduce** → Aggregate eco-benefits by district.  
  - **Geospatial Analysis** → Interactive maps of clusters, priority areas, and recommendations.  

---

##  Results
- **Clustering:** Silhouette score = 0.67, Davies–Bouldin = 0.95 (5 clusters).  
- **Regression:** R² ≈ 0.73, MAE = 23.18 (eco-benefits prediction).  
- **Decision Tree:** Accuracy/Precision/Recall ≈ 0.91 for classification.  
- **Priority clusters:** Cluster 1 & 4 identified as low-benefit → top candidates for tree planting.  
- **Recommendations:** Top 10 sites proposed, with trees needed per site to reach $1,000 yearly eco-benefits.

---

##  Visualizations
- DBH Distribution  
- Eco-benefits correlation  
- Cluster Map  
- Heatmap of benefits  
- Top 10 recommended sites  

---

## Quickstart
Clone and open in Jupyter or Colab:

bash-
git clone https://github.com/tarungangadhar/tree-planting-sites.git
cd tree-planting-sites
jupyter notebook code/phase_1.ipynb 

pip install pyspark folium matplotlib seaborn pandas scikit-learn

---

## Data

Source: Buffalo Tree Inventory

Features: DBH, CO₂ benefits, stormwater gallons saved, council district, etc.

~133,230 records, 28 columns.

---

## Future Work

Integrating tree species recommendation.

Estimating oxygen yield per species.

Scaling method to other cities for smart urban planning.
