# Diabetes Health Indicator Analysis

## Overview
I analyzed diabetes-related health indicators and trained classification models to predict diabetes status. I use a public health dataset with demographic, behavioral, and medical indicator features.

## Motivation
I used this project to practice imbalanced classification and metric interpretation. It taught me why accuracy alone can be misleading when some health classes are much harder to predict than others.

## Dataset
- **Source:** BRFSS 2015 diabetes health indicators dataset.
- **File:** `data/diabetes_012_health_indicators_BRFSS2015.csv`
- **Target variable:** diabetes status encoded as `0.0`, `1.0`, and `2.0`.
- **Known limitations:** Public health survey data can include sampling bias, self-reporting bias, and class imbalance.

## Methods
- I loaded and inspected the diabetes health indicators dataset.
- I compared preprocessing approaches.
- I trained classification models.
- I evaluated accuracy, precision, recall, and F1-score.

## Results
My notebook reports approximately **0.8483 accuracy** for two methods. The class-level report shows weak performance for class `1.0`, including zero precision and recall in the displayed output.

## Key Insights
- Accuracy is not enough for imbalanced health classification.
- Minority-class recall needs major improvement before the model can be useful.
- I treat the project as strongest when framed as model diagnosis rather than a polished medical predictor.

## Limitations
- I do not intend this as a medical diagnostic model.
- The model performs poorly on at least one minority class.
- I do not include class balancing, threshold tuning, or cross-validation yet.
- Dataset collection and clinical validity are not documented in this repository.

## Future Improvements
- Add class distribution plots.
- Try class weighting, resampling, and stronger baselines.
- Report macro-F1 and balanced accuracy.
- Add a model card emphasizing non-clinical use.

## How to Run
```bash
git clone https://github.com/BobbY-24/Diabete_Data_Analysis.git
cd Diabete_Data_Analysis
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook notebooks/diabetes_data_analysis.ipynb
```
