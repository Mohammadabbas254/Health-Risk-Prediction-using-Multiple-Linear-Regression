🩺 Health Risk Prediction (Multiple Linear Regression)

- Project Overview :

  This project predicts a patient's disease progression score (one year after baseline) using clinical and lifestyle variables. By leveraging the Scikit-learn Diabetes Dataset, the model identifies which physiological factors—such as BMI, Blood Pressure, and Glucose levels—most significantly influence health risks.

- Key Features :
  
    Predictive Modeling: Uses Multiple Linear Regression to estimate a continuous health risk score.

    Feature Analysis: Identifies the strongest drivers of disease progression (e.g., Glucose and BMI).

    Statistical Validation: Includes p-value analysis and R² scoring to ensure model reliability.

    Interactive "What-If" Scenarios: A custom function to simulate risk scores for hypothetical patient profiles.
  
- Dataset Summary

  The dataset includes 442 patient records with 10 normalized baseline features:
      Category,Features
      Demographics,"Age, Sex"
      Vital Signs,"Body Mass Index (BMI), Average Blood Pressure (BP)"
      Blood Serum,"Total Cholesterol (TC), LDL, HDL, TCH Ratio, Glucose, Insulin"
      Target,Disease Progression Score (Range: 25 – 346)


- Tech Stack
    Language: Python
    Libraries: * pandas & numpy: Data manipulation
    seaborn & matplotlib: Data visualization (heatmaps, scatter plots)
    scikit-learn: Model training, scaling, and evaluation
    statsmodels: Statistical significance testing (OLS)

- Model Performance
  The model explains approximately 45.3% of the variance in disease progression. While linear regression provides a strong baseline, the complexity of clinical data suggests that non-linear factors also play a role.
  Core Insights
  Strongest Risk Increasers: Glucose ($\beta \approx +35.16$) and BMI ($\beta \approx +25.61$).
  Protective Factors: Serum Cholesterol showed a negative correlation ($\beta \approx -44.45$) in this specific normalized model.
  Significant Drivers: BMI, Blood Pressure, Sex, and Glucose all maintained high statistical significance ($p < 0.05$).

- How to Use
  Exploratory Data Analysis: Run the EDA cells to visualize correlations via the heatmap and check the target distribution.
  Training: The model uses StandardScaler to ensure all features are on the same scale before fitting the LinearRegression model.
  Scenario Testing: Use the predict_risk() function to input custom values and see how specific lifestyle changes might impact the predicted risk score.
    Note: The input features in this notebook are normalized. For clinical use with raw units (e.g., mmHg for BP), a de-normalization step or a model trained on raw units would be required.

- Limitations
  Linearity: Assumes a straight-line relationship; may underfit if the biological progression is non-linear.
  Sample Size: Based on 442 patients; larger datasets are recommended for broader clinical generalizability.

  Images:

  <img width="1301" height="589" alt="Screenshot 2026-05-06 234557" src="https://github.com/user-attachments/assets/1e482d88-4da6-4014-b7b3-0e7d00cc4e02" />

<img width="1697" height="625" alt="Screenshot 2026-05-06 234618" src="https://github.com/user-attachments/assets/83f76622-4934-432b-a799-0ae2a9858b87" />
<img width="831" height="630" alt="Screenshot 2026-05-06 234644" src="https://github.com/user-attachments/assets/48c94d11-d97d-435b-abb7-470c576f022e" />

  <img width="885" height="643" alt="Screenshot 2026-05-06 234654" src="https://github.com/user-attachments/assets/2a65fe17-4570-402b-8d0e-a5e124b19c3f" />
