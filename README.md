# 📘 Early Stress Detection Using Daily Digital Activity Patterns

## Project Overview
This project implements a **machine learning–based early stress detection system** using **daily digital activity patterns** derived from smartphone usage behavior.  
The goal is to identify **early behavioral indicators of stress** before it manifests into severe psychological or physiological symptoms.

Unlike traditional stress detection approaches that rely on **wearable sensors or self-reported surveys**, this system leverages **passively collected digital behavior data**, making it scalable, non-intrusive, and privacy-aware.

> ⚠️ **Ownership Notice:**  
> This project and its research concept belong to **Ishita Roy Choudhury(22BAI71008)**.  
> The implementation is based on her academic research work.

---

## 👩‍🎓 Author
**Ishita Roy Choudhury(22BAI71008)**  
Department of Computer Science Engineering  
Apex Institute of Technology  
Chandigarh University, Punjab, India  

---

## 🎯 Objectives
- Detect early stress signals using **digital behavior patterns**
- Model stress as a **progressive risk score**, not just a binary outcome
- Ensure **interpretability** through feature importance analysis
- Design a **modular and reproducible ML pipeline**

---

## 📊 Dataset
Due to privacy and accessibility constraints of raw smartphone sensing datasets, this project uses a **synthetically generated dataset** that simulates realistic daily digital behavior of students.

### Features Used
| Feature | Description |
|------|------------|
| screen_time | Total screen usage per day (minutes) |
| app_sessions | Number of application launches |
| night_usage | Screen usage between 12 AM – 5 AM |
| call_count | Number of phone calls |
| sms_count | Number of SMS messages |
| sleep_hours | Estimated sleep duration |
| app_entropy | App usage diversity |
| screen_per_session | Average screen time per session |
| night_screen_ratio | Ratio of night usage to total screen time |
| sleep_deficit | Deviation from ideal sleep duration |

**Target Variable**
- stress_label  
  - 0 → Low Stress  
  - 1 → High Stress  

---

## 🧠 Methodology
1. **Feature Engineering**  
   Behavioral ratios and sleep-related indicators are derived to capture subtle stress signals.

2. **Model Architecture**  
   - Gradient Boosting Classifier  
   - Feature scaling using StandardScaler  
   - Stratified train–test split  

3. **Evaluation Strategy**
   - Precision, Recall, F1-Score  
   - ROC–AUC Curve  
   - Feature Importance Visualization  

4. **Risk-Based Output**
   - Continuous **Stress Risk Score (0–1)** generated using prediction probabilities  
   - Enables early-warning and graded intervention strategies

---

## 📈 Key Results
- The model demonstrates reliable discrimination between low-stress and high-stress behavioral patterns.
- Night-time smartphone usage, sleep deficit, and behavioral fragmentation are identified as strong stress indicators.
- Continuous stress risk scores support **early detection** rather than reactive classification.

---

## 📂 Project Structure
```
Stress Detection/
│
├── train_model.py
├── evaluate.py
├── graphs.py
├── feature_engineering.py
├── artifacts/
│   ├── model.pkl
│   ├── features.pkl
│   └── y_prob.npy
└── synthetic_studentlife_stress_data.csv
```

---

## ▶️ How to Run

### Step 1: Train the model
```bash
python train_model.py
```

### Step 2: Evaluate performance
```bash
python evaluate.py
```

### Step 3: Generate visualizations
```bash
python graphs.py
```


## 📌 Acknowledgement
This implementation is based on the original research work of **Ishita Roy Choudhury(22BAI71008)** and is intended strictly for **academic and research purposes**.
=======
# Early Stress Detection Using Daily Digital Activity Patterns



## Ownership & Authorship
This project and research concept belong to **Ishita Roy Choudhury(22BAI71008)**.

---





## System Architecture

Google Fit API → Raw Activity & Sleep Data → Proxy Mapping → Feature Engineering → Pre-trained ML Model → Stress Risk Score

---

## Machine Learning Pipeline

### Features Used
Primary:
- screen_time
- app_sessions
- night_usage
- call_count
- sms_count
- sleep_hours
- app_entropy

Engineered:
- screen_per_session
- night_screen_ratio
- sleep_deficit

### Model
- Ensemble classifier
- Probability-based inference
- Persistent trained model artifact

---

## Google Fit Integration
- Aggregated step count
- Sleep duration
- Local timezone aggregation
- Health Connect compatible

---

## Handling Partial Data
Unavailable behavioral features are proxy-estimated to maintain consistent model input.

---
## 🔐 Generating `client_secret.json` (Google OAuth Setup)

Follow these steps to generate it:

### Step 1: Create a Google Cloud Project
1. Go to: https://console.cloud.google.com/
2. Click **Select Project → New Project**
3. Give a project name and create it

---

### Step 2: Enable Google Fit API
1. Open your project
2. Go to **APIs & Services → Library**
3. Search for **Google Fit API**
4. Click **Enable**

---

### Step 3: Configure OAuth Consent Screen
1. Go to **APIs & Services → OAuth consent screen**
2. Select **External**
3. Fill basic details:
   - App name
   - User support email
   - Developer contact email
4. Add scopes:
   - `https://www.googleapis.com/auth/fitness.activity.read`
   - `https://www.googleapis.com/auth/fitness.sleep.read`
5. Save and continue

---

### Step 4: Create OAuth Client ID
1. Go to **APIs & Services → Credentials**
2. Click **Create Credentials → OAuth Client ID**
3. Application type: **Desktop App**
4. Give a name and create
5. Click **Download JSON**

Rename the downloaded file to: client_secret.json


---

## ⚖️ Ethical & Usage Disclaimer
- The system is **not a clinical diagnostic tool**
- Stress predictions represent **behavioral risk indicators**
- Synthetic data is used for experimental validation only
- Designed with **privacy-preserving principles**

---

## 🔮 Future Enhancements
- Temporal stress progression modeling
- Personalized baseline adaptation
- Federated learning for privacy-aware deployment
- Integration with real-world smartphone sensing data
- Intervention effectiveness modeling

---


