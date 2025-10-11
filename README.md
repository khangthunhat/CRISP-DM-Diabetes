# CRISP-DM-Diabetes
A data analytics project following the CRISP-DM methodology to analyze and predict the risk of diabetes using clinical health data.

🩺 Diabetes: EDA, Hypothesis Testing, and Predictions with Python

📘 Overview

This project focuses on analyzing diabetes health data and building predictive models to identify individuals at risk of diabetes.
The workflow follows the CRISP-DM framework and includes exploratory data analysis (EDA), hypothesis testing, feature engineering, and classification modeling with techniques to handle class imbalance.

By leveraging survey data from the Behavioral Risk Factor Surveillance System (BRFSS 2015), the project aims to provide insights into key health and lifestyle factors associated with diabetes and develop accurate screening models.


🎯 Objectives
	•	Explore and understand the BRFSS 2015 dataset.
	•	Conduct EDA and hypothesis testing to identify significant factors associated with diabetes.
	•	Build classification models to predict diabetes status (binary or multiclass).
	•	Apply resampling and class weighting to address class imbalance.
	•	Evaluate models using metrics such as ROC-AUC, F1-score, Recall, and Precision.


🧭 CRISP-DM Workflow

1. Business Understanding
	•	Early diabetes detection is critical for timely intervention and cost reduction.
	•	Objective: Predict diabetes risk using behavioral and demographic data instead of lab tests.
	•	Questions:
	•	Which factors most strongly predict diabetes risk?
	•	Can we build a lightweight screening model using a small set of features?

2. Data Understanding
	•	Source: BRFSS 2015
	•	253,680 samples, 21 health features, 1 target variable (Diabetes_binary or Diabetes_012)
	•	Includes demographics, lifestyle, and health indicators (e.g., BMI, HighBP, HighChol).
	•	Data is mostly clean and complete; class imbalance present (≈14% positive).

3. Data Preparation
	•	Checked for missing values, outliers, and data types.
	•	Encoded categorical features (ordinal / binary).
	•	Scaled continuous variables (BMI, MentHlth, PhysHlth).
	•	Split into train/test (80/20) with stratification.
	•	Applied class weighting and SMOTE for imbalance handling.

4. Modeling
	•	Models implemented:
	•	Logistic Regression
	•	Random Forest
	•	Gradient Boosting / XGBoost
	•	Hyperparameter tuning via GridSearchCV or RandomizedSearchCV.
	•	Evaluated with cross-validation and multiple metrics.

5. Evaluation
	•	Compared models by ROC-AUC, F1, and Recall.
	•	Feature importance / SHAP values used for interpretability.
	•	Identified key risk factors: BMI, HighBP, GenHlth, DiffWalk, Age.

6. Deployment (Optional)
	•	Model serialized using joblib.
	•	Example Streamlit / Flask app can be added for screening demo.


📊 Key Insights
	•	Overweight (BMI > 30), high blood pressure, poor general health, and mobility difficulty are top predictors.
	•	Lifestyle factors (physical activity, diet, smoking) show moderate association.
	•	Education and income correlate negatively with diabetes risk.
	•	Balanced training (via class weighting or SMOTE) improves recall significantly.


🧰 Tech Stack
	•	Language: Python
	•	Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn, scipy, shap
	•	Workflow: Jupyter Notebook / Google Colab
	•	Methodology: CRISP-DM


📂 Project Structure
```
📦 diabetes-eda-prediction
│
├── 📜 README.md
├── 📘 Diabetes_EDA_Hypothesis_Predictions.ipynb
├── 📄 requirements.txt
└── 📂 data/
    ├── diabetes_binary_health_indicators_BRFSS2015.csv
    └── diabetes_012_health_indicators_BRFSS2015.csv
```
🧠 Future Work
	•	Extend to multiclass prediction (Diabetes_012).
	•	Explore ensemble stacking and feature selection.
	•	Deploy lightweight web app for community screening.
	•	Integrate fairness analysis to ensure equitable predictions across groups.

🙌 Acknowledgements
	•	Dataset by Alex Teboul on Kaggle, derived from CDC BRFSS 2015.
	•	Inspired by Zidian Xie et al., “Building Risk Prediction Models for Type 2 Diabetes Using Machine Learning Techniques.”


Bạn có muốn mình tạo thêm một file requirements.txt tương ứng cho dự án (liệt kê các thư viện cần cài đặt) không?