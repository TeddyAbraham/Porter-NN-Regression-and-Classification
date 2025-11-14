# Porter-NN-Regression

## 📌 Project Overview
This project predicts **delivery time (in minutes)** for customer orders using time-based feature engineering, preprocessing, outlier handling, and a Neural Network regression model (Keras/TensorFlow). The pipeline includes extracting datetime features, cleaning data, encoding categorical variables, and training/evaluating neural networks.

---

## 🔄 Process & Methodology

### 1. Import & Initial EDA
- Load dataset with `pandas.read_csv()` / `read_parquet()`
- Inspect shape, dtypes, missing values, unique counts, and summary statistics

### 2. Data Preprocessing
**Data cleaning**
- Handle missing values (drop or impute depending on context)
- Normalize inconsistent categorical entries

**Feature engineering**
- `delivery_time = actual_delivery_time - created_at` → convert to minutes
- Extract `hour_of_day = created_at.dt.hour`
- Extract `day_of_week = created_at.dt.weekday`
- Use `dt` accessor (`.dt.hour`, `.dt.weekday`, `.dt.total_seconds()`)

**Null handling**
- Ensure no missing values in target or essential features; impute where needed

**Encoding**
- One-Hot Encode categorical columns (or use target encoding if appropriate)

---

## 📊 Visualization & Outlier Handling
- Plot distributions: histograms, boxplots, countplots, scatterplots
- Detect outliers using IQR / Z-score / domain rules
- Remove or Winsorize outliers
- Re-plot to verify improvements

---

## 🧪 Train/Test Split & Scaling
- Split: `train_test_split(X, y, test_size=0.2, random_state=42)`
- Scale numeric features with `StandardScaler` (important for NN convergence)

---

## 🤖 Neural Network (Regression)
**Architecture**
- Input layer → Dense layers (varying units) → Output layer (1 neuron, linear activation)

**Training**
- Loss: `mean_squared_error`
- Metrics: MSE, RMSE, MAE
- Optimizer: `Adam` (adaptive learning, fast convergence)
- Activation: `ReLU` in hidden layers (prevents vanishing gradients)

**Experimentation**
- Try different layer sizes, activations, learning rates, batch sizes, and epochs
- Monitor training vs validation loss; use EarlyStopping if required

---

## 📈 Evaluation Metrics
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- Visualize training/validation loss curves
