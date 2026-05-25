# 📊 Telco Customer Churn Prediction using Deep Learning

A Deep Learning based Customer Churn Prediction project built with **TensorFlow/Keras**, **Scikit-learn**, and **Python**.  
This project analyzes customer behavior from a telecom dataset and predicts whether a customer is likely to leave the service.

---

# 🚀 Project Overview

Customer churn prediction is one of the most important business problems in the telecom industry. Companies use churn prediction models to identify customers who are likely to cancel their subscriptions and take preventive actions.

In this project:

- Data preprocessing and feature engineering were performed.
- Categorical data was encoded.
- Numerical features were standardized.
- A Deep Neural Network (DNN) model was built using TensorFlow/Keras.
- EarlyStopping and Dropout were used to reduce overfitting.
- Model performance was evaluated using accuracy, confusion matrix, and classification report.

---

# 🧠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow / Keras
- Google Colab

---

# 📂 Dataset

Dataset used:

**Telco Customer Churn Dataset**  
Source: Kaggle

Dataset includes:

- Customer demographics
- Service subscriptions
- Billing information
- Contract details
- Churn status

---

# ⚙️ Project Workflow

## 1️⃣ Data Collection

The dataset was downloaded directly from Kaggle using the Kaggle API.

```python
!kaggle datasets download -d blastchar/telco-customer-churn
```

---

## 2️⃣ Data Preprocessing

Several preprocessing steps were performed:

- Converted `TotalCharges` column to numeric
- Removed missing values
- Dropped unnecessary columns (`customerID`)
- Encoded categorical features using `LabelEncoder`
- Standardized features using `StandardScaler`

---

## 3️⃣ Train-Test Split

Dataset was split into training and testing sets.

```python
train_test_split(X, y, test_size=0.2)
```

---

## 4️⃣ Deep Learning Model

A Sequential Neural Network was built using multiple Dense layers and Dropout layers.

### Model Architecture

- Dense(32) + ReLU
- Dropout(0.3)
- Dense(64) + ReLU
- Dropout(0.3)
- Dense(64) + ReLU
- Dropout(0.3)
- Dense(32) + ReLU
- Dropout(0.3)
- Dense(16) + ReLU
- Dropout(0.3)
- Dense(8) + ReLU
- Dropout(0.3)
- Dense(1) + Sigmoid

---

# 🛡️ Overfitting Prevention

Two important techniques were used:

## ✅ Dropout

Dropout randomly disables neurons during training to prevent overfitting.

```python
Dropout(0.3)
```

## ✅ EarlyStopping

Training stops automatically when validation performance stops improving.

```python
EarlyStopping(patience=5, restore_best_weights=True)
```

---

# 📈 Model Compilation

```python
model.compile(
    optimizer='adam',
    loss='binary_crossentropy',
    metrics=['accuracy']
)
```

---

# 🏋️ Model Training

```python
history = model.fit(
    X_train,
    y_train,
    epochs=50,
    batch_size=30,
    validation_split=0.2,
    callbacks=[early_stop]
)
```

---

# 📊 Evaluation Metrics

The following evaluation techniques were used:

- Accuracy
- Confusion Matrix
- Classification Report
- Loss Curve
- Accuracy Curve

---

# 📉 Visualization

Training and validation performance were visualized using:

- Loss Curve
- Accuracy Curve
- Churn Distribution Graph

---

# 📁 Project Structure

```bash
├── notebook.ipynb
├── WA_Fn-UseC_-Telco-Customer-Churn.csv
├── README.md
```

---

# ▶️ How to Run

## 1. Clone the repository

```bash
git clone <your-repository-link>
cd <repository-folder>
```

## 2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow
```

## 3. Run the notebook

Open the notebook using:

- Jupyter Notebook
- VS Code
- Google Colab

---

# 🎯 Future Improvements

Possible future improvements:

- Hyperparameter tuning
- Feature selection
- Using advanced models like XGBoost
- Deploying the model with Flask or FastAPI
- Building a frontend dashboard

---

# 📌 Key Learning Outcomes

This project demonstrates:

- End-to-end machine learning workflow
- Deep learning for binary classification
- Data preprocessing techniques
- Overfitting prevention methods
- Model evaluation and visualization

---

# 👨‍💻 Author

**MD. Faysal Islam Fahad**  
DL Engineer

---

# ⭐ If you like this project

Give this repository a ⭐ on GitHub and feel free to contribute or fork the project.

