# Hybrid VMD and DWT - Deep Learning for Short-Term Electricity Load Forecasting

This repository contains the source code and experimental models for short-term electricity load forecasting in the Central Java and D.I. Yogyakarta provinces. 

## 📌 Overview
Electrical load data is characterized by non-linear, non-stationary, and highly fluctuating patterns. To overcome the challenges of standard forecasting methods, this project proposes a hybrid approach integrating signal decomposition techniques with Deep Learning architectures. The models are trained on daily electrical load records spanning from January 1, 2016, to October 31, 2025. This research aims to ensure precise energy supply management and support the global Sustainable Development Goals (SDGs), particularly Goal 7 regarding clean and affordable energy.

## 🧠 Methodology
The forecasting framework is built upon a "Decomposition-Optimization-Modeling-Reconstruction" pipeline:
* **Signal Decomposition**: Utilizes Variational Mode Decomposition (VMD) and Discrete Wavelet Transform (DWT) to mitigate data volatility and extract stable frequency sub-signals.
* **Deep Learning Models**: Implements Long Short-Term Memory (LSTM), Gated Recurrent Unit (GRU), and Bidirectional GRU (BiGRU) networks to learn complex temporal dependencies.
* **Hyperparameter Tuning**: Employs Bayesian Optimization via the Optuna framework for automated and objective parameter tuning.
* **Evaluation Metrics**: Model performance is rigorously evaluated using Mean Squared Error (MSE), Root Mean Squared Error (RMSE), Mean Absolute Percentage Error (MAPE), and the coefficient of determination (R^2).

## 🏆 Key Findings
* The integration of decomposition techniques significantly enhances prediction accuracy compared to utilizing single Deep Learning models.
* The **VMD-LSTM** hybrid model with a 7-day time step demonstrated the most optimal performance across all tests.
* The best model achieved an outstanding MAPE of 0.58% and an R^2 of 98.81%.
* Utilizing the VMD-LSTM method successfully reduced the error rate by up to 75.53% when compared to the best performing standard baseline model.

## 🛠️ Main Libraries Used
* **Deep Learning**: LSTM, GRU, and BiGRU architectures.
* **Optimization**: `Optuna` framework for Bayesian Optimization.
* **Signal Processing**: `vmdpy` library for VMD implementation and `PyWavelets` library for DWT implementation.
