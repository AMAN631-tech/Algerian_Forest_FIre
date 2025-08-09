# Algerian_Forest_FIre

##  Project Overview
This project uses the **Algerian Forest Fire Dataset** to explore patterns, relationships, and predictions for **Fire Weather Index (FWI)** — an important indicator for forest fire risk.

The workflow includes:
- **Exploratory Data Analysis (EDA)**
- **Feature Engineering**
- **Data Preprocessing**
- **Regression Modeling** (Linear Regression, Ridge, Lasso, ElasticNet, and their Cross-Validated versions)
- **Model Evaluation**

---

##  Dataset
The **Algerian Forest Fire Dataset** contains meteorological and fire-related attributes collected from two regions in Algeria: **Bejaia** and **Sidi Bel-abbes**.

### **Columns**
- `Temperature` (°C) – Daily temperature
- `RH` (%) – Relative humidity
- `Ws` (km/h) – Wind speed
- `Rain` (mm/m²) – Rainfall
- `FFMC` – Fine Fuel Moisture Code
- `DMC` – Duff Moisture Code
- `DC` – Drought Code
- `ISI` – Initial Spread Index
- `BUI` – Buildup Index
- `FWI` – Fire Weather Index (**Target Column**)

---

##  Exploratory Data Analysis (EDA)
- Checked for **missing values**
- Visualized distributions using **histograms, boxplots, KDE plots**
- Correlation heatmap to identify **relationships between variables**
- Regional comparison between Bejaia and Sidi Bel-abbes

---

##  Feature Engineering
- Converted categorical features to numerical (if applicable)
- Removed or imputed missing values
- Feature scaling using **StandardScaler**
- Splitting into **training** and **testing** sets

---

##  Models Applied
We trained multiple regression models to predict **FWI**.

### **1. Linear Regression**
- Baseline model for comparison.

### **2. Ridge Regression**
- L2 regularization to reduce overfitting.

### **3. Lasso Regression**
- L1 regularization for feature selection.

### **4. ElasticNet Regression**
- Combination of L1 and L2 regularization.

---

##  Cross-Validation Versions
For each Ridge, Lasso, and ElasticNet model, **CV versions** (`RidgeCV`, `LassoCV`, `ElasticNetCV`) were used to:
- Automatically find the optimal regularization parameter **alpha**
- Improve generalization performance

---

##  Model Evaluation Metrics
For each model:
- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **R² Score**

---

##  Requirements
```bash
pandas
numpy
matplotlib
seaborn
scikit-learn
