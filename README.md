<img width="659" height="538" alt="image" src="https://github.com/user-attachments/assets/0ee904e8-48a8-4c48-8d31-20f4660b39b6" />**Project Overview**

This project, "Enhancing Wind Farm Operational Efficiency Through Power Output Classification Using MLP and Ensemble Models", presents a machine learning–based framework that reframes wind turbine power forecasting from a regression problem into a multi-class classification task.
By classifying turbine power output into low, medium, and high categories, the study enables actionable insights for maintenance scheduling, underperformance detection, and operational optimization. The framework leverages SCADA (Supervisory Control and Data Acquisition) data from a utility-scale wind farm and evaluates multiple ML models — Logistic Regression (LR), Random Forest (RF), Gradient Boosting (GB), XGBoost, and Multilayer Perceptron (MLP) — to identify the most effective classifier for turbine power level prediction.

**Key Steps**

Used Kaggle’s Wind Turbine SCADA dataset containing 50,530 records of turbine operational data (10-minute intervals). Reframed continuous power output into three categorical levels: Low, Medium, and High. Analyzed feature statistics and relationships among Wind Speed, Theoretical Power Curve, and Active Power. Verified the physical consistency of turbine performance using correlation and scatter plots.

Data Preprocessing: Replaced negative power values with zero (physically impossible values). Applied IQR outlier capping, feature normalization (Z-score), and label encoding for the target variable. Excluded LV ActivePower (target leakage prevention) and Date/Time (non-predictive).

Model Development & Optimization: Trained five ML classifiers — LR, RF, GB, XGBoost, and MLP. Conducted Grid Search with cross-validation to find optimal hyperparameters. Evaluated models using Accuracy, Precision, Recall, and F1-score on 80-20 stratified train-test split.

Feature Importance Analysis: Compared feature utilization across tree-based and neural models. Identified Wind Speed and Theoretical Power Curve as the most influential predictors.

**Key Findings**

Top Performance: MLP (Multilayer Perceptron) achieved the highest classification accuracy (93.51%), outperforming all ensemble models. Ensemble methods (RF, GB, XGBoost) also performed strongly, with accuracies between 93.3–93.5%.
<img width="659" height="538" alt="image" src="https://github.com/user-attachments/assets/8f68a755-674d-44a7-b50d-47fb91efa4cc" />

Model Insights: Tree-based models relied primarily on Wind Speed and Theoretical Power Curve, while MLP distributed its focus more evenly across all features — improving generalization.

Operational Value: Classification-based modeling improves interpretability, making it easier for wind farm operators to identify underperforming turbines, plan maintenance, and optimize energy dispatch.

Future Directions: Integrating real-time SCADA streaming, additional meteorological variables, and deep learning architectures (e.g., CNN, RNN). Extending the framework for fault diagnosis and predictive maintenance in renewable energy systems.
