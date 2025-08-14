📌 Project Overview

This project aims to analyze a diabetes dataset and build classification models to predict whether a patient has diabetes ("Yes") or not ("No").
Both numerical and categorical features are considered, and different preprocessing methods are compared to assess their impact on model performance.

The work involves:

Exploratory data analysis (EDA)

Preprocessing numerical and categorical data

Building and comparing multiple classification models

Evaluating accuracy, precision, recall, and F1-score

📂 Dataset

The dataset contains patient health-related data with both numerical (e.g., glucose level, BMI) and categorical features (e.g., gender, smoking status).
The target variable is "diabetes" with two possible values:

Yes → Patient has diabetes

No → Patient does not have diabetes

🛠 Methods

We tested three approaches for preprocessing and model training:

Method 1 – Combined Preprocessing Pipeline

Used ColumnTransformer to apply:

StandardScaler for numerical features

OneHotEncoder for categorical features

Trained a RandomForestClassifier in a single pipeline

Accuracy: ~0.85

Method 2 – Manual Encoding + Scaling

Manually:

Encoded categorical variables using pd.get_dummies

Scaled numerical columns with StandardScaler

Trained a RandomForestClassifier

Accuracy: ~0.85

Method 3 – Numerical Only

Used only numerical columns with StandardScaler

Ignored categorical features

Trained a RandomForestClassifier

Accuracy: ~0.65

📊 Model Comparison
Method	Categorical Data Used	Preprocessing Type	Accuracy	Notes
1	✅ Yes	Pipeline (OneHot + Scaling)	0.85	Fully automated pipeline
2	✅ Yes	Manual (GetDummies + Scaling)	0.85	Similar to Method 1 but manual steps
3	❌ No	Scaling only	0.65	Ignoring categorical features hurt performance
⚙️ Technologies Used

Python

pandas

numpy

scikit-learn

matplotlib / seaborn (for EDA)

📈 Conclusion

Including categorical features significantly improves model performance (from ~0.65 to ~0.85).
Both pipeline-based and manual preprocessing methods yield similar results, but pipelines are generally more maintainable and less error-prone.
