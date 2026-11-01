# Cardiometabolic Morbidity Prediction in Older Indian Adults Using Machine Learning

## **Project Overview**

This project explores the application of machine learning techniques to identify important predictors of cardiometabolic morbidity among older adults in India.

The study uses data from the Longitudinal Ageing Study in India (LASI), with an analytical sample of 59,689 individuals. Multiple machine learning algorithms were developed and evaluated to examine their ability to predict cardiometabolic morbidity.

The project also uses SHAP (SHapley Additive exPlanations) to interpret model predictions and understand the contribution of different factors.

**Research Status:** Manuscript submitted and currently under review.

## **Research Objectives**

The main objectives of this study are:

1. To identify important demographic, socioeconomic, behavioural, and health-related factors associated with cardiometabolic morbidity among older Indian adults.
2. To develop and compare multiple machine learning models for predicting cardiometabolic morbidity.
3. To evaluate model performance using appropriate classification metrics.
4. To interpret model predictions using SHAP to identify influential predictors.

## **Dataset Description**

- **Dataset:** Longitudinal Ageing Study in India (LASI).
- **Data Source:** International Institute for Population Sciences (IIPS), Mumbai.
- **Study Population:** Indian adults aged 45 years and above.
- **Analytical Sample Size:** 59,689 individuals.
- **Data Type:** Demographic, socioeconomic, behavioural, and health-related variables.
- **Target Variable:** Cardiometabolic morbidity.

Cardiometabolic morbidity is defined as the presence of at least one of the following five conditions:

- Hypertension
- Diabetes
- Cardiovascular disease
- Stroke
- High cholesterol

The original LASI dataset is not included in this repository. Researchers should obtain access through the official data source.

## **Data Preprocessing**

The dataset underwent preprocessing before model development. The preparation process included:

The initial data preparation involved:

Checking missing values across variables using their counts and percentages.

Separating the dataset into independent variables (18 predictors) and the dependent variable (CMD).

Examining the distribution of the target classes to understand the proportion of individuals with and without cardiometabolic morbidity.

- Data cleaning and preparation.
- Handling missing observations.
- Selection and preparation of predictor variables.
- Definition of the target variable.
- Splitting the data into training and testing sets.
- Applying appropriate preprocessing techniques for machine learning algorithms.

## **Machine Learning Models**

Eleven machine learning algorithms were considered for model development and comparison:

1. Logistic Regression
2. Support Vector Machine (SVM)
3. Artificial Neural Network (ANN)
4. Decision Tree
5. Random Forest
6. K-Nearest Neighbours (KNN)
7. Naive Bayes
8. Gradient Boosting
9. AdaBoost
10. XGBoost
11. CatBoost

## **Model Evaluation**

The models were evaluated using classification performance metrics to compare their predictive capabilities.

The evaluation included metrics such as:

- Accuracy
- Precision
- Sensitivity (Recall)
- Specificity
- F1-score
- Area Under the ROC Curve (AUC)
- Matthews Correlation Coefficient (MCC)

Confusion matrices and ROC curves were also used to examine model performance.

## **Explainable Artificial Intelligence (XAI)**

SHAP (SHapley Additive exPlanations) was used to interpret machine learning predictions.

The analysis helps to:

- Identify important predictors.
- Understand the contribution of individual features to model predictions.
- Examine how predictor values influence model outputs.
- Improve the interpretability of machine learning models.

## **Results and Visualizations**

The repository includes visualizations generated during the analysis, including:

- Confusion matrices
- ROC curves
- Feature importance plots
- SHAP summary plots
- SHAP heatmaps
- Partial dependence plots
- Model comparison visualizations

These visualizations provide insights into model performance and the contribution of different predictors.

## **Repository Structure**

```text
cardiometabolic-morbidity-prediction/
│
├── final_code.ipynb
├── README.md
│
└── images/
    ├── Confusion matrices
    ├── ROC curves
    ├── SHAP visualizations
    └── Other model visualizations
```

## **Technologies Used**

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- SHAP
- XGBoost
- CatBoost

## **How to Run the Project**

1. Clone the repository:

```bash
git clone https://github.com/Kiran-s-ml/cardiometabolic-morbidity-prediction.git
```

2. Navigate to the project directory:

```bash
cd cardiometabolic-morbidity-prediction
```

3. Install the required Python libraries.

4. Open the Jupyter Notebook:

```bash
jupyter notebook final_code.ipynb
```

5. Provide the LASI dataset locally, following the file path and format expected by the notebook.

6. Run the notebook cells in sequence.

**Note:** The dataset is not included in this repository due to data access restrictions.

## **Research Status**

The research manuscript based on this project has been submitted and is currently under review.

## **Acknowledgements**

The study uses data from the Longitudinal Ageing Study in India (LASI), conducted by the International Institute for Population Sciences (IIPS), Mumbai, in collaboration with its research partners.

