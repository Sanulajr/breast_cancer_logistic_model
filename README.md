# Breast Cancer Classification

This project aims to classify breast cancer as malignant or benign using several machine learning algorithms. The dataset used is the Breast Cancer Wisconsin (Diagnostic) dataset, available in `sklearn.datasets`. Multiple models were evaluated, with Logistic Regression achieving the highest accuracy of 98%.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Requirements](#requirements)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Model Comparison](#model-comparison)
- [Results](#results)
- [Future Improvements](#future-improvements)

## Project Overview

The objective of this project is to build a classification model that can accurately detect the likelihood of breast cancer based on various diagnostic features. The following steps were taken:

1. Data Loading and Exploration
2. Data Visualization
3. Data Preprocessing
4. Model Training and Evaluation
5. Model Comparison and Selection

## Dataset

The Breast Cancer Wisconsin (Diagnostic) dataset contains 569 samples, each with 30 features. Each sample is labeled as either malignant (1) or benign (0). This dataset is well-suited for binary classification tasks.

## Requirements

To run this project, install the following Python libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib
```

## Project Structure

- `breast_cancer_classification.ipynb`: Jupyter Notebook containing code for data exploration, preprocessing, model training, and evaluation.
- `breast_cancer_logistic_model.pkl`: Saved Logistic Regression model (created after tuning for best performance).
- `README.md`: Documentation of the project.

## Usage

1. Clone the repository and navigate to the project directory.

   ```bash
   git clone <repository-url>
   cd breast_cancer_classification
   ```

2. Open the Jupyter Notebook to run and explore the code.

   ```bash
   jupyter notebook breast_cancer_classification.ipynb
   ```

3. To evaluate all models, run each cell sequentially. The final output will display each model's accuracy and a bar chart comparing their performances.

4. (Optional) If you wish to load the saved Logistic Regression model and make predictions on new data:

   ```python
   import joblib

   # Load model
   model = joblib.load('breast_cancer_logistic_model.pkl')

   # Predict on new data
   prediction = model.predict(new_data)
   ```

## Model Comparison

Seven models were evaluated for this project:

- Logistic Regression
- K-Nearest Neighbors
- Decision Tree
- Random Forest
- Support Vector Machine
- Naive Bayes
- Gradient Boosting Classifier

Each model was trained on a training set and evaluated on a test set. Logistic Regression performed best with an accuracy of 98%.

## Results

| Model                  | Accuracy |
|------------------------|----------|
| Logistic Regression    | 0.98     |
| Gradient Boosting      | 0.97     |
| Random Forest          | 0.96     |
| Support Vector Machine | 0.96     |
| K-Nearest Neighbors    | 0.95     |
| Naive Bayes            | 0.94     |
| Decision Tree          | 0.92     |

**Final Model**: The Logistic Regression model was saved as `breast_cancer_logistic_model.pkl` for easy deployment or future predictions.

## Future Improvements

1. **Hyperparameter Tuning**: Additional tuning could improve the model's robustness.
2. **Ensemble Methods**: Combining top-performing models might yield even higher accuracy.
3. **Model Interpretability**: Using tools like SHAP and LIME to interpret the predictions and gain insights into important features for each prediction.
