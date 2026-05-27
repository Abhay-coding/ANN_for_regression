# ⚡ Combined Cycle Power Plant Output Prediction (ANN Regression)

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)

A regression-based Deep Learning project that predicts the **net hourly electrical energy output (EP)** of a power plant using environmental readings. Built with **PyTorch**.

---

## 📖 Overview
The dataset contains 9,568 data points collected from a Combined Cycle Power Plant over 6 years when the plant was set to work with a full load.

### 📉 Features (Inputs)
- **AT:** Ambient Temperature
- **V:** Exhaust Vacuum
- **AP:** Ambient Pressure
- **RH:** Relative Humidity

### 🎯 Target (Output)
- **PE:** Net hourly electrical energy output

---

## 🛠️ Technical Architecture

### 🧠 Model Structure (Regression)
The model is an **Artificial Neural Network (ANN)** designed for continuous value prediction:
- **Input Layer:** 4 Features
- **Hidden Layer 1:** 64 Neurons + ReLU Activation
- **Hidden Layer 2:** 64 Neurons + ReLU Activation
- **Output Layer:** 1 Neuron (Linear activation for regression)

### ⚙️ Training Process
* **Loss Function:** Mean Squared Error (MSE)
* **Optimizer:** Adam
* **Preprocessing:** `StandardScaler` for feature normalization
* **Persistence:** The best-performing model state is saved as `Best_model.pt`.

---

## 📊 Performance
The model accurately predicts power output with minimal variance between predicted and actual values.

| Component | Detail |
| :--- | :--- |
| **Data Split** | 80% Train | 20% Test |
| **Framework** | PyTorch |
| **Saved Model** | `Best_model.pt` |

---

## 📂 Project Structure
```bash
.
├── powerplant_data.csv    # Dataset (AT, V, AP, RH, PE)
├── ANN_Regression.ipynb   # Training script & Data Analysis
├── Best_model.pt          # Saved PyTorch model weights
└── README.md              # Project documentation
