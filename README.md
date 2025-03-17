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

# 📥 Downloading the Dataset (Kaggle API)



To download the dataset, you need a Kaggle API key.

### Step 1: Download kaggle.json
	1.	Go to Kaggle → Profile → Account
	2.	Click “Create New API Token” and make note of your username and token to input into the notebook
    3.      Make sure you have accepted the terms and conditions of the competition to be able to access the dataset



---
## Now Work Through the notebook


---
 Resources & Acknowledgments

	•	Dataset: Kaggle Bike Sharing Demand
	•	ML Frameworks Used: AutoGluon
	•	Developed by: Harish Kumaravel
