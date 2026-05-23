# Diabetes Health Indicator Analysis

## Overview
This project analyzes diabetes-related health indicators and trains classification models to predict diabetes status. It uses a public health dataset with demographic, behavioral, and medical indicator features. The notebook compares preprocessing methods and reports class-level model performance.

## Motivation
Health-related classification projects are valuable for practicing imbalanced classification, metric interpretation, and responsible limitation writing. This project demonstrates why accuracy alone can be misleading when some health classes are much harder to predict than others.

## Dataset
- **Source:** BRFSS 2015 diabetes health indicators dataset.
- **File:** `data/diabetes_012_health_indicators_BRFSS2015.csv`
- **Target variable:** diabetes status encoded as `0.0`, `1.0`, and `2.0`.
- **Important features:** TODO: add major health indicator features after rerunning notebook.
- **Dataset size:** TODO: add dataset size after rerunning notebook.
- **Known limitations:** Public health survey data may include sampling bias, self-reporting bias, and class imbalance.

## Methods
- Loaded and inspected the diabetes health indicators dataset.
- Compared preprocessing approaches.
- Trained classification models.
- Evaluated with accuracy, precision, recall, and F1-score.

## Results
The notebook reports approximately **0.8483 accuracy** for two methods. However, the class-level report shows very weak performance for class `1.0`, including zero precision and recall in the displayed output.

This is an important limitation: the model appears to perform well overall because the majority class dominates the dataset.

## Key Insights
- Accuracy is not enough for imbalanced health classification.
- Minority-class recall needs major improvement before the model can be considered useful.
- The project is strongest when framed as metric analysis and model-diagnosis practice.

## Limitations
- This is not a medical diagnostic model.
- The model performs poorly on at least one minority class.
- The notebook does not yet include class balancing, threshold tuning, or cross-validation.
- Dataset collection and clinical validity are not documented in this repository.

## Future Improvements
- Add class distribution plots.
- Try class weighting, resampling, and better baselines.
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
