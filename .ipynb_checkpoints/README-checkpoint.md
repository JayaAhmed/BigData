# Project Overview

This project builds a supervised ML pipeline to predict hair loss using lifestyle and health signals, primarily sleep hours, stress level, medical condition (incl. type), and demographics. Two public datasets (Kaggle + Mendeley) were integrated and harmonized to study the combined effects of these factors on hair-loss risk.

# Data

From four candidates, two datasets were selected for integration based on relevance and feature quality; the final unified dataset contains diverse variable types suited to classification analysis.

**Preprocessing & Integration:** Irrelevant fields were dropped, column names standardized, and missing values imputed. Key harmonisations included: mapping StressLevel to an ordinal scale, normalising SleepHours to numeric units, converting hair-fall counts to a binary HairLoss label using the median threshold, and removing weak/low-quality predictors. The datasets were then merged into a single table. 
 
**Final feature set:** The unified modelling table retained: SleepHours (numeric), StressLevel (ordinal 1–10), MedicalCondition (binary), MedicalConditionType (categorical), Gender_Male (binary), Age (numeric) and the target HairLoss (binary). Class distribution was relatively balanced, so no re-sampling was applied. 
 
# Methodology

* Preprocessing & Feature Harmonisation: Align schemas, encode categories/ordinals, and prepare a single modelling table.

* Model Suite (7): Logistic Regression, Decision Tree, Random Forest, Naïve Bayes, SVM, k-NN, and XGBoost. Each model underwent hyperparameter tuning before comparison.

* Train/Test Protocol: 75/25 split for hold-out evaluation.

* Evaluation: Six metrics—Accuracy, Precision, Recall, F1, AUC-ROC, MCC—aggregated via a weighted composite score to emphasise health-relevant performance.

# Results

**Best overall:** XGBoost (weighted 0.804) with strong F1, MCC, recall, and solid AUC-ROC—the most balanced option.
  
**Close contenders:** Decision Tree (0.801) and Random Forest (0.797), both handling non-linear interactions well and competitive on recall/AUC.

**Mid pack:** SVM (0.790) and k-NN (0.789) were close but showed precision–recall trade-offs; k-NN was sensitive to scaling/neighbour size.

**Feature signals:** MedicalCondition and MedicalConditionType dominated; SleepHours showed a protective trend; StressLevel elevated risk; Age/Gender weaker.

**Takeaway:** The weighted composite (F1/Recall/MCC-heavy) explains XGBoost’s win. Prefer XGBoost for performance; choose Decision Tree or Random Forest if interpretability is key.


# Limitations

**Compute constraints:** Experiments ran on a MacBook Air (M3, 8 GB), limiting exploration of more computationally intensive models (e.g., deep learning) and extensive cross-validation; higher-performance hardware would enable broader, faster optimisation. 

**Data scope & generalizability:** About 2,700 survey-based records with missing factors (e.g., genetics, detailed nutrition, longitudinal follow-up) constrain comprehensiveness and external validity. 

**Interpretability vs performance:** XGBoost led overall but is less transparent than simpler models, posing adoption challenges in clinical contexts.

# Future work

Incorporate larger, longitudinal datasets, add predictors such as genetics and nutrition, and deepen interpretability methods to support clinical use; with more compute, evaluate heavier models and more exhaustive validation.

  