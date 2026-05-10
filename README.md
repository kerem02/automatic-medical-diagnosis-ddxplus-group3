# Automatic Medical Diagnosis - DDXPlus Dataset

This project was prepared for the Introduction to Machine Learning course.

## Project Goal

The goal of this project is to predict the pathology of a patient using the DDXPlus medical diagnosis dataset.

This is a supervised multi-class classification problem because the target variable is `PATHOLOGY`, and the dataset contains multiple disease classes.

## Dataset

The dataset used in this project is DDXPlus. It contains synthetic patient records with age, sex, evidences, initial evidence, differential diagnosis, and pathology labels.

The dataset files used in the notebook are:

- train.csv
- validate.csv
- test.csv
- release_conditions.json
- release_evidences.json

The dataset files are not included in this GitHub repository because they are large.

Dataset Drive link:
https://drive.google.com/drive/folders/1eO7pTV3HKdk77n18I_90Iqvaxi4cJo8i?usp=drive_link

## Exploratory Data Analysis

Basic exploratory data analysis was performed before model training. The notebook includes:

- Dataset size check
- Missing value check
- Number of pathology classes
- Top 10 most common pathologies
- Pathology distribution graph
- Age distribution graph
- Sex distribution graph
- Number of evidences per patient

## Preprocessing

The following preprocessing steps were applied:

- The `EVIDENCES` column was converted from text into Python lists.
- Evidences were converted into binary features.
- `SEX` and `INITIAL_EVIDENCE` were converted using one-hot encoding.
- `PATHOLOGY` was converted into numerical labels.
- The `DIFFERENTIAL_DIAGNOSIS` column was not used as an input feature because it contains diagnosis-related information.

## Models Used

Three machine learning models were trained and compared:

- Logistic Regression
- Decision Tree
- Random Forest

For the Decision Tree model, different `max_depth` values were tested and the best value was selected according to validation performance.

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Matthews Correlation Coefficient
- Confusion Matrix

## Best Model

Based on the validation results, Logistic Regression was selected as the best model and evaluated on the test set.

Random Forest also performed very well, while Decision Tree had slightly lower performance compared to the other two models.

## Feature Importance

Feature importance was also checked using the Random Forest model. The most important features were mostly evidence-based features, which is expected because symptoms and antecedents are strongly related to the pathology.

## Limitations

The results are very high, but they should be interpreted carefully. DDXPlus is a synthetic and structured dataset, so the relationship between evidences and pathology may be cleaner than in real hospital data.

Also, this project uses the full evidence list of each patient. In a real diagnosis setting, all evidences may not be known at the beginning. Therefore, the results show model performance on this dataset, not real clinical performance.

## How to Run

1. Download the DDXPlus dataset.
2. Upload the dataset folder to Google Drive.
3. Open the notebook in Google Colab.
4. Update the dataset path if needed.
5. Run the cells from top to bottom.
