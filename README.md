# Social Media Addiction Analysis and Prediction

This project aims to analyze and predict student social media addiction using behavioral, demographic, and psychological data. It combines two datasets to build a machine learning model capable of estimating addiction levels based on usage patterns and self-reported factors.

## Notebooks

### Social Media Analysis Notebook  
This notebook contains the end-to-end workflow including data exploration, preprocessing, feature engineering, and the machine learning pipeline used to predict social media addiction scores.

## Datasets

### 1. `Students Social Media Addiction.csv`  
This dataset includes survey responses from students about their social media habits, mental well-being, and self-assessed addiction scores.

### 2. `SocialMediaUsage6.csv`  
This dataset provides detailed usage metrics including:
- Average daily time spent on social media  
- Number of posts, likes, and follows per day  
- Platform or application preferences  

## Data Cleaning and Preparation for Machine Learning

### Cleaning Steps  
- Missing values were handled through removal or imputation depending on the feature's importance.  
- Categorical variables such as gender and platform were standardized and converted to appropriate types.  
- Outliers in features such as `Daily_Minutes_Spent` and `Posts_Per_Day` were identified and removed based on distribution analysis.

### Rescaling  
Rescaling was performed to improve model performance:  
- StandardScaler was applied to features with approximately normal distributions such as `Usage_Hours` and `Sleep_Hours`.  
- MinMaxScaler was applied to features with skewed or bounded distributions such as `Likes_Per_Day` and `Follows_Per_Day`.

### One-Hot Encoding  
Categorical features including `Platform`, `Gender`, and `Device` were encoded using one-hot encoding to make them suitable for machine learning algorithms.

## Machine Learning

### Problem Formulation  
This task is framed as a regression or classification problem to estimate a student's social media addiction level based on behavior and survey data.

### Feature Selection and Preprocessing  
- Duplicate rows were removed.  
- Columns that were transformed through one-hot encoding were dropped in their original form.  
- Row identifiers such as `Student_ID` or `User_ID` were excluded from the model.  
- The target variable (`Addiction_Score`) was checked for proper format and encoded if necessary.

### Data Splitting  
The dataset was split into training, validation, and test sets using `train_test_split`. Stratified sampling was considered when applicable.

## Model Training

- A gradient boosting classifier was used as the primary algorithm. Other models may also be tested.  
- Emphasis was placed on building a working model rather than achieving optimal performance at this stage.  
- The model was trained on the training set and validated on the validation set.

## Model Evaluation

- Performance was evaluated using metrics appropriate to the task, such as accuracy, F1-score, or RMSE.  
- A score consistent with a Kaggle-style challenge was computed to assess model generalization.

## Model Application and Submission

The trained model was applied to the final test set. A submission file was generated containing:  
- User identifiers  
- Predicted addiction scores or class labels  

## Summary

This project presents a complete machine learning workflow for analyzing and predicting social media addiction among students. The process includes thorough data cleaning, appropriate feature engineering, model training, and evaluation. The outcome is a model capable of providing insight into patterns of excessive social media use.
