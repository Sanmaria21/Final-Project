# Final-Project
This project focuses on predicting sleeping disorders using machine learning techniques applied to lifestyle and health-related data. By analyzing various factors such as sleep duration, blood pressure, stress levels, physical activity, and demographic information, the model aims to identify patterns that indicate the presence of sleep disorders like insomnia and sleep apnea. The dataset undergoes thorough preprocessing, feature selection, and scaling to improve model accuracy. This work demonstrates how data-driven approaches can assist in early detection and better understanding of sleep health, potentially supporting medical diagnosis and personalized lifestyle interventions.

File Name : JUNE 16 - contains EDA and feature selection methods
CODE DETAILS:
Necessary libraries are imported , dataset was loaded successfully. 
Preprocessing done: Missing values handling, removing duplicates, blood pressure split, label encoding, feature-target split, and feature scaling. 
1. EDA:

Graph 1: Distribution of Stress Level
This bar graph shows how frequently each stress level (from 3 to 8) appears in the dataset.It shows the number of people of each stress levels. 

Graph 2 : Stress Level by Gender
This box plot compares stress levels between males and females. 

Graph 3: Sleep Duration by Sleep Disorder Category
The box plot compares sleep duration distributions across three sleep disorder categories: No Sleeping Disorders, Sleep Apnea, and Insomnia.

Graph 4: Correlation Heatmap
This heatmap provides a visual overview of the linear relationships (correlation 
coefficients) between all numeric variables in the dataset. 

Graph 5: Sleep Duration VS Stress Level
The scatter plot titled "Sleep Duration vs Stress Level (by Sleep Disorder)" visualizes how stress levels vary with sleep duration across different sleep disorders.

Graph 6: Sleep Disorder Distribution
The bar chart shows the frequency of sleep disorder categories: Not Known, Sleep Apnea,and Insomnia.

2.FEATURE SELECTION METHODS:
SelectKBest Feature Selection Method
The horizontal bar chart titled SelectKBest Feature Scores (chi2) ranks features based on their relevance to the target variable using chi-squared scores.
Correlation heatmap method (default)
The heatmap identifies and removes highly correlated features(|r|>0.9).

Final features selected after considering both feature selection methods : Disystolic, Sleep Duration, Quality of Sleep, Heart Rate, Age, Sleep Disorder, Systolic. 

File Name - MODEL1- contains model 1 - logistic regression
 
MODEL 1- LOGISTIC REGRESSION

HYPERTUNING METHOD : GRIDSEARCH 
Grid Search for parameters like eta0, alpha,and penalty is done to find the best parameter value. 
Training the model with early stopping is done and model is stabilize. The plotting of loss over epoch and accuracy over epoch is also found. 

PLOTTING:
Line plots:
Plots the training and testing loss over epochs.
Plots the training and testing accuracy over epochs.

Prediction and Metrics:
Makes predictions on the test set.
Prints a classification report (precision, recall, F1-score).
Displays a confusion matrix heatmap.

AUC
Uses label_binarize to handle multi-class ROC computation.
Displays an overall AUC score using roc_auc_score with multi_class

File Name: ALL_3_MODELS-contains all 3 models for the project


MODEL 2 - RANDOM FOREST
Imported necessary libraries for the model.
Grid Search for parameters like n_estimators,max_depth,min_samples_split,min_samples_leaf and bootstrap is done to find the best parameter value. 
Training the model with early stopping is done and model is stabilize.

PLOTTING:
Line plots:
Plots the Random Forest Log Loss vs. Number of Estimators.
Plots the Random Forest Accuracy vs. Number of Estimators.

Prediction and Metrics:
Makes predictions on the test set.
Prints a classification report (precision, recall, F1-score).
Displays a confusion matrix heatmap.


AUC
Uses label_binarize to handle multi-class ROC computation.
Displays an overall AUC score using roc_auc_score with multi_class

MODEL 3- SVM
Imported necessary libraries for the model.
Grid Search for parameters like eta0, alpha,and penalty is done to find the best parameter value.
Training the model with early stopping is done and model is stabilize.

PLOTTING:
Line plots:
Plots the training and testing loss over epochs.
Plots the training and testing accuracy over epochs.

Prediction and Metrics:
Makes predictions on the test set.
Prints a classification report (precision, recall, F1-score).
Displays a confusion matrix heatmap.


AUC
Uses label_binarize to handle multi-class ROC computation.
Displays an overall AUC score using roc_auc_score with multi_class

COMPARISON PLOTS 
PLotted a bar chart to compare model accuracies.
Plotted a bar charts for macro and weighted averged to comapre model precision,recall,and f1 score
Plotted a line graph to show the ROC comparison.
Plotted a bar chart for AUC comparison
