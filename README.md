# 🏁 Emilia-Romagna Grand Prix Race Position Predictor

This project predicts the **finishing positions** of **Alex Albon** and **Carlos Sainz**, and estimates the **Constructors' points** for **Williams Racing** in the Emilia-Romagna Grand Prix using historical Formula 1 data (1950–2020) from Kaggle.

---

## 📌 Problem Statement

**Objective:**  
Predict driver finishing positions and calculate expected constructors’ points for an upcoming race using machine learning models (Random Forest and XGBoost).  

**Focus:**
- **Drivers:** Alex Albon and Carlos Sainz  
- **Constructor of Interest:** Williams Racing  
- **Race Circuit:** Emilia-Romagna

---

## 📂 Dataset

- Source: [rohanrao/formula-1-world-championship-1950-2020](https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020)
- Downloaded using [`kagglehub`](https://pypi.org/project/kagglehub/)

---

## 📊 Key Features Used

- `grid` (starting position)
- `year`
- `points_x` (driver’s points before the race)
- `position_y` (last known finishing position)
- `avg_lap_time`, `fastest_lap_time`, `lap_time_stddev`

---

## 🧠 Model Workflow

1. **Data Preprocessing**  
   Merge multiple datasets: results, lap times, standings, constructors, drivers, constructor_results, driver_standings and races.

3. **Feature Engineering**  
   Aggregate lap time metrics and convert columns to numerical formats.

4. **Driver Filtering**  
   Focus on Albon and Sainz's historical performance in Emilia-Romagna races (2020–2024).

5. **Model Training**
   - Train/test split  
   - Standardization  
   - Grid search over **Random Forest** hyperparameters  
   - Baseline comparison with **XGBoost**

6. **Prediction Output**  
   - Predict finish positions  
   - Estimate Constructors' points using the F1 scoring system  

---

## 📈 Visualizations

- Average Lap Time Distribution (Albon vs. Sainz)
- Grid vs. Finish Position Scatter Plot
- Feature Correlation Heatmap

---

## 🧪 Requirements

Install dependencies:

```bash
pip install kagglehub pandas numpy matplotlib seaborn scikit-learn xgboost
```
---

## 🧑‍💻 Author
This project was developed using Python with scikit-learn and XGBoost for machine learning and Matplotlib/Seaborn for visual analytics.


