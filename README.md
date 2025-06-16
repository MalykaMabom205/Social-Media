# Social Media Addiction and Usage Datasets

## Overview
# Social Media Addiction Score Prediction

This project uses machine learning to predict social media addiction scores among students based on behavioral, demographic, and psychological data.

---

## 📁 Dataset Files

- `cleaned_social_media_usage.csv`  
- `cleaned_Students Social Media Addiction.csv`

These datasets include features such as daily usage hours, platform preference, sleep hours, mental health scores, and self-reported social media addiction impact.

---

## 🧹 Data Cleaning & Preprocessing

- Removed duplicates and ID columns (`Student_ID` excluded from model)  
- Handled missing values with removal or imputation  
- One-hot encoded categorical variables (Gender, Academic Level, Relationship Status)  
- Scaled numerical features where applicable  
- Selected only relevant numerical and encoded features for modeling

---

## 🧠 Machine Learning

- **Model Used:** Random Forest Regressor  
- **Target Variable:** `Addicted_Score`  
- **Train-Test Split:** 85% training, 15% test  
- **Evaluation Metrics:** MAE, RMSE on validation set  

---

## 📊 Final Predictions & Confidence Intervals

The final model predicts addiction scores on test data and includes 90% confidence bounds estimated from ensemble trees.

| Column                    | Description                               |
|---------------------------|-------------------------------------------|
| `Predicted_Addicted_Score`| Rounded predicted score (2 decimal places)|
| `Lower_90%_Bound`         | Estimated 10th percentile of predictions  |
| `Upper_90%_Bound`         | Estimated 90th percentile of predictions  |

---

## 📂 Output File

- `social_media_addiction_predictions.csv` — predictions with confidence intervals

---

## 📈 Visualizations

*(Add your charts here)*

- Distribution of features before and after scaling  
- Actual vs predicted addiction scores  
- Feature importance from the Random Forest model

![Feature Importance Example](images/feature_importance.png)  
![Prediction Distribution](images/prediction_distribution.png)  

*(Replace with your actual plots or notebook output snapshots)*

---

## 🚀 Getting Started

### Prerequisites

- Python 3.7+  
- Required packages (can install via pip):

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
