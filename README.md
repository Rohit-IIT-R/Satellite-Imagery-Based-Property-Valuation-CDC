# Satellite Imagery-Based Property Valuation

##  Project Overview
This project leverages **Multimodal Machine Learning** to estimate property values. Unlike traditional models that rely solely on tabular data (square footage, bedrooms, year built), this approach integrates **satellite imagery embeddings** to capture "invisible" neighborhood features like green cover, road density, and urban layout.

**Author:** Rohit Kumar 23119035
**Affiliation:** IIT Roorkee  

---

##  Methodology

### 1. The Data
* **Tabular Data:** 16,000+ records containing structural details (bedrooms, bathrooms, sqft, etc.).
* **Visual Data:** High-resolution satellite images (processed into embeddings using `EfficientNetB0`).

### 2. The Pipeline
1.  **Exploratory Data Analysis (EDA):** * Geospatial visualization using **Mapbox** to map price hotspots.
    * Correlation analysis using `Magma` themed heatmaps.
2.  **Baseline Model:** * XGBoost Regressor trained on 18 tabular features.
3.  **Hybrid Model (Final):**
    * Concatenates tabular features with **1280-dimensional image embeddings**.
    * Uses PCA for dimensionality reduction before feeding into the regressor.

---

##  Repository Structure
* ├── data_fetcher.ipynb # Fetches satellite / external data
* ├── preprocessing.ipynb # Data cleaning & feature engineering
* ├── model_trained.ipynb # Final model 
* ├── train.csv # Training dataset (public, small)
* ├── test.csv # Test dataset (public, small)
* ├── requirements.txt # Project dependencies
* └── README.md
