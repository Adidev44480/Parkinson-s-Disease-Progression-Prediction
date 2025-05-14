# Parkinson-s-Disease-Progression-Prediction
This project aims at identifying the progression of Parkinson's disease using Speech-based Assessments reducing patient's inconvenience and healthcare cost.
This project is a Regression project done under the kind supervision of Dr. Monika Bhattacharjee, Department of Mathematics, Indian Institute of Technology Bombay. 

The details and workflow of the Projects are given below:

# Data
The data used for this project is `parkinsons_updrs.csv`. The data contains 5875 voice recording observations of patients with early-stage Parkinson's disease. There are 18 columns: `age`, `sex`, `16 biomedical voice measures`, and `total_updrs`. `total_updrs` is a measure for the progression and severity of Parkinson's disease.

# Methodology
1. **Data Preprocessing**:
   * Dropped irrelevent columns `id` and `motor_updrs`
   * `sex` column was converted to `binary` datatype
   * Feature Scaling
2. **Exploratory Data Analysis (EDA)**
   * KDE of `total_updrs`
   * Pair plot
   * Heatmap/Correlation matrix
3. **Detected multicollinearity using:**
   * Correlation matrix `|r| > 0.8`
   * Variance Inflation Factor `VIF > 10`
   * Condition Number `Cn > 50`
4. **Fitted Linear Regression Model**
   * Identified outliers using:
     - DFFITS
     - DFBETAS
     - Cook's Distance
5. **Retrained the Linear Regression Model on filtered data**
    * Performed residual analysis
    * Residual vs Fitted value plot
    * Q-Q plot of residual
6. **Regualrization regression model**
   * Ridge regression (L2)
   * Lasso regression (L1)
   * Identified most significant features
7. **Applied Random Forest Regressor**
   * To check for futher improvement in the results

# Dependencies
* numpy
* pandas
* scikit-learn
* matplotlib
* seaborn
* statsmodels 
