# 💳 Credit Risk Modeling Web App

The Credit Risk Modeling App helps lenders, analysts, and fintech platforms make smarter loan decisions by calculating:

🔢 Default Probability

🧮 Credit Score (300–900)

🟢 Risk Rating (Poor, Average, Good, Excellent)

By analyzing behavioral signals like delinquency trends, credit usage habits, and loan-to-income pressure, it goes beyond traditional checks to detect hidden risk.


---


## 🏗️ App Architecture

```text
            ┌───────────────────────────────┐
            │        🌐 Frontend UI         │
            │         (Streamlit)           │
            │                               │
            │ - Takes user inputs           │
            │ - Shows credit score & risk   │
            │ - Displays default probability│
            └─────────────▲─────────────────┘
                          │
                          │ calls
                          ▼
            ┌───────────────────────────────┐
            │       🧠 Prediction Logic      │
            │   (`prediction_helper.py`)    │
            │                               │
            │ - Prepares input dataframe    │
            │ - Applies feature scaling     │
            │ - Runs model prediction       │
            │ - Converts to credit score    │
            │ - Returns rating & probability│
            └─────────────▲─────────────────┘
                          │
                          │ loads
                          ▼
            ┌───────────────────────────────┐
            │     📦 Model Artifacts         │
            │     (`model_data.joblib`)     │
            │                               │
            │ - Trained ML model            │
            │ - Scaler                      │
            │ - Feature list                │
            └───────────────────────────────┘
---

## 🚀 Try the App

🔗 [Launch Credit Risk App]--> https://credit-risk-model-app.streamlit.app/

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
