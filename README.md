# 🚴‍♂️ AutoGluon-Kaggle-Ride-Sharing  

This project predicts **bike rental demand** using **AutoGluon**, as part of the **Kaggle Bike Sharing Demand competition**.  
It explores **feature engineering, model tuning, and hyperparameter optimization** to improve RMSE scores.  

---

## 📌 Project Overview  

### **1️⃣ Exploratory Data Analysis (EDA)**  
- Analyze dataset trends and visualize distributions.  
- Identify **seasonal patterns, temperature effects, and peak demand hours**.  

### **2️⃣ Baseline Model with AutoGluon**  
- Train an **initial `TabularPredictor` model** with default settings.  
- Submit predictions to **Kaggle** as a **benchmark score**.  

### **3️⃣ Feature Engineering & Model Improvement**  
- Extract additional features to enhance model accuracy:  
  - `hour`, `is_rush_hour`, `weekday`, `temperature_interaction`  
- Train an updated model and compare performance.  

### **4️⃣ Hyperparameter Optimization (HPO)**  
- Tune **key hyperparameters** for better model performance:  
  - `num_boost_round`, `learning_rate`, `max_depth`  
- Evaluate optimized models **vs. baseline performance**.  

### **5️⃣ Final Evaluation & Findings**  
- Compare **feature engineering vs. hyperparameter tuning** impact.  
- Identify the **best strategy** for improving AutoGluon models.  

### **6️⃣ Performance Metric**  
- Using **RMSE (Root Mean Squared Error)** to evaluate model effectiveness and the impacts of the feature engineering and hyperparameter tuning.

---

## 🛠️ Setup Instructions  

### **🔹 1️⃣ Clone the Repository**  

git clone https://github.com/yourusername/AutoGluon-Kaggle-Ride-Sharing.git
cd AutoGluon-Kaggle-Ride-Sharing

---

### **🚀 Step-by-Step Guide to Setting Up Kaggle API and Downloading the Dataset Securely**

To download the dataset using Kaggle’s API, follow these steps to ensure **security and proper setup**.

---

## Step 1: Get Your Kaggle API Key
1. Go to [Kaggle](https://www.kaggle.com/) and **log in**.
2. Click on your **profile picture (top-right corner) → "Account"**.
3. Scroll down to the **API** section and click **"Create New API Token"**.
4. This will download a file named **`kaggle.json`**, which contains your API credentials.

---

## Step 2: Store Your Kaggle API Key Securely
To avoid exposing your credentials, store them in a **`.env` file** instead of hardcoding them in your scripts.


create a `.env` file in your project directory:
```sh
touch .env
```
Then, **edit `.env`** and add your Kaggle credentials:
```ini
KAGGLE_USERNAME=your_kaggle_username
KAGGLE_KEY=your_kaggle_api_key
```

---

## Step 3: Ensure You Have Access to the Dataset
Before downloading the dataset, **make sure you have accepted the Bike-Sharing-Demand Competition terms**.

1. Go to the **Kaggle competition page**.
2. Click **“Rules”** and **accept the terms**.

---



## Step 4: Add `.env` to `.gitignore` to Keep It Private
To prevent your API credentials from being uploaded to GitHub, add `.env` to your `.gitignore` file:
```sh
echo ".env" >> .gitignore
```

---

## **🚀 You’re All Set!**


---
## Now Work Through the notebook


---
 Resources & Acknowledgments

	•	Dataset: Kaggle Bike Sharing Demand
	•	ML Frameworks Used: AutoGluon
	•	Developed by: Harish Kumaravel
