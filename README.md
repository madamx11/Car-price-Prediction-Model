# 🚗 Car Price Prediction using Machine Learning

## 📌 Project Overview

This project predicts the selling price of used cars using Machine Learning. The objective was not only to build a regression model but also to understand every stage of a real-world ML workflow—from loading raw data to debugging preprocessing issues, training models, evaluating performance, and interpreting results.

The project was developed as a complete learning exercise where every step was implemented manually instead of relying on automated pipelines.

---

# 🛠 Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Google Colab / Jupyter Notebook

---

# 📂 Dataset Overview

The dataset contains information related to used cars such as:

- Brand / Company
- Model
- Year
- Kilometers Driven
- Fuel Type
- Transmission
- Owner
- Selling Price (Target Variable)

> **Target Variable:** Selling Price

---

# 📚 Project Workflow

## Phase 1 — Data Loading & Understanding

Performed:

- Imported required libraries
- Loaded dataset into Pandas DataFrame
- Used:
  - `head()`
  - `shape`
  - `info()`
  - `describe()`
  - `columns`
  - `isnull().sum()`

### Objective

Understand the dataset before making any modifications.

---

## Phase 2 — Exploratory Data Analysis (EDA)

Performed:

- Distribution plots
- Histograms
- Boxplots
- Correlation analysis
- Feature relationship analysis
- Checked categorical and numerical features separately

### Observations

- Numerical features had different scales.
- Categorical columns required encoding.
- Some columns contained missing values.
- Certain columns required cleaning before model training.

---

## Phase 3 — Data Cleaning

Performed:

- Missing value inspection
- Duplicate checking
- Null handling
- Data type verification
- Feature consistency checks

The dataset was cleaned before feature engineering.

---

## Phase 4 — Feature Engineering

Performed:

- Selected relevant features
- Separated Features (X) and Target (y)
- Encoded categorical variables
- Train-Test Split (80:20)
- StandardScaler for numerical features where required

The preprocessing pipeline ensured that the model could correctly interpret both numerical and categorical data.

---

## Phase 5 — Model Building

The following regression models were implemented and compared:

### Linear Regression

Used as the baseline regression model.

Evaluated using:

- MAE
- MSE
- RMSE
- R² Score

---

### Decision Tree Regressor

Implemented to learn non-linear relationships between car features and price.

Observed overfitting tendencies compared to Linear Regression.

---

## Phase 6 — Model Evaluation

Each model was evaluated using:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

### Understanding the Metrics

- **MAE** → Average prediction error.
- **MSE** → Penalizes larger errors more heavily.
- **RMSE** → Error in the same unit as car price.
- **R² Score** → Explains how well the model fits the data.

During the project, these metrics were analyzed to compare model performance and understand why one model performed better than another.

---

# 📊 Model Comparison

| Model | MAE | MSE | RMSE | R² Score |
|------|------------:|-------------:|------------:|----------:|
| Linear Regression | 171180 | 93,171,700,000 | 305240 | 0.5752 |
| Decision Tree Regression | **94124** | **34,040,000,000** | **184499** | **0.8448** |

### Conclusion from Model Comparison

Based on the evaluation metrics, **Decision Tree Regression significantly outperformed Linear Regression** on this dataset.

- Decision Tree achieved a much lower **MAE**, meaning its average prediction error was substantially smaller.
- The **MSE** and **RMSE** were also considerably lower, indicating fewer large prediction errors.
- The **R² Score improved from 0.5752 to 0.8448**, meaning the Decision Tree model explained approximately **84.5%** of the variance in car prices, compared to **57.5%** for Linear Regression.

Overall, the Decision Tree model provided much more accurate predictions for this dataset, suggesting that the relationship between the input features and the selling price is **non-linear**, which Decision Trees are able to capture more effectively than Linear Regression.

---

# 📈 Visualization

Generated visualizations including:

- Feature distributions
- Correlation plots
- Actual vs Predicted values
- Regression performance graphs

These plots helped verify model behavior and identify issues.

---

# 🐞 Debugging Journey

A major part of this project involved learning how to debug Machine Learning code.

Some of the issues encountered and resolved included:

### 1. Feature Matrix Merge Issue

While preprocessing, `df_features` and `df` were merged incorrectly.

Problems faced:

- Column mismatch
- Incorrect indices
- Shape mismatch
- Duplicate columns

Resolution:

- Verified DataFrame shapes
- Checked column names
- Reset indices where required
- Carefully reconstructed the preprocessing pipeline

---

### 2. Train/Test Shape Errors

Encountered inconsistent feature dimensions after preprocessing.

Solved by verifying:

- Shape of X_train
- Shape of X_test
- Shape after encoding
- Shape after scaling

---

### 3. Scaling Issues

Initially scaling was being applied incorrectly.

Learnt that:

- Fit scaler only on training data.
- Transform test data using the fitted scaler.

---

### 4. Graph Issues

While plotting regression results, graphs initially appeared incorrect.

Debugging involved:

- Verifying prediction arrays
- Checking axes
- Matching actual and predicted values correctly

---

### 5. Notebook Disconnection (Google Colab)

During development, notebook disconnections resulted in variables being removed from memory.

Learnt:

- Runtime memory is temporary.
- Variables like `df` disappear after reconnecting.
- Cells must be executed again to recreate objects.

---

# 💡 Key Learnings

This project helped build practical understanding of:

- Complete Machine Learning workflow
- Data preprocessing
- Exploratory Data Analysis
- Feature Engineering
- Feature Scaling
- Encoding categorical variables
- Regression algorithms
- Model comparison
- Error metrics (MAE, MSE, RMSE, R²)
- Debugging preprocessing pipelines
- Handling DataFrame merge issues
- Understanding overfitting
- Importance of verifying shapes at every stage
- Reading and interpreting regression graphs

---

# ✅ Final Conclusion

This project was more than just predicting car prices—it was a hands-on exercise in understanding how an end-to-end Machine Learning pipeline works.

Beyond building regression models, the biggest takeaway was learning how to debug real-world ML problems. Fixing DataFrame merge issues, preprocessing mistakes, scaling errors, plotting problems, and notebook runtime issues provided practical experience that is difficult to gain from theory alone.

The project strengthened my understanding that successful Machine Learning depends not only on choosing the right algorithm but also on careful data preparation, systematic debugging, and proper evaluation.

---

# 🚀 Future Improvements

Possible future enhancements include:

- Hyperparameter tuning
- Random Forest Regressor
- XGBoost / LightGBM
- Cross Validation
- Feature Selection
- Pipeline automation using `Pipeline`
- Model deployment using Flask or FastAPI

---

# 👨‍💻 Author

**Ayush Dutta**

Machine Learning Project
