# US Seatbelts Exploratory Data Analysis & Advanced Modeling
**Course Project**  
**Author**: Karan Rajesh  
**Registration Number**: 23BDS0277  
**Notebook Name**: 23BDS0277_EDA_Project_Phase1.ipynb

---

## 📌 Project Overview
This project presents a multi-phase, rigorous statistical investigation, unsupervised pattern recognition pipeline, predictive modeling framework, and reinforcement learning conceptualization applied to the **USSeatBelts** dataset. The dataset tracks key traffic safety, regulatory policies, socioeconomic, and demographic metrics across 50 US States from 1983 to 1997.

---

## 🛠️ Project Structure & Methodology

### 🔹 Phase 1: Data Ingestion, Data Preprocessing & Initial EDA
* **Ingestion**: Raw data is loaded from the public repository and structural profiles are established using high-level DataFrame metadata.
* **Cleaning**: Column alignments are performed. Row identifier artifacts (`rownames`) are deleted, and duplicates are checked and resolved.
* **Imputations**: Missing values (primarily concentrated within the `seatbelt` usage column) are imputed robustly using column-wise medians for continuous attributes and modes for categorical indicators.
* **Initial EDA**: Performed univariate, bivariate, and multivariate visualizations using `matplotlib` and `seaborn` (e.g., categorical frequency bar charts, continuous histograms with kernel density estimates, pairwise correlation heatmaps).

### 🔹 Phase 2: Descriptive Statistics, Advanced Visualizations & Unsupervised Benchmarking
* **Descriptive Profiles**: Extracted rigorous shape parameters—including Coefficient of Variation (CV%), Skewness, Kurtosis, and interquartile distributions—to mathematically evaluate non-normality.
* **Temporal Dynamics**: Evaluated trend variations using custom **Sun Ray (Polar Radial) Plots** to analyze year-over-year fluctuations in mean national fatalities.
* **Bivariate & Contingency Testing**: Analyzed regulatory structures (cross-tabulating Speed Limit 65 vs. Speed Limit 70 policies) backed by **Chi-Square Tests of Independence** and strength measurements via **Cramer's V**.
* **Dimensionality Projections**: Developed benchmark **Principal Component Analysis (PCA)** projections, visual loading matrices, and **Parallel Coordinates** maps over scaled features.
* **Clustering Benchmarks (Sample size n=50)**:
  * **K-Means Clustering**: Parameterized via Elbow and Silhouette diagnostics.
  * **Hierarchical Linkages**: Modeled and compared Single, Complete, Average, Centroid, and Ward linkage strategies.
  * **Divisive Partitioning**: Implemented top-down splits utilizing Bisecting K-Means algorithms.
  * **Spectral & MST Clustering**: Extracted topological relationships via Nearest-Neighbor Affinity Graph clustering and custom **Minimum Spanning Tree (MST)** segmentations.
  * **Expectation-Maximization (EM)**: Fit Gaussian Mixture Models (GMM) optimized using AIC/BIC parameters.
  * **Outlier Isolation**: Isolated structural anomalies using **Isolation Forest** modeling.

### 🔹 Phase 3: Advanced Dimensionality Reduction, High-Dimensional Latent Structures & Predictive Modeling
* **Advanced Manifold Learning & Dimension Reduction**:
  * **Exploratory Factor Analysis (FA)**: Derived underlying latent dimensions influencing traffic outcomes, yielding structural factor load patterns.
  * **Multidimensional Scaling (MDS)**: Computed non-linear distance preservation maps to inspect policy separation patterns.
  * **t-SNE (t-Distributed Stochastic Neighbor Embedding)**: Projected high-dimensional structures onto a 2D map to optimize cluster isolation and discover neighborhood policy groups.
* **Model-Based Unsupervised Partitioning & Outliers**:
  * Implemented Spectral Clustering alongside GMM Density Thresholding (lower 5% density boundaries) to serve as a robust model-based outlier diagnostic tool.
* **Predictive Supervised Modeling**:
  * Constructed a **Multiple Linear Regression** model targeting the continuous response variable (`fatalities`).
  * Performed training/testing splits ($80/20$), computed model coefficients, and assessed accuracy through predictive metrics:
    * Mean Absolute Error (**MAE**)
    * Mean Squared Error (**MSE**)
    * Root Mean Squared Error (**RMSE**)
    * Coefficient of Determination (**$R^2$ Accuracy Score**)
  * Rendered actual-vs-predicted diagnostic visualizations and residual error distribution plots.
* **Reinforcement Learning (RL) Framework**:
  * Constructed a simulated decision-policy matrix (**Q-Table**) modeling state-action combinations to define how an agent learns highway safety enforcement policies (e.g., 'Enforce Primary Law' vs. 'No Policy Change' across varying fatality conditions) based on iterative reward optimizations.

---

## 📊 Libraries & Technologies Utilized
* **Data Wrangling**: `pandas`, `numpy`
* **Scientific & Statistical Computation**: `scipy.stats`, `scipy.cluster` 
* **Supervised & Unsupervised Machine Learning**: `scikit-learn` 
* **Information Visualization**: `matplotlib.pyplot`, `seaborn`
