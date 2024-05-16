Report: Fetal Health Classification Using Cardiotocogram Data

1. Introduction

1.1 Background
Child and maternal mortality reduction are critical aspects of global health, aligned with the United Nations' Sustainable Development Goals. By 2030, the aim is to end preventable deaths of newborns and children under 5 years, with a target of reducing under‑5 mortality to at least as low as 25 per 1,000 live births. Maternal mortality remains a significant concern, with a majority of deaths occurring in low-resource settings and being preventable.

1.2 Significance of Cardiotocograms (CTGs)
Cardiotocograms (CTGs) offer a cost-accessible method to assess fetal health, playing a pivotal role in preventing child and maternal mortality. These devices utilize ultrasound pulses to measure fetal heart rate (FHR), fetal movements, uterine contractions, and more, providing valuable insights for healthcare professionals to take timely actions.

2. Objectives
The primary goal is to develop a classification model for fetal health using features extracted from CTG exams. The dataset comprises 2126 records classified into three categories: Normal, Suspect, and Pathological by expert obstetricians.
3. Data Description

3.1 Dataset Overview
The dataset consists of 2126 records, each containing features extracted from Cardiotocogram exams. These features are then classified into three classes by expert obstetricians:

•	Normal: Representing healthy fetal conditions.
•	Suspect: Indicating a potential need for further examination.
•	Pathological: Signifying a higher risk, demanding immediate attention.
 
Key:  1 - Normal 2 - Suspect 3 - Pathological
3.2 Features
The features include information related to fetal heart rate, movements, and uterine contractions, among others. The dataset is rich in information crucial for understanding fetal health dynamics.

4. Methodology

4.1 Data Preprocessing
•	Initial data exploration and cleansing to handle any missing or duplicate values.(EDA)
•	Utilization of the SMOTETomek method to address imbalanced classes.
•	Feature normalization through MinMaxScaler.
•	Dropping features with high correlation (>70%) using Pearson correlation.

 

4.2 Model Selection
A range of classification algorithms, including Naive Bayes, Logistic Regression, Decision Tree, Random Forest, K-Nearest Neighbors, Support Vector Machine, and Gradient Boosting, are considered for model development.

4.3 Evaluation Metrics
Common classification metrics such as accuracy, precision, recall, and F1 score will be employed to evaluate model performance.

5. Results
5.1 Model Training
The dataset was divided into training and testing sets to facilitate model training. Various classification algorithms were implemented and fine-tuned, including Naive Bayes, Logistic Regression, Decision Tree, Random Forest, K-Nearest Neighbors, Support Vector Machine, and Gradient Boosting.

5.2 Evaluation Metrics
Multiple evaluation metrics were employed to gauge the performance of each model:
 

5.3 Analysis
Random Forest emerged as the top-performing model.
•	Training Accuracy: 0.999458434876794
•	Testing Accuracy: 0.9780666125101544


To improve the testing accuracy, an exploration of different parameters was conducted:
•	Best Grid Parameters:
{'bootstrap': False,
 'max_depth': None,
 'max_features': 'sqrt',
 'min_samples_leaf': 1,
 'min_samples_split': 2,
 'n_estimators': 300}

Testing Accuracy reached using these best parameters is 0.9829406986190089


5.5 Discussion
Random Forest demonstrated superior performance, emphasizing its potential as the chosen model for fetal health classification. The model maintained a high level of accuracy, indicating its efficiency with reduced complexity.
Random Forest Model Accuracy is 98.29%.

6. Conclusion
This research contributes to the reduction of child and maternal mortality by leveraging Cardiotocogram data for fetal health classification. The development of a robust Random Forest model holds promise for early intervention and improved healthcare outcomes. Further investigations could explore additional features and data sources to refine the model and enhance its applicability in diverse healthcare settings.

7. References
https://www.sciencedirect.com/science/article/pii/S1877050921023541
https://www.kaggle.com/datasets/andrewmvd/fetal-health-classification
