**Chronic Kidney Disease Data Analysis and Feature Reduction**

**Overview:**

This project focuses on analyzing and reducing features in a Chronic Kidney Disease (CKD) dataset from the UCI Machine Learning Repository. The aim is to improve classification accuracy using feature selection and reduction techniques on clinical data, which includes both numerical and categorical indicators of CKD.


**Dataset:**

The dataset contains 400 patient samples with 24 features, including:

- Numerical features like blood pressure, glucose levels, and hemoglobin.

- Categorical features such as the presence of hypertension, diabetes, and coronary artery disease.

- The target variable (class) indicates CKD presence, making the dataset suitable for classification tasks.


**Project Structure:**

The code is organized into distinct sections for clarity, each explained with accompanying comments, visualizations, and tables.


**Key Sections:**

**- Data Preprocessing**

  - Handling missing values by replacing numerical NaNs with column means and categorical NaNs with the mode.
  - Encoding categorical features using LabelEncoder and normalizing all features with Min-Max Scaling.

**- Feature Selection Techniques:**

  - Filter Method: Selected top features using Chi-squared statistics.
  - Forward and Backward Feature Selection: Sequential selection techniques to add or remove features based on their predictive power.
  - Hybrid Selection: Combined forward and backward selection to balance inclusion and exclusion of features.
  - Principal Component Analysis (PCA): Reduced dimensionality by transforming features into principal components, retaining 95% of cumulative variance.

**- Classification with MED (Minimum Euclidean Distance):**

  - A custom MED classifier was implemented, calculating distances between samples and class centroids for predictions.

**Evaluation:**

  - Accuracy of each feature selection method was compared, with Forward and Hybrid Selection achieving the highest accuracy (0.9625).


**Results Summary:**
  - Feature selection improved model accuracy significantly compared to baseline.
  - PCA, while effective for dimensionality reduction, achieved lower accuracy due to potential loss of detailed information.
  - Key features like blood glucose (bgr) and hemoglobin (hemo) were consistently identified as crucial across multiple methods.
