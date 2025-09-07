# Heart-disease-prediction

->This project is a Heart Disease Prediction System that uses machine learning to predict whether a person is likely to have heart disease based on their medical attributes.

🔹 Model Used

->The system is based on the K-Nearest Neighbors (KNN) algorithm, a supervised machine learning method.

->KNN works by finding the k most similar patients (neighbors) in the training dataset and classifying a new patient based on the majority class of those neighbors.

->It’s effective for medical predictions because it uses pattern similarity to detect disease risk.

🔹 Input Features

The model expects patient health data as input (from columns.pkl).
Typical features include:

->Age

->Sex

->Chest Pain Type (cp)

->Resting Blood Pressure (trestbps)

->Cholesterol (chol)

->Fasting Blood Sugar (fbs)

->Resting ECG Results (restecg)

->Maximum Heart Rate Achieved (thalach)

->Exercise-Induced Angina (exang)

->ST Depression (oldpeak)

->Slope of ST segment (slope)

->Number of major vessels (ca)

->Thalassemia test result (thal)

🔹 Preprocessing

->Scaling: Features are scaled using the saved scaler.pkl (probably StandardScaler) to normalize numerical values.

->Encoding: Some categorical values (like chest pain type, sex, thal) are converted into numerical form.

This ensures fair distance calculation in KNN (since KNN is distance-based).

🔹 Prediction Output

The trained model (KNN_heart.pkl) outputs:

0 → No Heart Disease

1 → Heart Disease Detected

This binary classification helps doctors or users understand their heart risk.

🔹 Deployment

The app.py script likely uses Flask or Streamlit to create a web interface.

User inputs their health data → Data gets preprocessed with scaler.pkl → Passed to the trained model (KNN_heart.pkl) → Model returns prediction.
