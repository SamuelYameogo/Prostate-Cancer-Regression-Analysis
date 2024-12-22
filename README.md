# Prostate Cancer Regression Analysis

This project focuses on analyzing the *Prostate Dataset* to predict prostate cancer outcomes using multiple regression models. The analysis includes thorough data preprocessing, exploratory data analysis (EDA), and model evaluation to determine the most effective regression approach. Below is an overview of the project structure and methodology.

---

## Dataset
The dataset used in this project is `prostate_dataset.txt`, which contains clinical and demographic data related to prostate cancer patients. Key features include:
- `lcavol`, `lweight`, `age`, `lpsa`, `lbph`, `lcp`: Continuous variables
- `svi`, `pgg45`, `gleason`: Categorical variables

---

## Key Steps

### 1. Data Preprocessing
- Removed unnecessary columns (`col`, `train`).
- Handled outliers using the Interquartile Range (IQR) method, replacing them with the mean for small datasets.
- Standardized continuous variables using `StandardScaler`.

### 2. Exploratory Data Analysis (EDA)
- Visualized distributions of key variables using histograms and boxplots.
- Checked for normality using Shapiro-Wilk tests and Q-Q plots.
- Examined correlations between variables using Pearson and Spearman methods.
- Generated pairwise scatterplots and pie charts for categorical data.

### 3. Regression Models
The following models were evaluated:
- **Linear Regression**
- **Ridge Regression** (L2 regularization)
- **Lasso Regression** (L1 regularization)
- **Elastic Net** (Combination of L1 and L2)

#### Model Selection
- Evaluated models using Mean Squared Error (MSE) as the primary metric.
- Tuned hyperparameters for Ridge, Lasso, and Elastic Net using cross-validation and grid search.

---

## Results
1. Ridge Regression: Achieved optimal performance with a tuned `alpha`.
2. Lasso Regression: Improved sparsity with the best `alpha`.
3. Elastic Net: Achieved the lowest MSE with optimized `alpha` and `l1_ratio`.

---

## Deployment
- The best-performing Elastic Net model was saved using `joblib` for future predictions.
- Example: Prediction of `lpsa` for a new patient after scaling and feature alignment.

---

## How to Use
1. Clone this repository.
2. Ensure all dependencies are installed: `pip install -r requirements.txt`.
3. Run the notebook or Python script to execute the analysis.

---

## Files in Repository
- `prostate_dataset.txt`: The dataset.
- `prostate_analysis.ipynb`: Main Jupyter Notebook with the full analysis.
- `elastic_net_model.pkl`: Saved Elastic Net model.
- `requirements.txt`: List of required Python libraries.

---

## Future Enhancements
- Extend the analysis with additional models (e.g., Support Vector Regression).
- Incorporate more robust methods for handling outliers.
- Visualize feature importance for better interpretability.

---

## Dependencies
- Python 3.8+
- Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, SciPy, Joblib

Install dependencies with:
```bash
pip install -r requirements.txt
```

---

## License
This project is licensed under the MIT License.

