# Predictive-maintenance-nasa
Predictive maintenance using NASA turbofan sensor data
# 🔧 Predictive Maintenance System – NASA Turbofan Dataset

---

## 📌 Project Overview
This project implements an end-to-end **predictive maintenance system** using machine learning to anticipate turbofan engine failures before they occur.

By analyzing multivariate sensor data collected over an engine’s operational life, the model identifies early degradation patterns and predicts failure risk, enabling **proactive maintenance decisions** and reducing unplanned downtime.

---

## 🧠 Problem Statement
Unplanned equipment failures lead to operational delays and increased maintenance costs.

The objective of this project is to:
- Analyze time-series sensor data from turbofan engines
- Detect early degradation trends
- Predict **engine failure within the next 30 operational cycles**

The problem is framed as a **binary classification task**:
- **1 → Engine likely to fail within 30 cycles**
- **0 → Normal engine operation**

---

## 📊 Dataset
**NASA C-MAPSS Turbofan Engine Degradation Dataset**

### Dataset Files Used
The following training files are used and combined in this project:
- `train_FD001.txt`
- `train_FD002.txt`
- `train_FD003.txt`
- `train_FD004.txt`

Each file contains run-to-failure time-series data for multiple engines under different operating and fault conditions.

### Dataset Structure
Each record represents one engine at one operational cycle and includes:
- Engine ID
- Cycle number
- 3 operational settings
- 21 sensor measurements (temperature, pressure, vibration, etc.)

---

## 🧭 Project Workflow

### 1️⃣ Data Loading
- Uploaded all dataset files to Google Colab
- Loaded raw `.txt` files using correct whitespace parsing
- Labeled each dataset by source file
- Combined all four datasets into a single dataframe

### 2️⃣ Data Preprocessing
- Validated engine ID and cycle integrity
- Removed non-predictive identifiers
- Prepared clean input features for modeling

### 3️⃣ Feature Engineering
- Computed **Remaining Useful Life (RUL)** for each engine
- Converted RUL into a binary failure label using a 30-cycle threshold
- Created final feature matrix and target variable

### 4️⃣ Exploratory Data Analysis
- Analyzed class imbalance between failure and normal states
- Visualized sensor degradation trends across engine life cycles
- Identified early warning patterns prior to failure

### 5️⃣ Model Development
- **Baseline Model:** Logistic Regression
- **Primary Model:** Random Forest Classifier
- Addressed class imbalance using class-weighted learning

### 6️⃣ Model Evaluation
Evaluation focused on minimizing missed failures:
- Confusion Matrix
- Recall (primary metric)
- ROC-AUC score
- Decision threshold tuning

---

## 📈 Results Snapshot
- Strong recall achieved on the failure class
- ROC-AUC demonstrates good class separation
- High-risk engines can be identified up to 30 cycles in advance

---

## 🛠️ Tech Stack
- **Programming Language:** Python  
- **Data Processing:** Pandas, NumPy  
- **Machine Learning:** Scikit-learn  
- **Visualization:** Matplotlib, Seaborn  
- **Environment:** Google Colab  

---

## 💼 Business Impact
The predictive maintenance solution enables:
- Proactive maintenance scheduling
- Reduced unplanned downtime
- Lower maintenance and operational costs
- Improved equipment reliability and safety

---

## ▶️ How to Run
1. Upload the dataset files to Google Colab:
   - `train_FD001.txt`
   - `train_FD002.txt`
   - `train_FD003.txt`
   - `train_FD004.txt`
2. Open `predictive_maintenance_nasa_turbofan.ipynb`
3. Run all cells in order

---

## ⚠️ Limitations
- The dataset is simulated and may not capture all real-world noise
- Temporal dependencies are not fully modeled
- Performance may vary across unseen operating conditions

---

## 📁 Repository Structure

🙋‍♂️ Author
Divya Kathare
SQL • Data Analyst • Data Science Enthusiast
GitHub: https://github.com/Divya-Kathare
LinkedIn: https://www.linkedin.com/in/divya-kathare-41323a3a0
