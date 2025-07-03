# Customer Churn Prediction

## 📌 Overview
This project aims to predict customer churn using machine learning techniques on the **Telco Customer Churn Dataset**. The dataset includes customer demographics, account information, and service usage patterns. Our goal is to identify key drivers of churn and build predictive models that can flag customers at risk of leaving.

---

## 🗂️ Project Structure
```
customer-churn-prediction/
├── data/
│   └── WA_Fn-UseC_-Telco-Customer-Churn.csv      # Raw dataset
├── notebooks/
│   └── Customer_Churn_Prediction_using_ML.ipynb  # Jupyter notebook for EDA & modeling
├── src/
│   ├── preprocessing.py                          # Data preprocessing scripts
│   ├── model.py                                  # Model training and evaluation
│   └── utils.py                                  # Helper functions
├── README.md                                     # Project documentation
├── requirements.txt                              # Python dependencies
```

---

## 📊 Dataset Information
- **Source**: Telco Customer Churn dataset
- **Rows**: 7,043  
- **Columns**: 21  
- **Target Variable**: `Churn` — indicates whether a customer has left the service.

The dataset contains customer demographics, account status, contract details, and service usage information.

---

## ⚙️ Installation

To set up the project locally:

```bash
# Clone the repository
git clone https://github.com/yourusername/customer-churn-prediction.git
cd customer-churn-prediction

# Create and activate a virtual environment
python -m venv venv
source venv/bin/activate        # On Windows use: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

---

## 🚀 Usage

### To run the model training and evaluation notebook:

```bash
jupyter notebook
```

Then open:  
`notebooks/Customer_Churn_Prediction_using_ML.ipynb`  
It covers:
- Data exploration
- Preprocessing
- Model training & evaluation

---

## 🔄 Data Preprocessing

The following steps were taken:
1. **Dropped** `customerID` as it has no predictive value.
2. **Encoded** categorical features using `LabelEncoder`.
3. **Balanced** the dataset using **SMOTE** (Synthetic Minority Over-sampling Technique) to address class imbalance.

---

## 🤖 Machine Learning Models

### ✔️ Exploratory Data Analysis (EDA)
- Identified relationships between features and churn.
- Visualized trends in tenure, charges, and contract types.

### ✔️ Models Implemented
- **Decision Tree**: A simple model that splits data based on feature thresholds.
- **Random Forest**: Ensemble of decision trees to reduce overfitting and improve accuracy.
- **XGBoost**: Gradient boosting framework known for high performance and robustness.

### ✔️ Evaluation Metrics
- **Accuracy**
- **Confusion Matrix**
- **Precision, Recall, F1-score** (via Classification Report)
- **ROC Curve** and **AUC Score**

---

## 📈 Key Findings
- The **best-performing model** (XGBoost) achieved **~80% accuracy** on the test set.
- **Top influential features**:
  - `Tenure`
  - `MonthlyCharges`
  - `Contract` type

---

## 📌 Future Improvements
- Hyperparameter tuning using GridSearchCV or Optuna.
- Incorporation of deep learning models (e.g., Neural Networks).
- Deployment via Flask or Streamlit for live predictions.

---
