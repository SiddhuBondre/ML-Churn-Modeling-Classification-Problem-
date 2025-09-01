# ML-Churn-Modeling-Classification-Problem-

# 🧠 Customer Churn Prediction using ANN

## 📌 Project Overview
This project predicts whether a customer will churn (leave the bank) using an **Artificial Neural Network (ANN)** built with **Keras** and optimized with **GridSearchCV**.  
The dataset used is `Churn_Modelling.csv`, which contains information about bank customers.

---

## ⚙️ Steps Followed

### 1. Data Preprocessing
- Imported dataset (`Churn_Modelling.csv`)
- Selected features (`X`) and target (`y`)
- Converted categorical variables (`Geography`, `Gender`) into dummy variables
- Dropped unnecessary columns
- Split data into training (80%) and testing (20%)
- Applied feature scaling using **StandardScaler**

### 2. Building the ANN
- Initialized ANN with **Keras Sequential API**
- Added:
  - Input layer + 1st hidden layer (ReLU, He Uniform init)
  - 2nd hidden layer (ReLU, He Uniform init)
  - Output layer (Sigmoid, Glorot Uniform init)
- Compiled ANN using:
  - Optimizer: `Adamax` (tested others in tuning)
  - Loss function: `binary_crossentropy`
  - Metrics: `accuracy`

### 3. Training
- Trained model on training set
- Used `validation_split` for validation during training
- Plotted accuracy & loss curves for monitoring

### 4. Evaluation
- Predictions on test set
- Converted probabilities → binary (threshold = 0.5)
- Evaluated performance with:
  - Accuracy Score
  - Confusion Matrix
  - Classification Report

### 5. Hyperparameter Tuning
- Wrapped ANN using **SciKeras KerasClassifier**
- Applied **GridSearchCV** with:
  - Optimizers: `adam`, `rmsprop`, `adamax`
  - Epochs: 50, 100
  - Batch sizes: 10, 20, 32
- Selected best parameters based on cross-validation

---

## 📊 Results
- Achieved test accuracy of around **X%** (update with your best score).
- Best hyperparameters: *(update with GridSearch results)*.

---

## 🛠️ Technologies Used
- Python 3.12
- NumPy, Pandas, Matplotlib, Seaborn
- Scikit-learn
- TensorFlow / Keras
- SciKeras

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/churn-ann.git
   cd churn-ann
