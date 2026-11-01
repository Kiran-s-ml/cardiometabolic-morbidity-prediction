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

### **Train-Test Split and Feature Scaling**

- The dataset was divided into training (80%) and testing (20%) sets using `train_test_split`.
- A random state of 42 was used to ensure reproducibility.
- Feature scaling was performed using `StandardScaler`.
- The scaler was fitted on the training data and subsequently applied to the test data to maintain consistency and avoid data leakage.

### **Handling Class Imbalance**

The Synthetic Minority Over-sampling Technique (SMOTE) was applied to the training data for Logistic Regression and Support Vector Machine (SVM) to address class imbalance.

SMOTE generates synthetic observations for the minority class. The test dataset was kept unchanged during this process.

The remaining nine machine learning models were trained using the original training data without applying SMOTE.
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

All 11 machine learning models were evaluated using a common set of classification metrics to compare their predictive performance.

The evaluation metrics included:

- Accuracy
- Sensitivity (Recall)
- Specificity
- Precision
- F1-score
- Negative Predictive Value (NPV)
- Balanced Accuracy
- Matthews Correlation Coefficient (MCC)
- Cohen's Kappa
- Area Under the ROC Curve (ROC-AUC)
- Area Under the Precision-Recall Curve (PR-AUC)

Confusion matrices, ROC curves, Precision-Recall curves, and classification reports were also used to assess model performance.
## **Explainable Artificial Intelligence (XAI)**

SHAP (SHapley Additive exPlanations) was used to interpret machine learning predictions.

The analysis helps to:

- Identify important predictors.
- Understand the contribution of individual features to model predictions.
- Examine how predictor values influence model outputs.
- Improve the interpretability of machine learning models.

**Results and Model Comparison**

The performance of all 11 machine learning models was compared using multiple classification metrics.

The key findings were:

- **XGBoost** achieved the highest accuracy (0.7120), balanced accuracy (0.6528), MCC (0.3414), and Cohen's Kappa (0.3286).
- **ANN** achieved the highest sensitivity (0.4570), F1-score (0.5292), and NPV (0.7342).
- **Gradient Boosting** achieved the highest ROC-AUC (0.7457) and PR-AUC (0.2619).
- **Decision Tree** achieved the highest specificity (0.9995) and precision (0.7778), but had very low sensitivity (0.0032).

Overall, XGBoost demonstrated the strongest performance across several evaluation metrics, while ANN and Gradient Boosting performed better on selected measures.

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

