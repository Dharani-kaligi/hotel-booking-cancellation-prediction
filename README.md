# 🏨 Hotel Booking Cancellation Prediction using Machine Learning

## 📌 Project Overview

Hotel booking cancellations can lead to revenue loss, inefficient room allocation, and operational challenges. This project predicts whether a hotel booking will be canceled using Machine Learning. The solution helps hotels identify high-risk bookings and take proactive measures to minimize cancellations.

This project demonstrates a complete end-to-end Machine Learning workflow, including data preprocessing, exploratory data analysis (EDA), feature engineering, model building, hyperparameter tuning, and business-driven model selection.

---

## 🎯 Business Problem

Hotel booking cancellations affect occupancy planning and revenue management. By predicting cancellations in advance, hotels can:

- Improve room allocation
- Reduce revenue loss
- Identify high-risk bookings
- Take preventive actions such as reminder emails or promotional offers

---

## 📂 Dataset

**Dataset:** Hotel Booking Demand Dataset

**Target Variable**

| Value | Meaning |
|-------|---------|
| 0 | Booking Not Canceled |
| 1 | Booking Canceled |

---

# 🛠️ Project Workflow

## 1️⃣ Data Preprocessing

- Loaded dataset
- Checked data types
- Handled missing values
- Removed duplicate records
- Removed unnecessary columns

---

## 2️⃣ Exploratory Data Analysis (EDA)

### Univariate Analysis

- Distribution of categorical features
- Distribution of numerical features

### Bivariate Analysis

- Categorical Features vs Target
- Numerical Features vs Target

### Correlation Analysis

- Correlation Heatmap
- Multicollinearity Check

---

## 📊 Key Business Insights

- Customers with previous cancellations are more likely to cancel again.
- Customers with previous successful bookings are less likely to cancel.
- Customers making more booking changes are less likely to cancel.
- Customers requesting parking are significantly less likely to cancel.
- Customers making more special requests are less likely to cancel.
- Long lead-time bookings have a higher chance of cancellation.
- Deposit type and customer type influence booking cancellation.

---

## ⚙️ Feature Engineering

- One-Hot Encoding
- Train-Test Split

---

# 🤖 Model Building

Algorithm Used:

✅ Random Forest Classifier

Reasons for choosing Random Forest:

- Handles nonlinear relationships
- Robust to outliers
- Works well with mixed data types
- Less prone to overfitting
- Provides Feature Importance

---

# 🔍 Hyperparameter Tuning

RandomizedSearchCV was used to optimize the Random Forest model.

### Tuned Parameters

- n_estimators
- max_depth
- min_samples_split
- min_samples_leaf
- max_features
- bootstrap
- class_weight

---

# 📈 Model Performance

| Metric | Baseline Model | Tuned Model |
|---------|---------------:|------------:|
| Accuracy | **85.45%** | **85.70%** |
| Precision | 78.82% | **79.10%** |
| Recall | 64.49% | **65.33%** |
| F1 Score | 70.94% | **71.56%** |
| ROC-AUC | 0.91 | **0.91** |

---

# 📉 Model Evaluation

The model was evaluated using:

- Confusion Matrix
- Classification Report
- ROC Curve
- ROC-AUC Score
- Feature Importance

---

# ✅ Final Model Selection

The Hyperparameter Tuned Random Forest was selected as the final model because it achieved improvements in:

- Accuracy
- Precision
- Recall
- F1 Score

Although overall accuracy is important, the business objective of this project required reducing **False Negatives (Type II Errors)**.

A False Negative occurs when the model predicts that a booking will not be canceled, but the customer actually cancels. Missing such cancellations can prevent hotels from taking proactive measures, resulting in inefficient room allocation and potential revenue loss.

Therefore, recall was considered an important evaluation metric while selecting the final model.

---

# 💼 Business Recommendations

- Monitor customers with previous cancellations more closely.
- Pay special attention to bookings with long lead times.
- Identify high-risk bookings using the prediction model.
- Send reminder emails or promotional offers to customers likely to cancel.
- Improve occupancy planning based on predicted cancellation risk.

---

# 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

# 📁 Project Structure

```
Hotel-Booking-Cancellation-Prediction/
│
├── data/
├── images/
├── notebooks/
├── Hotel_Booking_Cancellation.ipynb
├── requirements.txt
└── README.md
```

---

# 🚀 Future Improvements

- Compare with XGBoost and LightGBM
- Perform threshold tuning to improve recall
- Build an end-to-end prediction pipeline
- Deploy the model using Streamlit

---

## 👩‍💻 Author

**Dharani Kaligi**

Data Engineer | Aspiring Data Scientist | Machine Learning Enthusiast

If you found this project useful, feel free to ⭐ this repository.
