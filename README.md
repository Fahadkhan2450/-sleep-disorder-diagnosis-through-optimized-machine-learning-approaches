# Sleep disorder diagnosis through optimized machine learning approaches

An end-to-end Machine Learning pipeline for predicting sleep disorders through comprehensive exploratory data analysis, feature engineering, model comparison, cross-validation, and hyperparameter optimization.



# Abstract

Sleep disorders have become increasingly prevalent due to modern lifestyles, work-related stress, and unhealthy daily routines. Early identification of sleep-related disorders enables healthcare professionals to recommend preventive measures and personalized treatment plans before the condition worsens. Machine learning has emerged as an effective solution for developing predictive healthcare systems by identifying complex relationships among clinical and lifestyle variables.

This project presents a comprehensive machine learning framework for classifying sleep disorders using demographic, physiological, and lifestyle-related features. The study begins with extensive exploratory data analysis (EDA) to understand the structure and characteristics of the dataset, followed by data preprocessing, feature engineering, categorical encoding, and model development.

Several supervised machine learning algorithms— ncluding Logistic Regression, Decision Tree, Random Forest, Gradient Boosting, AdaBoost, and Extreme Gradient Boosting (XGBoost) are trained and evaluated. To ensure reliable performance estimation, Stratified K-Fold Cross Validation is employed. Furthermore, hyperparameter optimization is performed to improve predictive performance and minimize overfitting.

The experimental results demonstrate that ensemble learning techniques outperform conventional classification models for sleep disorder prediction, highlighting their capability to capture complex nonlinear relationships within healthcare data. The project establishes a complete machine learning workflow that can serve as a foundation for intelligent clinical decision-support systems.

---

# Table of Contents

- Dataset Overview
- Data Analysis
- Exploratory Data Analysis
- Data Preprocessing
- Feature Engineering
- Model Development
- Cross Validation
- Hyperparameter Optimization
- Model Evaluation
- Conclusion



# Dataset Overview

The dataset contains demographic, physiological, and lifestyle-related information collected from individuals with different sleep conditions.

## Features

| Feature | Description |
|----------|-------------|
| Person ID | Unique Identifier |
| Gender | Male / Female |
| Age | Age of participant |
| Occupation | Profession |
| Sleep Duration | Average sleep duration |
| Quality of Sleep | Sleep quality score |
| Physical Activity Level | Daily physical activity |
| Stress Level | Reported stress level |
| BMI Category | Body Mass Index category |
| Blood Pressure | Systolic/Diastolic BP |
| Heart Rate | Resting heart rate |
| Daily Steps | Average daily steps |
| Sleep Disorder | Target Variable |



# Data Analysis

Before developing predictive models, the dataset was carefully analyzed to understand its quality, distribution, and characteristics.

## Observation

### Data Types

- The dataset contains **5 categorical (object) columns**.
- Remaining columns are numerical variables.

###  Missing Values

- The **Sleep Disorder (Target Variable)** contains missing values.
- These missing values were inspected before preprocessing.
- Appropriate handling techniques were applied to maintain data integrity.

### Dataset Quality

- Duplicate records were inspected.
- Data types were verified.
- Feature consistency was validated.
- Numerical columns were checked for abnormal values.


# Exploratory Data Analysis (EDA)

Exploratory Data Analysis helps understand feature distributions, class balance, and relationships among variables before model training.


## Blood Pressure Distribution

The Blood Pressure feature was separated into:

- Upper Blood Pressure (Systolic)
- Lower Blood Pressure (Diastolic)

Histogram analysis was performed to study their distributions.

### Upper Blood Pressure Histogram

> **Image Placeholder**


