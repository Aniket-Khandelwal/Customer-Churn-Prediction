Customer Churn Prediction

Overview:-
  This project focuses on predicting customer churn using machine learning techniques. The dataset used is the Telco Customer Churn Dataset, which includes customer       demographics, account details, and service usage patterns. By analyzing this data, we aim to identify key factors influencing customer retention and develop models that can predict whether a customer is likely to leave.
  
Project Structure:-
  ├── data
  │   ├── WA_Fn-UseC_-Telco-Customer-Churn.csv  	# Dataset
  ├── notebooks
  │   ├── Customer_Churn_Prediction_using_ML.ipynb   # Jupyter notebook for model development
  ├── src
  │   ├── preprocessing.py        # Data preprocessing functions
  │   ├── model.py                # ML model training and evaluation
  │   ├── utils.py                # Utility functions
  ├── README.md                    # Project documentation
  ├── requirements.txt             # List of dependencies
  
Dataset Information:-
  The dataset contains 7,043 rows and 21 columns, providing insights into customer details, services subscribed, contract types, and monthly charges. The key feature is   Churn, which indicates whether a customer has discontinued the service.
  
Installation:-
  Follow these steps to set up the project:
  # Clone the repository
    git clone https://github.com/yourusername/customer-churn-prediction.git
    cd customer-churn-prediction

  # Create and activate a virtual environment
    python -m venv venv
    source venv/bin/activate  # On Windows use: venv\Scripts\activate

  # Install required dependencies
    pip install -r requirements.txt
    
Usage:-
   (i)To run the Jupyter notebook and execute the model training steps:
    jupyter notebook
   (ii)Open Customer_Churn_Prediction_using_ML.ipynb to explore data analysis, preprocessing, and model evaluation.
   
Data Preprocessing Steps:-
   (i)Removed the customerID column as it is not relevant to predictions., 
   (ii)Encoded categorical variables using LabelEncoder., 
   (iii)Applied SMOTE to balance the dataset and address class imbalance.
  
Machine Learning Models Used:-
   (i)Exploratory Data Analysis (EDA): Conducted data visualization and identified important features., 
   (ii)Model Training: 
          -Decision Tree: A simple yet effective model that classifies data by splitting it into branches based on feature values., 
          -Random Forest: An ensemble learning technique that builds multiple decision trees to enhance accuracy and reduce overfitting., 
          -XGBoost (Extreme Gradient Boosting): A high-performance boosting algorithm that optimizes predictions by iteratively improving weak models.
   (iii)Evaluation Metrics Used: 
          -Accuracy, 
          -Confusion Matrix, 
          -Precision, Recall, and F1-score (via Classification Report), 
          -ROC Curve & AUC for model performance comparison
          
Key Findings
   (i)The most effective model achieved 80 % accuracy on the test set., 
   (ii)Features such as Tenure, MonthlyCharges, and Contract Type significantly impact churn prediction.
