# Porter-Delivery-Time-Prediction 
### Tech Stack: Python | Pandas | Scikit-learn | ML |Linear Regression | Random Forest |XGBoost | Neural Network | TensorFlow | Power BI

## 📌 Project Overview
This project predicts **food delivery time (in minutes)** using **machine learning, neural networks, and business intelligence analysis**.

The workflow combines **EDA, feature engineering, hypothesis testing, predictive modeling, and interactive Power BI dashboards** to identify operational drivers affecting delivery time.

The goal is to support **logistics optimization, driver allocation, and ETA prediction systems**.

---

# 🔄 Project Workflow

## 1️⃣ Data Loading & Exploratory Data Analysis (EDA)

- Inspect dataset structure, missing values, and summary statistics
- Explore feature distributions and correlations
- Identify operational variables influencing delivery time

---

## 2️⃣ Data Preprocessing & Feature Engineering

### Data Cleaning
- Handle missing values
- Convert datetime columns

### Feature Engineering

Key engineered features:

- `Actual_time_taken = actual_delivery_time - created_at`
- `hour_of_day`, `day_of_week`
- Restaurant preparation time approximation
---

## 3️⃣ Visualization & Outlier Treatment

Visualization techniques:

  Histograms |Boxplots |Scatter plots |Count plots

Outlier detection methods:

- **IQR Method**
- **Z-Score**
- Domain based filtering

Extreme values were clipped or removed to improve model stability.

---

## 4️⃣ Hypothesis Testing & Feature Importance

Statistical tests were used to validate relationships between variables and delivery time.

Tree-based models such as **XGBoost** were used to evaluate **feature importance**, helping identify the strongest operational drivers.

---

# 🤖 Machine Learning Models

### Regression Models
Predict **exact delivery time in minutes**

Models used:

  Linear Regression | Random Forest |XGBoost

Evaluation Metrics:

  MSE |RMSE |MAE

---

### Classification Models
Categorize deliveries into **time buckets**

Examples:

- Fast
- Medium
- Slow deliveries

---

# 🧠 Neural Network Model

### Architecture
- Input Layer
- Dense Hidden Layers (ReLU activation)
- Output Layer (Linear / Softmax)

### Training Configuration
- Optimizer → Adam
- Loss → MSE / Crossentropy
- Feature scaling using `StandardScaler`
- EarlyStopping to reduce overfitting

Model performance was evaluated using **training vs validation loss curves** and **prediction error metrics**.

---

# 📈 Model Results

| Model | MAE | RMSE |
|-----|-----|-----|
| Linear Regression | ~2.4 | ~3.2 |
| Random Forest | ~1.19 | ~1.63 |
| XGBoost | **~0.85** | **~1.15** |

**XGBoost achieved the best performance in ML**, significantly reducing prediction error compared to the baseline model.

| Model | MAE |
|-----|-----|
| Neural Network | **~0.49** | 

**Neural Outperformed XGBoost**, reducing the prediction error even better.
---

# 🚀 Business Applications

- Improve **ETA prediction systems**
- Optimize **driver allocation**
- Reduce **delivery delays during peak hours**
- Identify **high-delay markets**
- Support **logistics planning and operational strategy**

---
# 📊 Power BI Dashboard Analysis

An interactive **Power BI dashboard** was developed to analyze operational performance and visualize delivery patterns.

### Dashboard Metrics

- Average Delivery Time → **40.44 minutes**
- Average Preparation Time → **31.34 minutes**
- Average Driving Time → **9.10 minutes**
- Total Orders → **175K+**
- Total Order Value → **474M**

### Key Operational Insights

**1️⃣ Driver Utilization**

- **62% of orders occur during understaffed periods**
- Indicates demand frequently exceeds available drivers.

**2️⃣ Delivery Time Drivers**

Delivery time is mainly influenced by:

- Restaurant preparation time
- Number of outstanding orders
- Available drivers in a market

**3️⃣ Peak Order Hours**

Two major peaks observed:

- **0hrs to 5hrs**
- **18hrs to 23hrs**


It is unusual since normally the peak time should be during lunch and dinner time. Possible explaination - This data might be of different country probabily *USA*

**4️⃣ Market Performance Variation**

Some markets show significantly **higher delivery times**, indicating:

- Supply-demand imbalance
- Operational inefficiencies.

---
## 📊 Dashboard Preview

![Dashboard Preview](https://github.com/TeddyAbraham/Porter-NN-Regression-and-Classification/blob/main/Porter%20Food%20Delivery%20Analysis.png)
