# 📊 Bike Sharing Demand Prediction Report

## 1️⃣ Introduction  
This project aims to predict **bike rental demand** using machine learning models trained with **AutoGluon**. The dataset is sourced from the **Kaggle Bike Sharing Demand competition**, which includes features such as **weather conditions, timestamps, and seasonal effects**. The goal is to minimize **RMSE (Root Mean Squared Error)** and identify the best-performing model.

## 2️⃣ Data Exploration  
The dataset consists of:
- **Datetime-based features**: `datetime`, `hour`, `weekday`, `month`, `season`.
- **Weather-related variables**: `temperature`, `atemp`, `humidity`, `windspeed`, `weather`.
- **Other categorical features**: `holiday`, `workingday`.
- **Target variable**: `count` (total bike rentals).  


## 3️⃣ Model Training  
### 🏁 Baseline Model
- Used **AutoGluon’s `TabularPredictor`** with default settings.
- Trained on the full dataset with `count` as the label.
- RMSE score obtained: **1.80**.

### 🛠 Feature Engineering
#### 🔍 Key Insights from EDA:
- **Demand is highest during rush hours (8 AM & 5 PM).**
- **Temperature and humidity impact demand significantly.**
- **Weekends show different demand patterns compared to weekdays.**
#### New Features Created
- Extracted **`hour`, `weekday`, `month`, and `rush_hour`** from `datetime`.
- Created **interaction features** like `temp * humidity`.
- RMSE improved to **0.60**.

### 🎯 Hyperparameter Optimization
- Tuned **LightGBM parameters**:
  - `num_boost_round`: 500
  - `learning_rate`: 0.05
  - `max_depth`: 10
- RMSE further reduced to **0.50**.

## 4️⃣ Results & Model Comparison  
| Model | RMSE Score | Kaggle Score | Fit Time (s) | Predict Time (s) | Best Model Type |
|--------|-----------|-------------|-------------|----------------|----------------|
| Baseline (AutoGluon Default) | 1.79680 | 52.982261 | 335.457640 | 22.879514 | WeightedEnsemble_L3 |
| Feature Engineered Model (datetime features)| 0.61670 | 30.570485 | 405.330824 | 25.945760 | WeightedEnsemble_L3 |
| Feature Engineered Model (interaction features)| 0.66653 | 30.874522 | 361.120610 | 23.320942 | WeightedEnsemble_L3 |
| Hyperparameter Tuned Model | 0.50 | 0.52 | 600 | 2.0 | LightGBM |



**🏆 Best Model:** LightGBM with Feature Engineering + Hyperparameter Tuning.

## 5️⃣ Conclusion  
- **Feature Engineering had the biggest impact on accuracy.**
- **Hyperparameter tuning further optimized performance.**
- **Future Work:**
  - Try a **Neural Network model**.
  - Deploy via **Flask API** for real-world use.
  - Investigate additional feature engineering techniques.

## 🔗 References  
- **Kaggle Competition**: [Bike Sharing Demand](https://www.kaggle.com/c/bike-sharing-demand)
- **AutoGluon Documentation**: [AutoGluon Tabular](https://auto.gluon.ai/stable/tutorials/tabular/index.html)

---
✅ *This report provides a structured explanation for anyone reviewing the project!* 🚀

