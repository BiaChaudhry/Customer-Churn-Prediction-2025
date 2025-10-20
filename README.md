# 🧠 Telco Customer Churn Prediction 2025

Predicting whether a customer will leave (churn) is one of the most important business problems in telecom.
This project performs **exploratory data analysis (EDA)** and builds **machine learning models** to understand and predict customer churn using the **Telco Customer Churn dataset**.

---

## 📊 Project Overview

The goal of this project is to:

* Analyze telecom customer data to find churn patterns
* Visualize key insights with graphs
* Build predictive models (Logistic Regression, Random Forest)
* Evaluate model performance and explain results in business terms

---

## 🧩 Dataset

The dataset contains information about customers, their account details, services subscribed, and whether they churned.

**Key Columns:**

* `gender`, `SeniorCitizen`, `Partner`, `Dependents`
* `tenure`, `MonthlyCharges`, `TotalCharges`
* `Contract`, `PaymentMethod`, `InternetService`
* `Churn` – Target variable (Yes = 1, No = 0)

---

## 🔍 Exploratory Data Analysis (EDA)

### 1. **Churn Distribution**

Shows the number of customers who stayed vs. left.

➡ *Observation:* The dataset is imbalanced — most customers did not churn.

### 2. **Customer Tenure Distribution**

Illustrates how long customers have stayed with the company.

➡ *Observation:* Most customers are new (short tenure), which correlates with higher churn risk.

### 3. **Monthly Charges vs Churn**

Boxplot comparing monthly bills of churned vs non-churned customers.

➡ *Observation:* Customers with higher bills tend to churn more often.

### 4. **Churn Rate by Contract Type**

Bar chart showing churn rates for month-to-month, one-year, and two-year contracts.

➡ *Observation:* Month-to-month customers are most likely to churn — longer contracts help retain users.

### 5. **Correlation Matrix**

Shows relationships between numerical variables.

➡ *Observation:* `tenure`, `TotalCharges`, and `MonthlyCharges` are closely related to churn probability.

---

## 🧠 Machine Learning Models

Two models were trained and compared:

| Model               | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
| :------------------ | :------: | :-------: | :----: | :------: | :-----: |
| Logistic Regression |   ~80 %  |   ~71 %   |  ~62 % |   ~66 %  |  ~0.84  |
| Random Forest       |   ~83 %  |   ~74 %   |  ~68 % |   ~71 %  |  ~0.87  |

➡ **Interpretation:**

* **Accuracy** – How many predictions were correct overall
* **Precision** – Of all predicted churners, how many actually churned
* **Recall** – Of all churners, how many were correctly identified
* **F1-Score** – Balance between precision and recall
* **ROC-AUC** – How well the model distinguishes churn vs. no-churn

✅ **Random Forest performed best**, offering better recall and AUC — crucial for identifying at-risk customers.

---

## 🌟 Feature Importance

Top features driving churn (Random Forest):

1. Contract Type
2. Tenure
3. Monthly Charges
4. Total Charges
5. Payment Method

➡ *Insight:* Short-term contracts and high monthly bills are strong churn indicators.

---

## ⚙️ Tech Stack

* **Python 3.10+**
* **pandas**, **NumPy**
* **matplotlib**, **seaborn**
* **scikit-learn**
* **joblib**

---

## 🚀 How to Run the Project

1. Clone the repository

   ```bash
   git clone https://github.com/BiaChaudhry/Customer-Churn-Prediction-2025.git
   cd Customer-Churn-Prediction-2025
   ```

2. Install dependencies

   ```bash
   pip install -r requirements.txt
   ```

3. Run the analysis

   ```bash
   python churn_analysis.py
   ```

4. The trained model will be saved as

   ```
   models/RandomForest_churn_model.pkl
   ```

---

## 📈 Business Takeaways

* Customers on **month-to-month contracts** are at the highest risk.
* Offering **discounted long-term contracts** can reduce churn.
* **High monthly charges** are a churn trigger — consider personalized retention offers.
* Predictive churn models help customer service teams take **proactive actions**.

---

## 🤝 Connect

💼 GitHub: [BiaChaudhry](https://github.com/BiaChaudhry)
🔗 LinkedIn: [Let's connect](https://linkedin.com/in/biachaudhry1312)

If you find this project useful, please ⭐ the repository!
