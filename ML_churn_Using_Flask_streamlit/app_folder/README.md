## Project Overview: Telecom Churn Prediction System

This project focuses on predicting customer churn in the telecommunications industry. It provides a comprehensive machine learning solution to help telecom companies identify customers at risk of leaving and take proactive steps to retain them.

### Project Breakdown:
- **Modeling**: Developed a churn prediction model using machine learning techniques like **Random Forest**.
- **Flask API**: Created a **Flask** application that serves the model, allowing real-time predictions.
- **Streamlit Dashboard**: Built an interactive dashboard using **Streamlit** to visualize the model's predictions and insights.

### Key Features:
1. **Churn Prediction**: The model predicts whether a customer is likely to churn based on features like usage patterns, customer service calls, and demographic data.
2. **Real-Time API**: The **Flask API** allows for real-time integration with other systems or applications.
3. **Interactive Dashboard**: The **Streamlit app** provides an easy-to-use interface to analyze customer data and visualize churn predictions.

### Tech Stack:
- **Programming Languages**: Python
- **Machine Learning**: Random Forest (Model stored as a `.joblib` file)
- **Libraries**: Scikit-learn, Pandas, NumPy
- **APIs**: Flask (for backend)
- **Visualization**: Streamlit (for dashboard)
- **Deployment**: Can be deployed on cloud platforms (AWS, Heroku, etc.)

### Setup Instructions:
1. **Model**: The trained model is saved in `telecom_churn_rf_model.joblib`. To load and use it for predictions:
   ```python
   from joblib import load
   model = load('telecom_churn_rf_model.joblib')
   ```

2. **Flask API**:
   - The Flask app (`Telecom-Churn-Flask-App.py`) provides an endpoint for real-time predictions. You can run it using:
     ```bash
     python Telecom-Churn-Flask-App.py
     ```

3. **Streamlit App**:
   - The Streamlit dashboard (`Telecom-Churn-Streamlit-App.py`) provides a graphical interface for making predictions. You can run it using:
     ```bash
     streamlit run Telecom-Churn-Streamlit-App.py
     ```

### How It Works:
1. **Input**: Users provide customer data such as service usage, contract type, payment methods, etc.
2. **Prediction**: The model predicts whether the customer is likely to churn.
3. **Visualization**: The Streamlit dashboard displays the input data and the prediction results in an easy-to-read format.

### Usage Scenarios:
- **Telecom companies** can use this project to proactively address customer churn by identifying high-risk customers.
- **Marketing teams** can target retention strategies based on the predictions.
