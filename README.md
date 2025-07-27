# Part B: Data Analysis and Visualization

To understand the relationship between various lifestyle and health factors and hair loss, multiple datasets were integrated, cleaned, and analyzed. The final dataset was created by combining information from different sources, followed by several stages of transformation, exploration, and modeling to uncover meaningful insights.

1. Loaded and Combined Datasets:
Multiple CSV files related to hair loss were imported, each containing different attributes such as medical conditions, sleep hours, stress levels, and more. These were combined to form a unified dataset for analysis.

2. Cleaned and Simplified the Data: 
To make the dataset easier to work with, unnecessary columns (e.g., ID, Hair Type) were removed, and some columns were renamed for clarity. A new column, MedicalCondition, was created to indicate whether a person had any medical issue (Yes or No).

3. Converted Text to Numbers:
Categorical text values such as gender and health status were converted into numeric codes, making the dataset compatible with machine learning algorithms.

4. Reclassified Hair Loss:
Simplified the HairLoss data into two categories - people with little to no hair loss, and those experiencing significant hair loss - to make the analysis more meaningful.

5. Explored the Data Visually:
Various visualizations such as bar plots, regression plots, and correlation heatmaps were used to explore how hair loss is associated with factors like stress levels, sleep hours, age, and medical conditions.

6. Model Analysis:
After data preprocessing, machine learning models such as Random Forest and Logistic Regression were applied to identify important features and predict hair loss outcomes. Model performance was evaluated using accuracy, precision, recall, and confusion matrices.


# Part C: Model Selection

To identify which model might work better for the final merged dataset, 7 different models were tested. The models are: 

* Logistic Regression
* Random Forest
* Naive Bayes
* Decision Tree
* Support Vector Machine (SVM)
* XGBoost
* k-Nearest Neighbours (kNN)

For each model, different hyperparameters were tuned across multiple configurations to find the optimal setup. An ablation study was conducted for all models, and each configuration was evaluated using a balanced weighted scoring system based on six performance metrics: F1-score (25%), Recall (20%), Matthews Correlation Coefficient (20%), AUC-ROC (15%), Precision (10%), and Accuracy (10%). This ensured a fair and consistent comparison across models.

After evaluating over 90 total configurations, the XGBoost model emerged as the best performer with the highest weighted score (0.804), showing strong performance in recall, F1-score, and MCC. It was followed closely by Decision Tree (0.801) and Random Forest (0.797). These models were especially effective in capturing complex relationships between features like sleep, stress, and medical condition.

The final results suggest that tree-based ensemble models, especially XGBoost, are most suitable for this classification task due to their high predictive accuracy and ability to model nonlinear interactions.















