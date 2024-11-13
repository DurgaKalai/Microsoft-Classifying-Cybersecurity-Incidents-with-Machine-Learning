# Microsoft-Classifying-Cybersecurity-Incidents-with-Machine-Learning
# Objective
 Develope a machine learning model to improve Security Operation Centers (SOCs) by accurately predicting the triage grade of cybersecurity incidents using the GUIDE dataset. The model should classify incidents as true positive (TP), benign positive (BP), or false positive (FP), based on historical data and customer feedback. The goal is to support SOC analysts with context-rich recommendations, enhancing overall security. 
# Skills take away
- Data Preprocessing and Feature Engineering
- Machine Learning Classification Techniques
- Model Evaluation Metrics (Macro-F1 Score, Precision, Recall)
- Cybersecurity Concepts and Frameworks (MITRE ATT&CK)
- Handling Imbalanced Datasets
- Model Benchmarking and Optimization
# Domain
Cybersecurity and Machine Learning
# Business Use Cases:
- Security Operation Centers (SOCs)
- Incident Response Automation
- Threat Intelligence
- Enterprise Security Management
# Approach:
 Data Exploration
* Initial Inspection: Load train.csv, examine feature types (categorical, numerical), and assess the target variable distribution (TP, BP, FP).
* Exploratory Data Analysis (EDA): Visualize data to identify patterns, correlations, and anomalies, especially class imbalances.
 Data Preprocessing:
* Handle Missing Data: Identify missing values and apply imputation or removal strategies.
* Feature Engineering: Create new features or transform existing ones (e.g., timestamp features, normalization).
* Encode Categorical Variables: Apply one-hot encoding or label encoding based on feature characteristics.
   Data Splitting:
* Train-Validation Split: Split train.csv into training and validation sets (e.g., 80-20), using stratification if the target is imbalanced.
 Model Selection & Training:
* Baseline Model: Start with a simple model (e.g., logistic regression) to set a performance benchmark.
* Advanced Models: Experiment with models like Random Forest, XGBoost, or Neural Networks. Tune hyperparameters via grid or random search.
* Cross-Validation: Implement k-fold cross-validation to ensure robust model performance.
 Model Evaluation & Tuning:
* Evaluate Metrics: Use macro-F1 score, precision, and recall on the validation set to assess model performance.
* Hyperparameter Tuning: Optimize model hyperparameters based on initial evaluation.
* Handle Class Imbalance: Apply techniques like SMOTE or class weights to improve minority class performance.
 Model Interpretation:
* Feature Importance: Use SHAP values or permutation importance to identify key features.
* Error Analysis: Examine misclassifications to inform improvements.
 Final Evaluation on Test Set:
* Test Evaluation: Assess the final model on test.csv using the same performance metrics.
* Comparison to Baseline: Compare performance on the test set with baseline and validation results.
  Documentation & Reporting:
* Document Process: Provide a summary of methods, challenges, and results.
* Recommendations: Suggest integration into SOC workflows, future improvements, and deployment considerations.
# Results: 
Various machine learning models were implemented and compared using the macro-F1 score, precision, recall, and other metrics. These models include:
Comparison report:

![comparison table](https://github.com/user-attachments/assets/0031a513-faf1-45e6-83a4-c2d32f365730)

# Applying SMOTE to the Training Data for Class Imbalance and Hyperparameter Tuning
SMOTE generates synthetic samples of the minority class (e.g., true positives) by interpolating between existing minority class examples. This helps balance the class distribution and prevents the model from being biased toward the majority class.
results after smote:

![Screenshot 2024-11-13 221318](https://github.com/user-attachments/assets/b06529de-80c4-4492-8ad9-40a5c03a7fea)

# Conclusion
The Random Forest model has demonstrated superior performance in classifying cybersecurity incidents, outpacing alternative models through its robust accuracy and adaptability. This project not only establishes a reliable framework for incident classification but also delivers a scalable solution tailored for Security Operations Center (SOC) teams.

