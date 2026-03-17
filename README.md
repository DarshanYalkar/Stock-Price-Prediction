# 📈 Stock Price Prediction using Machine Learning & Deep Learning

## 📖 Overview

This project focuses on predicting stock prices of companies listed on the **New York Stock Exchange (NYSE)** using historical data.

It uses **Machine Learning and Deep Learning techniques (RNN, LSTM, GRU)** to analyze past stock trends and predict future prices.

---

## 🎯 Aim

To build a model that predicts stock prices using historical data from the NYSE dataset, where:

* **80% data** is used for training
* **20% data** is used for testing

---

## 🛠️ Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* Keras / TensorFlow
* Deep Learning (RNN, LSTM, GRU)

---

## 📂 Dataset Description

### 1. `prices.csv`

Contains stock price data:

* **Date** → Trading date

* **Symbol** → Company code

* **Open** → Opening price

* **Close** → Closing price

* **Low** → Lowest price

* **High** → Highest price

* Total Records: **851,264**

* Covers multiple companies (≈ 501)

---

### 2. `securities.csv`

Contains company details:

* **Ticker Symbol**
* **Company Name**
* **Sector**
* **Sub Industry**
* **Headquarters Location**

---

## ⚙️ Installation

### 1. Clone Repository

```bash
git clone https://github.com/your-username/stock-price-prediction.git
cd stock-price-prediction
```

### 2. Install Dependencies

```bash
pip install numpy pandas matplotlib scikit-learn tensorflow keras
```

---

## 🚀 Project Workflow

### 1. Data Loading

* Load dataset using Pandas
* Explore structure, shape, and columns

---

### 2. Data Analysis

* Check:

  * Missing values
  * Duplicate records
  * Unique companies
* Perform statistical analysis using `.describe()`

---

### 3. Data Visualization

Selected companies:

* Yahoo
* Xerox
* Microsoft
* Facebook
* Adobe
* Goldman Sachs

Graphs plotted:

* Opening price vs Time
* Closing price vs Time

---

### 4. Data Preprocessing

#### 🔹 Feature Scaling

* Normalize data using **MinMaxScaler (0–1)**

#### 🔹 Train-Test Split

* 80% Training
* 20% Testing

---

### 5. Data Preparation

* Use previous values to predict next value
* Example: Use last **10 values → predict next value**

```python
def process_data(data, n_features):
    ...
```

---

### 6. Model Building

Model Architecture:

* GRU Layer (256 units)
* Dropout (0.4)
* LSTM Layer (256 units)
* Dropout (0.4)
* Dense Layer (64 units, ReLU)
* Output Layer (1 neuron)

---

### 7. Model Compilation

* Loss Function: Mean Squared Error
* Optimizer: Adam

```python
model.compile(loss='mean_squared_error', optimizer=Adam(0.0005))
```

---

### 8. Model Training

* Epochs: 100
* Batch Size: 128
* Callbacks:

  * ReduceLROnPlateau
  * ModelCheckpoint

---

### 9. Prediction

* Predict stock prices using test data
* Convert predictions back to original scale

---

### 10. Evaluation

* Metric Used: **R² Score**

```python
from sklearn.metrics import r2_score
```

---

### 11. Visualization

* Blue Line → Actual Prices
* Red Line → Predicted Prices

---

## 📊 Results

* Model successfully predicts stock trends
* Shows strong correlation between actual and predicted values
* Accuracy evaluated using **R² score**

---

## 📌 Key Features

✔ Data Analysis & Visualization
✔ Time Series Prediction
✔ Deep Learning Model (GRU + LSTM)
✔ Feature Scaling
✔ Model Evaluation
✔ Graphical Comparison of Results

---

## ⚠️ Limitations

* Prediction accuracy depends on historical data quality
* Market volatility is not fully captured
* Requires high computational power

---

## 🔮 Future Improvements

* Use real-time stock data
* Implement advanced models (Transformer, Prophet)
* Add multi-stock prediction
* Deploy as a web app

---

## 👨‍💻 Author

**Darshan Yalkar**
