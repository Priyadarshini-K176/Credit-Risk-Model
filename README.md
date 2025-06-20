# 💳 Credit Risk Modeling Web App

This Streamlit-based app predicts an applicant's **default probability**, generates a **credit score (300–900)**, and assigns a **risk rating** (Poor to Excellent) based on various financial and behavioral factors.

---

## 🚀 Try the App

🔗 [Launch Credit Risk App](https://credit-risk-model-app.streamlit.app/)

---

## 🧠 Model Inputs (Features Used)

The model uses the following **13 features**:

| Feature Name                   | Description                                                                 |
|-------------------------------|-----------------------------------------------------------------------------|
| `age`                         | Age of the applicant                                                       |
| `loan_tenure_months`          | Loan repayment period in months                                            |
| `number_of_open_accounts`     | Number of currently active loan accounts                                   |
| `credit_utilization_ratio`    | % of credit limit currently being used                                     |
| `loan_to_income`              | Ratio of loan amount to annual income (`loan_amount / income`)            |
| `delinquency_ratio`           | % of months with late payments over the loan tenure                       |
| `average_dpd_per_delinquency` | Average number of days payment was delayed when delinquent                |
| `residence_type_Owned`        | One-hot encoded: 1 if residence is owned, else 0                          |
| `residence_type_Rented`       | One-hot encoded: 1 if rented, else 0                                      |
| `loan_purpose_Education`      | One-hot encoded: 1 if loan is for education                               |
| `loan_purpose_Home`           | One-hot encoded: 1 if loan is for home purchase                           |
| `loan_purpose_Personal`       | One-hot encoded: 1 if loan is for personal use                            |
| `loan_type_Unsecured`         | One-hot encoded: 1 if loan is unsecured                                   |

> 🧩 The categorical features are converted into one-hot encoded values.

---

## 🧮 How It Works

1. **User fills out the form**
2. Data is **preprocessed and scaled**
3. The model returns:
   - ✅ **Default Probability**
   - 📊 **Credit Score** (300–900)
   - 🟢 **Risk Rating**: Poor, Average, Good, Excellent

---

## 📦 Tech Stack

- **Frontend**: Streamlit
- **ML Model**: Logistic Regression (via scikit-learn)
- **Preprocessing**: pandas, NumPy, MinMaxScaler
- **Model Persistence**: joblib
- **Deployment**: Streamlit Cloud

---

## 🖥 Run Locally

```bash
git clone https://github.com/Priyadarshini-K176/Credit-Risk-Model.git
cd Credit-Risk-Model
pip install -r requirements.txt
streamlit run main.py
