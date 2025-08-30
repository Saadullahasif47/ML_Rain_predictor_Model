🌦️ Rainfall Prediction Using Machine Learning

This project predicts whether it will rain tomorrow or not, based on real-world weather data and machine learning models.
The pipeline includes data preprocessing, feature engineering, model training, and deployment with a Flask API accessible via an ngrok tunnel.

📂 Project Workflow
1. Dataset Preparation

• Collected weather data with features like temperature, humidity, wind speed, precipitation, clouds, ozone, etc.
• Removed unnecessary columns (like description).
• Applied One-Hot Encoding for categorical variables (city, weather conditions).
• Applied Label Encoding where necessary.
• Normalized numerical features using StandardScaler.
• Handled class imbalance using SMOTE (Synthetic Minority Oversampling Technique).

2. Model Training

• Trained multiple models: Logistic Regression, Random Forest, and XGBoost.
• XGBoost outperformed others with 100% accuracy on the test set.
• Saved the trained model and preprocessing objects (xgb_model_1.pkl, standard_scaler.pkl, encoders).

3. Feature Importance

• Used Random Forest to identify most important weather predictors.
• Top features included: precipitation, probability of precipitation (pop), mid-level clouds.

4. Deployment

• Built a Flask backend that loads the trained model and preprocessors.
• Created a frontend (HTML + JavaScript) for users to enter a city name and check if it will rain tomorrow.
• Connected Flask API with ngrok tunnel to make it accessible over the internet.

🖥️ Tech Stack

• Python (pandas, scikit-learn, XGBoost, imbalanced-learn, joblib)
• Flask for backend
• HTML + CSS + JavaScript for frontend
• Ngrok for deployment

🚀 How It Works

User enters a city name in the web interface.

Flask backend fetches the corresponding weather features, applies preprocessing (scaling + encoding).

Trained XGBoost model makes the rainfall prediction.

Result is displayed with an icon:
• ☔ Rain Expected
• 🌞 No Rain Expected

📌 Key Files

• xgb_model_1.pkl → Trained XGBoost model
• standard_scaler.pkl → Scaler for numeric features
• label_encoder.pkl / onehot_encoder.pkl → Encoders for categorical features
• app.py → Flask backend code
• index.html → Frontend code

🤝 Contributors

👨‍💻 Saadullah Asif – Machine Learning & Software Engineer
👨‍💻 Saad Hassan Faisal – Collaborator
