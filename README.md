# creditcard-fraud-detection-
"Credit Card Fraud Detection using XGBoost with Gradio interface. This project trains a machine learning model on transaction data to identify fraudulent activity. Features preprocessing, probability visualization, custom CSS UI, and real-time prediction demo for fraud risk detection."
# 🚨 Credit Card Fraud Detection 💳  
This project focuses on detecting fraudulent credit card transactions using XGBoost and other machine learning models. The final app is deployed with a Gradio interface for real-time fraud risk prediction, supported by a custom CSS design and interactive probability visualization.

## 📂 Dataset 

The dataset used is the **[Credit Card Fraud Detection Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud)** from Kaggle.

- Contains **284,807 transactions** made by European cardholders in September 2013.  
- Each transaction is labeled as:  
  - **0 → Legitimate**  
  - **1 → Fraudulent**  

## 🤖 Model Comparison  

We experimented with several models to identify the best fraud detection approach.


| Model                  | Accuracy | Precision | Recall | F1-Score |
|-------------------------|----------|-----------|--------|----------|
| Logistic Regression     | 94%      | 0.72      | 0.62   | 0.67     |
| K-Nearest Neighbors     | 95%      | 0.75      | 0.64   | 0.69     |
| Decision Tree           | 91%      | 0.68      | 0.61   | 0.64     |
| Random Forest           | 97%      | 0.83      | 0.74   | 0.78     |
| **XGBoost (final)**     | **99%**  | **0.92**  | **0.88** | **0.90** |

✅ XGBoost was selected as the final model due to its superior performance


⚡ Features


- **Data Preprocessing:**  

Scaling transaction amounts.

Handling class imbalance with undersampling/oversampling.

- **Visualization:** 

Fraud probability meter (green → orange → red).

HTML transaction summary table.

- **Gradio Web App:**  

User inputs: Country, Transaction Type, Amount, Time, Device Type, Recurring.


Real-time fraud probability output with alerts.

## 🛠️ How to Use  
Use our demo on Hugging Face Spaces:

[👉 Try it Live](https://huggingface.co/spaces/Moaz-ai/creditcard)

## 📒 Notebook
We included a Jupyter Notebook (notebooks/fraud_detection.ipynb) for:

Exploratory Data Analysis (EDA).

Model training & evaluation.

Feature importance visualization.

[view on colab](https://colab.research.google.com/drive/1LvlK4Q9-3IHKsqoe8bbizo2UCSZNuf6V?authuser=0#scrollTo=PpFjUYL10Mv5)

 ## ⚠️ Challenges & Solutions

| Problem | Solution |
|---------|----------|
| **Imbalanced Dataset** (fraud cases ~0.17% of all transactions) | Applied SMOTE oversampling, undersampling, and class weights to balance the dataset. |
| **High False Positives** (many normal transactions flagged as fraud) | Tuned probability threshold, added rule-based checks (e.g., very large transactions at unusual times). |
| **Model Interpretability** (users struggle to trust black-box ML) | Used feature importance (XGBoost), added probability meter + HTML summary table for clarity. |
| **Scalability for Real-Time Use** | Designed app with Gradio interface and structured code for easy integration into APIs (Flask/Kafka). |
| **UI/UX Engagement** | Customized Gradio with CSS, risk meter visualization, and fraud alerts for better user experience. |

## 🎯 Future Work

Integrate with real-time transaction streams(Kafka/Flask API).

Apply Deep Learning models (LSTM/Autoencoders).
حp
prepared by moazmohamed

[linkedin](https://www.linkedin.com/in/moaz-mohamed-545725375/)




