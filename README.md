# 🚗 Vehicle Trajectory Prediction with LSTM and Residual Correction

This project predicts short-term vehicle trajectories on highways using real-world traffic data from the NGSIM US-101 dataset.

The approach combines sequence learning with residual error correction to improve trajectory prediction accuracy.

---

## 🎯 Objectives

- Predict short-term future vehicle positions from time-series trajectory data
- Learn motion patterns using deep learning
- Improve prediction stability through residual error correction
- Evaluate performance using real-world highway traffic data

---

## 📊 Dataset

NGSIM US-101 highway trajectory dataset.

Includes:

- Vehicle positions (X, Y)
- Velocity and acceleration
- Lane information
- Time-series tracking data

Preprocessing steps:

- Remove tracking noise and inconsistencies
- Convert units (feet → meters)
- Normalize features
- Generate time-series sequences

---

## 🧠 Model Approach

### LSTM Trajectory Predictor
Learns temporal motion patterns and predicts future vehicle positions.

### Residual Error Correction (XGBoost)
Learns prediction errors from LSTM output and corrects lateral movement (Y-axis).

### Hybrid Output
Final prediction:

- X coordinate → LSTM output  
- Y coordinate → LSTM + residual correction  

---

## 📈 Results

- Reduced prediction error compared to LSTM-only model
- ~11.5% improvement in mean squared error (MSE)
- Improved stability in lateral trajectory prediction

---

## 📓 Project Workflow

The project is implemented through Jupyter notebooks:

1️⃣ Data preprocessing  
→ `Data_PreProcessing.ipynb`

2️⃣ Sequence generation and feature preparation  
→ `Data_processing.ipynb`

3️⃣ Model training and evaluation  
→ `Model_Final1.ipynb`

---

## 🛠️ Tech Stack

- Python
- TensorFlow / Keras
- XGBoost
- NumPy
- Pandas
- Scikit-learn
- Matplotlib

---

## ▶️ How to Run

Run notebooks in order:

1. Data_PreProcessing.ipynb  
2. Data_processing.ipynb  
3. Model_Final1.ipynb  

---

## 📄 Documentation

- Project report (PDF)
- Model presentation slides (PPT)

These files describe methodology, experiments, and results in detail.

---

## 🔬 Future Work

- Longer prediction horizons
- Additional motion features
- Transformer-based models
- Real-time prediction system
