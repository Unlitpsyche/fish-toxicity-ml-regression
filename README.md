# FISH TOXICITY ML REGRESSION
QSAR-based Fish Toxicity Prediction using Regression Models in Python

# OVERVIEW
This project reflects my early steps in machine learning, where I implemented and evaluated regression techniques to deepen my understanding.
It predicts fish toxicity (LC50) using regression models, based on six molecular descriptors of chemical compounds. LC50 measures the concentration required to kill 50% of a test fish population, important for environmental safety assessments.

# DATASET
Size: 908 samples, 7 columns

# FEATURES

CIC0 (information index)

SM1_Dz(Z) (2D matrix, some zero/invalid values)

GATS1i (2D autocorrelation)

NdsCH, NdssC (atom-type counts)

MLOGP (molecular property)

Target: LC50 [-LOG(mol/L)] (the toxicity label)

# WORKFLOW
Data Checking: Loaded and explored for missing or zero values, and outliers.

Cleaning: Filled missing/zero values using medians; removed outliers (IQR method).

Feature Scaling: Standardized features for fair comparison.

Model Building: Tested multiple regressors:

Linear Regression, Ridge, Lasso

Decision Tree

SVR (Support Vector Regressor)

Hyperparameter Tuning: Manually optimized alpha (Ridge), max_depth/min_samples_leaf (Decision Tree), and C (SVR).

Ensemble Models: Compared Bagging, Random Forest, and AdaBoost.

Evaluation: Used R², MAE, and RMSE for model performance.

# RESULT
Best Single Model: SVR (C=10) gave the strongest R² (~0.60), lowest error.

Best Overall: Random Forest performed best overall:

R²: ~0.60

MAE: ~0.70

RMSE: ~0.96

Lasso: Performed poorly with R² near zero.

Generalization: Random Forest and SVR generalized well to new data.

# FINAL CONCLUSION
Random Forest is the most suitable model for predicting fish LC50 given this dataset.

Data cleaning, scaling, and careful model selection/tuning are critical for robust results.

# HOW TO USE
Clone/download the repository and install Python dependencies (see requirements.txt).

Place your dataset CSV in the project directory.

Run main.ipynb or the main Python script step-wise to see data processing, model building, and outputs.

# CONTRIBUTORS
This project was developed as a group academic assignment.

# REFERENCE
Samanipour, S. et al. (2023). "From molecular descriptors to intrinsic fish toxicity..." Environmental Science & Technology.

# LICENSE
MIT License — use freely, with attribution.
