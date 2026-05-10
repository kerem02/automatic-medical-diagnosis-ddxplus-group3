# Automatic Medical Diagnosis - DDXPlus Dataset

This project was prepared for the Introduction to Machine Learning course.

## Project Goal

The goal of this project is to predict the pathology of a patient using the DDXPlus medical diagnosis dataset.

## Dataset

The dataset used in this project is DDXPlus. It contains synthetic patient records with age, sex, evidences, initial evidence, and pathology labels.

The dataset files used in the notebook are:

- train.csv
- validate.csv
- test.csv
- release_conditions.json
- release_evidences.json

The dataset files are not included in this GitHub repository because they are large. Here is the drive link for dataset: https://drive.google.com/drive/folders/1eO7pTV3HKdk77n18I_90Iqvaxi4cJo8i?usp=drive_link

## Models Used

Three machine learning models were trained and compared:

- Logistic Regression
- Decision Tree
- Random Forest

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

## How to Run

1. Download the DDXPlus dataset.
2. Upload the dataset folder to Google Drive.
3. Open the notebook in Google Colab.
4. Update the dataset path if needed.
5. Run the cells from top to bottom.
