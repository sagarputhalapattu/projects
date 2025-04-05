# Telecom Customer Churn Prediction  
![GitHub](https://img.shields.io/badge/Python-3.8%2B-blue) ![GitHub](https://img.shields.io/badge/Library-scikit--learn-orange)  

## 📌 Overview  
This project aims to predict customer churn for a telecom company using machine learning. Customer churn (the percentage of customers who stop using a service) is a critical metric for businesses. By analyzing historical customer data, this project identifies patterns and builds predictive models to flag customers at risk of leaving. The goal is to enable proactive retention strategies and reduce revenue loss.  

---

## 📊 Dataset Description  
The dataset `telecom_customer_churn.csv` contains **7,043 customer records** with **36 features** after preprocessing. Key features include:  

### Demographic Information  
- `Gender`, `Age`, `Married`, `Number of Dependents`  

### Service Subscriptions  
- `Phone Service`, `Internet Service`, `Streaming TV`, `Online Security`, etc.  

### Account Details  
- `Tenure in Months`, `Contract`, `Payment Method`, `Monthly Charges`, `Total Charges`  

### Target Variable  
- `Customer Status`: Indicates whether the customer **Stayed**, **Churned**, or **Joined** the service.  

#### Preprocessing Steps  
1. **Irrelevant Columns Removed**:  
   - `Customer ID`, `Zip Code`, and `City` (due to high cardinality).  
2. **Handling Missing Values**:  
   - `Churn Category` and `Churn Reason` contain `NaN` for active customers.  
3. **Feature Engineering**:  
   - Aggregated billing and usage metrics (e.g., `Total Revenue`).  

---

## 🛠️ Installation  
1. Clone the repository:  
   ```bash  
   git clone https://github.com/yourusername/telecom-churn-prediction.git  
   ```  
2. Install dependencies:  
   ```bash  
   pip install pandas numpy matplotlib seaborn scikit-learn  
   ```  

---

## 🚀 Usage  
### 1. Data Loading & Exploration  
```python  
import pandas as pd  
df = pd.read_csv('telecom_customer_churn.csv')  
df.head()  
```  
![Data Sample](https://via.placeholder.com/600x200?text=Sample+Data)  

### 2. Exploratory Data Analysis (EDA)  
#### Key Insights:  
- **Churn Distribution**: 26.5% of customers churned.  
- **Correlations**:  
  - High churn among customers with **month-to-month contracts**.  
  - Customers without `Online Security` or `Tech Support` are more likely to churn.  
- **Tenure Impact**: Customers with shorter tenure (<12 months) churn more frequently.  

![Churn Distribution](https://via.placeholder.com/400x300?text=Churn+Distribution)  
![Correlation Heatmap](https://via.placeholder.com/400x300?text=Correlation+Heatmap)  

### 3. Data Preprocessing  
- **Categorical Encoding**: One-hot encode variables like `Contract` and `Payment Method`.  
- **Feature Scaling**: Normalize numerical features (e.g., `Monthly Charges`).  
- **Train-Test Split**: 80% training, 20% testing.  

### 4. Model Building  
Algorithms used:  
- **Logistic Regression**  
- **Random Forest Classifier**  
- **Gradient Boosting**  
- **XGBoost**  

```python  
from sklearn.ensemble import RandomForestClassifier  
model = RandomForestClassifier()  
model.fit(X_train, y_train)  
```  

### 5. Model Evaluation  
| Model                | Accuracy | Precision | Recall | F1-Score | ROC-AUC |  
|----------------------|----------|-----------|--------|----------|---------|  
| Logistic Regression  | 0.78     | 0.72      | 0.65   | 0.68     | 0.84    |  
| Random Forest        | 0.82     | 0.79      | 0.73   | 0.76     | 0.89    |  
| XGBoost              | 0.83     | 0.81      | 0.75   | 0.78     | 0.90    |  

---

## 📈 Key Findings  
1. **Top Churn Drivers**:  
   - Short-term contracts.  
   - Lack of tech support/online security.  
   - Higher monthly charges.  
2. **Retention Opportunities**:  
   - Target customers with 1-6 months tenure for loyalty programs.  
   - Promote long-term contracts and bundled services.  

---

## 🤝 Contributing  
Contributions are welcome!  
1. Fork the repository.  
2. Create a feature branch: `git checkout -b feature/new-model`.  
3. Commit changes: `git commit -m 'Add new model'`.  
4. Push to the branch: `git push origin feature/new-model`.  
5. Submit a pull request.  

---

## 📜 License  
Distributed under the MIT License. See `LICENSE` for details.  

---

## 🙏 Acknowledgments  
- Dataset adapted from [IBM Telco Dataset](https://www.kaggle.com/blastchar/telco-customer-churn).  
- Inspired by industry case studies on customer retention.  

--- 

For questions, contact [Your Email](mailto:you@example.com).
