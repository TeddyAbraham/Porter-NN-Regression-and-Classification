# Porter-Delivery-Time-Prediction (ML & Neural Networks)

## 📌 Project Overview
This project predicts **food delivery time (in minutes)** using machine learning and neural network models. The workflow includes **data preprocessing, feature engineering, hypothesis testing, outlier treatment, and model building** for both **regression and classification tasks**. The objective is to identify operational drivers affecting delivery time and develop predictive models that can support **logistics optimization and delivery ETA systems**.

---

## 🔄 Process & Methodology

### 1. Data Loading & Exploratory Data Analysis (EDA)
- Load dataset using `pandas.read_csv()` or `read_parquet()`
- Inspect dataset structure: shape, data types, missing values, and summary statistics
- Analyze feature distributions and relationships
- Identify operational variables influencing delivery time

---

### 2. Data Preprocessing & Feature Engineering

**Data Cleaning**
- Handle missing values using appropriate imputation or removal
- Normalize inconsistent categorical entries
- Convert datetime columns to proper datetime format

**Feature Engineering**
- `Actual_time_taken = actual_delivery_time - created_at` → converted to minutes
- Extract time-based features:
  - `hour_of_day`
  - `day_of_week`
- Derive additional operational features such as approximate restaurant preparation time
- Use pandas datetime accessor (`.dt.hour`, `.dt.weekday`, `.dt.total_seconds()`)

**Encoding**
- Apply **One-Hot Encoding** to categorical variables
- Transform categorical features into model-compatible numeric format

---

## 📊 Visualization & Outlier Treatment
- Use **histograms, boxplots, bar plots, and scatter plots** to explore feature distributions
- Detect outliers using:
  - **IQR method**
  - **Z-score**
  - Domain-based filtering
- Remove or cap extreme values to stabilize model performance
- Re-visualize distributions after outlier treatment

---

## 🧪 Hypothesis Testing & Feature Importance
- Conduct statistical hypothesis tests to evaluate relationships between variables and delivery time
- Analyze correlations and statistical significance
- Train tree-based models (e.g., XGBoost) to evaluate **feature importance**
- Use insights to guide feature selection and model design

---

## 🤖 Machine Learning Models

### Regression Models
Used to predict **exact delivery time in minutes**

Examples:
- Linear Regression
- Random Forest Regressor
- Gradient Boosting / XGBoost

Evaluation Metrics:
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)

---

### Classification Models
Used to categorize deliveries into **time-based buckets (e.g., Fast / Medium / Slow)**

Examples:
- Logistic Regression
- Random Forest Classifier
- Gradient Boosting Classifier

Evaluation Metrics:
- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

---

## 🧠 Neural Network Model (Deep Learning)

**Architecture**
- Input Layer
- Multiple Dense Hidden Layers
- Output Layer:
  - Linear activation for regression
  - Sigmoid / Softmax for classification

**Training Configuration**
- Optimizer: `Adam`
- Loss Functions:
  - `Mean Squared Error` (Regression)
  - `Binary/Categorical Crossentropy` (Classification)
- Activation: `ReLU` in hidden layers
- Feature scaling using `StandardScaler`

**Model Tuning**
- Experiment with number of layers, neurons, batch size, and epochs
- Monitor **training vs validation loss**
- Apply **EarlyStopping** to reduce overfitting

---

## 📈 Model Evaluation & Results
- Compare performance across machine learning and neural network models
- Evaluate prediction quality using regression and classification metrics
- Visualize:
  - Training vs validation loss curves
  - Predicted vs actual delivery times
- Analyze feature importance and operational insights

---

## 🚀 Business Applications
- Improve **delivery time estimation systems**
- Assist in **driver allocation and routing decisions**
- Identify operational bottlenecks affecting delivery performance
- Enhance **customer experience through more accurate ETA predictions**


## 6.	Screenshots / Demos
Show what the dashboard looks like.
Example: ![Dashboard Preview]([https://github.com/the-mansi-goel/Ski-dashboard/blob/main/Snapshot%20of%20the%20Dahbaord.png](https://github.com/TeddyAbraham/Porter-NN-Regression-and-Classification/blob/main/Porter%20Food%20Delivery%20Analysis.png))
