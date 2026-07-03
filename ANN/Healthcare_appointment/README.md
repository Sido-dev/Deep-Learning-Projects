# 🏥 Healthcare Appointment No-Show Prediction using Artificial Neural Network (ANN)

A Deep Learning classification project that predicts whether a patient will **show up for a scheduled healthcare appointment** using an Artificial Neural Network (ANN). The project covers the complete machine learning workflow, including data preprocessing, handling class imbalance with ADASYN, model training, and performance evaluation.

---

# 📌 Project Overview

Missed medical appointments lead to increased healthcare costs and inefficient resource utilization. This project develops an ANN classifier to predict whether a patient is likely to miss an appointment based on healthcare-related features.

The notebook follows a complete end-to-end deep learning pipeline using **TensorFlow/Keras**.

---

# 📂 Project Structure

```
Healthcare-Appointment-No-Show-ANN/
│
├── Healthcare_ann.ipynb
├── synthetic_healthcare_appointment_no_show.csv
└── README.md
```

---

# 🚀 Workflow

### 1. Import Libraries

- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow / Keras
- imbalanced-learn (ADASYN)

---

### 2. Load Dataset

- Read dataset
- Inspect records
- Explore dataset structure

---

### 3. Exploratory Data Analysis (EDA)

- Dataset information
- Statistical summary
- Missing value analysis
- Duplicate value analysis
- Correlation analysis
- Target distribution

---

### 4. Data Preprocessing

- Feature selection
- Target variable separation
- Train-Test Split
- Feature Scaling using StandardScaler

---

### 5. Handle Class Imbalance

The training dataset is balanced using **ADASYN (Adaptive Synthetic Sampling)** to improve model performance on the minority class.

---

### 6. Artificial Neural Network

Network Architecture

```
Input Layer
      │
      ▼
Dense (32, ReLU)
      │
      ▼
Dense (16, ReLU)
      │
      ▼
Dense (1, Sigmoid)
```

---

### 7. Model Compilation

- Optimizer: Adam
- Loss Function: Binary Crossentropy
- Evaluation Metric: Accuracy

---

### 8. Model Training

- Batch Size: 32
- Epochs: 100
- Validation Split: 20%

---

### 9. Prediction

The trained ANN predicts whether a patient is likely to attend or miss the appointment.

---

### 10. Model Evaluation

The model is evaluated using:

- Accuracy
- Confusion Matrix
- Classification Report
  - Precision
  - Recall
  - F1-Score

---

# 🛠 Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow
- Keras
- imbalanced-learn (ADASYN)
- Jupyter Notebook

---

# 📊 Machine Learning Pipeline

```
Dataset
    │
    ▼
EDA
    │
    ▼
Data Preprocessing
    │
    ▼
Train-Test Split
    │
    ▼
Feature Scaling
    │
    ▼
ADASYN Oversampling
    │
    ▼
Artificial Neural Network
    │
    ▼
Prediction
    │
    ▼
Model Evaluation
```

---

# 🧠 ANN Architecture

```
Input Features
      │
      ▼
Dense (32, ReLU)
      │
      ▼
Dense (16, ReLU)
      │
      ▼
Dense (1, Sigmoid)
      │
      ▼
Prediction
```

---

# 📦 Installation

Clone the repository

```bash
git clone https://github.com/Sido-dev/Deep-Learning-Projects.git
```

Install dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn tensorflow imbalanced-learn jupyter
```

---

# ▶️ Run the Project

Launch Jupyter Notebook

```bash
jupyter notebook
```

Open

```
Healthcare.ipynb
```

Run all cells sequentially.

---

# 📈 Model Configuration

| Parameter | Value |
|-----------|-------|
| Hidden Layer 1 | 32 Neurons |
| Hidden Layer 2 | 16 Neurons |
| Activation | ReLU |
| Output Activation | Sigmoid |
| Optimizer | Adam |
| Loss Function | Binary Crossentropy |
| Batch Size | 32 |
| Epochs | 100 |
| Validation Split | 20% |

---

# 📊 Evaluation Metrics

- Accuracy Score
- Confusion Matrix
- Precision
- Recall
- F1-Score
- Classification Report

---

# ✨ Features

- Complete Exploratory Data Analysis (EDA)
- Missing & Duplicate Value Analysis
- Feature Scaling
- ADASYN Oversampling
- Artificial Neural Network using TensorFlow/Keras
- Binary Classification
- Confusion Matrix
- Classification Report
- Well-structured and easy-to-follow notebook

---

# 🚀 Future Improvements

- Hyperparameter tuning using Keras Tuner
- Dropout layers for regularization
- Early Stopping
- ROC Curve & AUC Score
- Model Saving and Deployment
- Cross Validation

---

# 👨‍💻 Author

**Sudhanshu Narayane**

- GitHub: https://github.com/Sido-dev

---

# ⭐ If you found this project helpful, consider giving the repository a Star!