# 🏦 Loan Approval Classification

A Streamlit web app that predicts whether a loan application will be **Approved** or **Rejected** using a machine learning model.

## 📌 About the Project
Banks receive many loan applications, and checking each one by hand takes time. This project uses past loan data to train a model that predicts the loan status from the applicant's details. The user fills in the form, clicks **Predict Loan Status**, and gets the result instantly.

## ✨ Features
- Simple, easy-to-use web interface
- Predicts loan approval or rejection in one click
- Compares 5 machine learning models and saves the best one
- Data analysis (EDA) included in a Jupyter notebook

## 📊 Dataset

### Data Source
This is a synthetic dataset inspired by the original Credit Risk dataset on Kaggle, enriched with extra variables based on Financial Risk for Loan Approval data. SMOTENC was used to simulate new data points and enlarge the dataset. It contains both categorical and continuous features.

### Details
- 45,000 records and 14 variables
- Target column: `loan_status` (1 = approved, 0 = rejected)
- The data is imbalanced: about 78% rejected and 22% approved

| Column | Description | Type |
|---|---|---|
| `person_age` | Age of the person | Float |
| `person_gender` | Gender of the person | Categorical |
| `person_education` | Highest education level | Categorical |
| `person_income` | Annual income | Float |
| `person_emp_exp` | Years of employment experience | Integer |
| `person_home_ownership` | Home ownership status (rent, own, mortgage) | Categorical |
| `loan_amnt` | Loan amount requested | Float |
| `loan_intent` | Purpose of the loan | Categorical |
| `loan_int_rate` | Loan interest rate | Float |
| `loan_percent_income` | Loan amount as a percentage of annual income | Float |
| `cb_person_cred_hist_length` | Length of credit history in years | Float |
| `credit_score` | Credit score of the person | Integer |
| `previous_loan_defaults_on_file` | Indicator of previous loan defaults | Categorical |
| `loan_status` | Loan approval status: 1 = approved, 0 = rejected | Integer |

### Known Data Issue
The original data has some unrealistic ages (over 100 years old). These are handled during cleaning.

## 🤖 Models Used
- Logistic Regression
- Naive Bayes
- Support Vector Machine (SVM)
- Decision Tree
- Random Forest

Each model is built as a pipeline with scaling and encoding. The model with the best accuracy is saved as `best_model_pipeline.pkl` and used in the app.

## 🗂️ Project Structure
```
loan-approval-classification/
├── app.py                    # Streamlit app
├── EDA.ipynb                 # Data analysis and model training
├── Cleaned_data.csv          # Cleaned dataset
├── best_model_pipeline.pkl   # Trained model
├── requirements.txt          # Required libraries
├── images/                   # Logo
└── README.md
```

## 🚀 How to Run Locally
1. Download this repository and open the folder in a terminal
2. Install the libraries
```bash
   pip install -r requirements.txt
```
3. Start the app
```bash
   streamlit run app.py
```

## 💡 How to Use
1. Enter the applicant's details using the sliders and dropdowns.
2. Click **Predict Loan Status**.
3. The app shows **Loan Approved** or **Loan Rejected**.

## ⚠️ Notes
- The dataset is synthetic, so the model's results are only a prediction and not a real bank decision.
- Predictions are most reliable for values close to those in the dataset.
- The data has more rejected loans than approved ones, so the model may lean toward "Rejected".

## 🛠️ Built With
Python · Pandas · Scikit-learn · Streamlit

## 👤 Author
**Rajdeep**