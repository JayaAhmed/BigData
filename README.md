# Data Analysis and Visualization

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