![image alt](https://github.com/Fahadkhan2450/-sleep-disorder-diagnosis-through-optimized-machine-learning-approaches/blob/b84f11dc5ef84c9f1367cd2ebce72a6cff963c8b/Graphs/UpperBP.jpeg)


---

### Lower Blood Pressure Histogram

> **Image Placeholder**

```
[ Insert Histogram Here ]
```

---

## Distribution of Sleep Disorders

The target variable distribution was analyzed to determine class balance.

> **Image Placeholder**

```
[ Insert Disorder Distribution Chart ]
```

---

## Gender-wise Sleep Disorder Analysis

The prevalence of sleep disorders across male and female participants was analyzed.

### Gender Distribution

> **Image Placeholder**

```
[ Insert Gender Distribution Chart ]
```

---

### Sleep Disorder by Gender

> **Image Placeholder**

```
[ Insert Gender vs Disorder Chart ]
```

---

## Categorical Feature Analysis

Each categorical feature was explored to understand its unique values and frequency distribution.

Examples include:

- Gender
- Occupation
- BMI Category
- Sleep Disorder

> **Image Placeholder**

```
[ Insert Categorical Values Chart ]
```

---

## Sleep Disorder vs Stress Level

Stress level is one of the most influential factors affecting sleep quality.

The relationship between stress levels and sleep disorders was visualized.

> **Image Placeholder**

```
[ Insert Stress Level Chart ]
```

---

## BMI Category Distribution by Sleep Disorder

BMI categories were compared across different sleep disorder classes.

This visualization highlights the relationship between obesity, overweight conditions, and sleep disorders.

> **Image Placeholder**

```
[ Insert BMI Category Chart ]
```

---

## Correlation Heatmap

A correlation matrix was generated to understand relationships among numerical variables.

Highly correlated features can significantly influence predictive performance.

> **Image Placeholder**

```
[ Insert Correlation Heatmap ]
```

---

# Data Preprocessing

Before training the machine learning models, the dataset underwent several preprocessing steps.

### Preprocessing Pipeline

- Missing value handling
- Splitting Blood Pressure into two numerical columns
- Label Encoding
- One-Hot Encoding (where required)
- Feature Scaling
- Removing unnecessary columns
- Data type conversion

---

# Train-Test Split

The processed dataset was divided into training and testing datasets.

- Training Set: **80%**
- Testing Set: **20%**

This ensures unbiased evaluation of model performance on unseen data.

---

# Model Development

Multiple supervised machine learning algorithms were trained and compared.

The following classifiers were implemented:

---

## Logistic Regression

A baseline linear classification model used for comparison with more advanced ensemble methods.

---

## Decision Tree Classifier

A tree-based algorithm capable of capturing nonlinear decision boundaries.

---

## Random Forest Classifier

An ensemble learning algorithm that combines multiple decision trees to improve prediction accuracy and reduce overfitting.

---

## Gradient Boosting Classifier

A boosting technique that sequentially improves weak learners by minimizing prediction errors.

---

## AdaBoost Classifier

Adaptive Boosting combines multiple weak learners to create a stronger classifier.

---

## XGBoost Classifier

Extreme Gradient Boosting is a highly optimized boosting algorithm designed for speed, scalability, and improved predictive performance.

---

# Cross Validation

To ensure reliable model evaluation, **Stratified K-Fold Cross Validation** was applied.

Benefits include:

- Reduced overfitting
- Better generalization
- Stable performance estimation
- Improved robustness

Performance metrics were averaged across all folds.

---

# Feature Engineering

Feature engineering was performed to enhance predictive performance.

Techniques include:

- Splitting Blood Pressure into Systolic and Diastolic values
- Encoding categorical variables
- Feature scaling
- Creating meaningful numerical representations
- Removing redundant features
- Selecting informative variables

These transformations improve model learning while preserving important clinical information.

---

# Hyperparameter Optimization

To maximize predictive performance, hyperparameter tuning was performed using **GridSearchCV**.

Each model's important parameters were optimized.

Examples include:

### Random Forest

- Number of Trees
- Maximum Depth
- Minimum Samples Split
- Minimum Samples Leaf

### XGBoost

- Learning Rate
- Maximum Depth
- Number of Estimators
- Subsample Ratio
- Column Sampling

### Gradient Boosting

- Learning Rate
- Maximum Depth
- Number of Estimators

The optimized models demonstrated improved predictive performance compared to their default configurations.

---

# Model Evaluation

Each classifier was evaluated using multiple performance metrics.

Evaluation metrics include:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC Score
- Confusion Matrix
- Cross Validation Accuracy

A comprehensive comparison was conducted to identify the best-performing model for sleep disorder classification.

---

# Conclusion

This project presents a complete machine learning workflow for predicting sleep disorders using demographic, physiological, and lifestyle-related information.

Beginning with extensive exploratory data analysis, the study proceeds through preprocessing, feature engineering, model training, cross-validation, and hyperparameter optimization to build robust predictive models.

The comparison of multiple supervised learning algorithms demonstrates the effectiveness of ensemble techniques in accurately classifying sleep disorders. The resulting workflow provides a scalable framework that can support future research in healthcare analytics, clinical decision support systems, and intelligent sleep monitoring applications.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Jupyter Notebook

---

# Future Work

- Deep Learning (Artificial Neural Networks)
- Explainable AI (SHAP & LIME)
- Feature Selection Techniques
- Model Deployment using Flask/FastAPI
- Real-time Sleep Disorder Prediction System
- Integration with Wearable Health Devices
