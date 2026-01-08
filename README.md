# 🚦 Traffic Flow Prediction and Classification

This project presents a complete **machine learning pipeline for traffic flow analysis**, including **regression**, **multi-class classification**, and **binary classification**. The system predicts traffic volume, classifies congestion levels, and evaluates model performance using statistical metrics, visualization, and cross-validation.

The implementation is optimized for **Google Colab** and uses real-world traffic data.


---

## 📊 Dataset

### Download Link
Download the dataset and upload it to Colab before running the notebook:

🔗 https://drive.google.com/file/d/1mcmISHHaDD3GBBdw7DzTNev0T2RGCe9P/view?usp=sharing

### Dataset Description
The dataset contains traffic and environmental information such as:

- `time` – Hour of the day  
- `flow` – Traffic volume (target variable)  
- `id` – Sensor/location identifier  
- `long`, `lat` – Geographic coordinates  
- `temp` – Temperature  
- `desc` – Weather description code  
- `visibility` – Visibility level  
- `weekday` – Day of the week  
- `date` → converted to `date_as_int` (Unix timestamp)

---

## 🛠️ Technologies Used

- **Python**
- **Pandas & NumPy** – Data processing
- **Scikit-learn** – Machine learning models and evaluation
- **Matplotlib & Seaborn** – Visualization

---

## 🧠 Machine Learning Workflow

### 1️⃣ Traffic Flow Regression

**Objective:** Predict continuous traffic volume values.

- **Model:** Random Forest Regressor
- **Preprocessing:**
  - Date conversion to numerical timestamp
  - Feature scaling using `StandardScaler`
  - Train-test split (80% / 20%)
- **Evaluation Metrics:**
  - Mean Squared Error (MSE)
  - R² Score
- **Visualization:**
  - True vs. Predicted traffic volume scatter plot

**Results:**
- **MSE:** ~270  
- **R² Score:** ~0.94  

---

### 2️⃣ Multi-Class Traffic Classification (Softmax)

**Objective:** Classify traffic intensity into three categories.

| Class | Meaning |
|------|--------|
| Red | High traffic congestion |
| Yellow | Medium traffic |
| Green | Low traffic |

- **Model:** Logistic Regression (Softmax)
- **Data:** Simulated using `make_classification`
- **Metric:** Accuracy

**Result:**  
- **Accuracy:** ~65%

---

### 3️⃣ Binary Traffic Classification (High / Low)

**Objective:** Predict whether traffic flow is **High** or **Low**.

- **Label Definition:**
  - High → Flow > 50  
  - Low → Flow ≤ 50
- **Model:** Logistic Regression
- **Preprocessing:**
  - Feature normalization
  - 80/20 train-test split
- **Evaluation:**
  - Classification report
  - Confusion matrix with heatmap

**Result:**  
- **Accuracy:** ~80%

---

## 🔍 Feature Importance Analysis

- Extracted from the trained Random Forest model
- Visualized using a bar chart ranked by importance

### Why This Matters
- Improves model transparency
- Identifies the most influential features
- Supports feature selection and model optimization

---

## 🔁 Cross-Validation

- **Method:** 5-Fold Cross-Validation
- **Purpose:**
  - Evaluate model stability
  - Measure generalization performance
  - Reduce overfitting risk
- **Visualization:** Line plot of cross-validation scores

---

## 🧪 Real-Time Traffic Prediction

The project demonstrates how to predict traffic flow for **new, unseen input data**, enabling:

- Real-time traffic monitoring
- Route optimization
- Smart city and urban planning applications


---

## 📌 Key Takeaways

- Random Forest performs exceptionally well for traffic volume prediction
- Logistic Regression is effective for both binary and multi-class classification
- Feature scaling and preprocessing are critical for performance
- Visualization and cross-validation enhance reliability and interpretability
- The pipeline is suitable for real-world traffic prediction systems

---

## 🚀 How to Run

1. Open the notebook in **Google Colab**
2. Upload `traffic-flow-df.csv` to the Colab environment
3. Run all cells sequentially
4. Review model outputs, metrics, and visualizations

---

## 🔮 Future Enhancements

- Apply time-series models (LSTM, ARIMA)
- Use real labeled data for multi-class congestion levels
- Perform hyperparameter tuning
- Deploy the model as a web or API service

---

## 📄 License

This project is intended for **educational and research purposes**.



