# 🛠️ ITSM Incident Service & Management System

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white"/>
  <img src="https://img.shields.io/badge/XGBoost-189fdd?style=for-the-badge&logo=xgboost&logoColor=white"/>
  <img src="https://img.shields.io/badge/NLP-8A2BE2?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge"/>
</p>

<p align="center">
  <b>ML-powered IT service management — automating incident prioritization, ticket classification, volume forecasting, and RFC failure prediction.</b>
</p>

---

## 📌 Overview

The **ITSM Incident Service & Management System** is a machine learning–based solution that automates and optimizes IT service management workflows. By analyzing historical IT ticket data, the system predicts incident priority, auto-classifies tickets, forecasts future incident volumes, and flags high-risk change requests — helping IT teams respond faster and plan smarter.

> 💡 Built to reduce manual IT workload, improve SLA compliance, and enable proactive resource planning.

---

## ✨ Key Features

| Feature | Description |
|---|---|
| 🚨 **Incident Priority Prediction** | Classifies incoming tickets as high / medium / low priority using ML |
| 🏷️ **Automatic Ticket Tagging** | Categorizes incidents into predefined types using NLP |
| 📈 **Incident Volume Forecasting** | Time-series forecasting to predict future ticket volumes |
| ⚠️ **RFC Failure Prediction** | Flags change requests likely to fail before they are executed |
| ⚖️ **Data Imbalance Handling** | Applies SMOTE and downsampling to handle skewed class distributions |

---

## 🧠 How It Works

```
Historical ITSM Ticket Data
          │
          ▼
  Data Cleaning & Preprocessing
  (null handling, encoding, normalization)
          │
          ▼
  Class Imbalance Handling
  (SMOTE / Downsampling)
          │
          ▼
  ┌───────────────────────────────────────┐
  │         ML Model Training             │
  │                                       │
  │  ├── Priority Prediction              │
  │  │   (XGBoost / Classification)       │
  │  │                                    │
  │  ├── Ticket Tagging                   │
  │  │   (NLP-based Classification)       │
  │  │                                    │
  │  ├── Volume Forecasting               │
  │  │   (Time-Series Models)             │
  │  │                                    │
  │  └── RFC Failure Prediction           │
  │      (Binary Classification)          │
  └───────────────────────────────────────┘
          │
          ▼
  Model Evaluation & Performance Metrics
          │
          ▼
  Actionable Insights for IT Teams
```

---

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| **Language** | Python 3.8+ |
| **Data Handling** | Pandas, NumPy |
| **ML Models** | Scikit-learn, XGBoost |
| **NLP** | Scikit-learn (TF-IDF / text features) |
| **Imbalance Handling** | SMOTE (imbalanced-learn), Downsampling |
| **Forecasting** | Time-Series models (Scikit-learn / statsmodels) |
| **ETL** | Custom data preprocessing & feature engineering pipelines |
| **Development** | Jupyter Notebook, Git |

---

## 📂 Project Structure

```
itsm-incident-management/
│
├── notebooks/
│   ├── 01_data_preprocessing.ipynb       # Cleaning, encoding, feature engineering
│   ├── 02_priority_prediction.ipynb      # High-priority ticket classification
│   ├── 03_ticket_classification.ipynb    # NLP-based auto ticket tagging
│   ├── 04_volume_forecasting.ipynb       # Time-series incident volume forecasting
│   └── 05_rfc_failure_prediction.ipynb   # RFC risk identification
│
├── data/
│   ├── raw/                              # Raw ITSM ticket data
│   └── processed/                        # Cleaned & feature-engineered data
│
├── models/                               # Trained model artifacts
├── requirements.txt
└── README.md
```

---

## ⚙️ Setup & Installation

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/nirusanathara/itsm-incident-management.git
cd itsm-incident-management
```

### 2️⃣ Create & Activate Virtual Environment
```bash
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate           # Windows
```

### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 4️⃣ Add Your Dataset
Place your ITSM ticket data (CSV format) inside `data/raw/`.

### 5️⃣ Run Notebooks in Order
Open Jupyter and run notebooks sequentially:
```bash
jupyter notebook
```

---

## 🔬 ML Models & Techniques

### 1. 🚨 Incident Priority Prediction
- **Type:** Multi-class Classification
- **Model:** XGBoost / Random Forest
- **Target:** High / Medium / Low priority
- **Challenge:** Class imbalance handled with SMOTE

### 2. 🏷️ Automatic Ticket Tagging
- **Type:** Text Classification (NLP)
- **Technique:** TF-IDF vectorization + ML classifier
- **Input:** Raw ticket description text
- **Output:** Predicted ticket category/type

### 3. 📈 Incident Volume Forecasting
- **Type:** Time-Series Forecasting
- **Goal:** Predict daily/weekly ticket volumes
- **Use Case:** Resource planning & staffing optimization

### 4. ⚠️ RFC Failure Prediction
- **Type:** Binary Classification
- **Target:** Will this change request fail? (Yes / No)
- **Use Case:** Proactive risk assessment in change management

---

## 📊 Model Evaluation Metrics

| Model | Key Metrics |
|---|---|
| Priority Prediction | Accuracy · Precision · Recall · F1-Score |
| Ticket Classification | Accuracy · Macro F1 · Confusion Matrix |
| Volume Forecasting | MAE · RMSE · MAPE |
| RFC Failure Prediction | AUC-ROC · Precision · Recall |

---

## 📈 Results

- ✅ Improved incident prioritization accuracy through ML-based classification
- ✅ Reduced manual ticket classification effort with NLP auto-tagging
- ✅ Enabled proactive resource planning via volume forecasting
- ✅ Provided risk insights for change management through RFC failure prediction

---

## 🔮 Roadmap

- [ ] Real-time integration with **ServiceNow** or **Jira Service Management**
- [ ] REST API deployment via FastAPI microservices
- [ ] Interactive analytics dashboard (Streamlit / Power BI)
- [ ] Deep learning models for improved NLP classification (BERT)
- [ ] Automated retraining pipeline with MLflow
- [ ] Docker containerization for production deployment

---

## 👨‍💻 Author

**Niru Sanathara**  
AI/ML Engineer | Applied Scientist  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sanatharaniru/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/Niru-112)



<p align="center"><i>⚡ Automating IT operations through machine learning — faster response, smarter decisions.</i></p>
