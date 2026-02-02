Advanced Multivariate Time Series Forecasting

Evidence-based implementation of Transformer, LSTM, and SARIMA models for multivariate time series forecasting.
This project generates a synthetic multivariate dataset, trains deep learning and classical models, and benchmarks their forecasting performance using real metrics and visualizations.
 Project Overview

This repository demonstrates:

Synthetic multivariate time series generation

End-to-end forecasting pipeline

Comparison of:

🔹 Transformer (Multi-Head Attention)

🔹 LSTM baseline

🔹 SARIMA (classical statistical model)

Quantitative evaluation using RMSE and MAE

Saved datasets, metrics, plots, and attention visualizations for reproducibility

 Models Implemented
1. Transformer

Multi-Head Self-Attention

Layer Normalization

Global Average Pooling

Dense prediction head

Optimized with Huber loss

2. LSTM Baseline

Single LSTM layer

Dense multi-step output

Same loss and evaluation for fair comparison

3. SARIMA

Seasonal ARIMA with:

Trend

Seasonal periodicity

Used as a classical statistical benchmark

 Project Structure
.
├── data/
│   └── generated_multivariate_timeseries.csv
│
├── results/
│   ├── metrics.csv
│   └── plots/
│       ├── raw_timeseries.png
│       ├── forecast_comparison.png
│       └── attention_weights.png
│
├── final2.py
└── README.md

 Dataset

2000 time steps

3 correlated time series

Components:

Linear trend

Multiple seasonal patterns

Gaussian noise

Automatically saved to:

data/generated_multivariate_timeseries.csv

 Forecasting Setup

Input window: 100 time steps

Forecast horizon: 24 steps

Target: Series1

Train/Test split: 80% / 20%

Scaling: StandardScaler (inverse-transformed for evaluation)

 Evaluation Metrics

Models are evaluated on inverse-scaled data using:

RMSE (Root Mean Squared Error)

MAE (Mean Absolute Error)

Final Benchmark Results
Transformer RMSE: 8.173, MAE: 6.970
LSTM RMSE       : 3.738, MAE: 3.045
SARIMA RMSE     : 51.480, MAE: 44.257


Results are saved to:

results/metrics.csv

 Visualizations

Generated automatically during execution:

Raw multivariate time series

Forecast comparison (first test window)

Temporal attention strength from Transformer

Saved under:

results/plots/

 How to Run
1. Install Dependencies
pip install numpy pandas matplotlib scikit-learn tensorflow statsmodels

2. Run the Script
python final2.py


All datasets, metrics, and plots will be generated automatically.

🔬 Key Takeaways

Deep learning models significantly outperform SARIMA on this dataset

LSTM performs best numerically, while Transformer provides:

Better interpretability via attention

Strong multi-step forecasting capability

The pipeline is fully reproducible and evidence-backed

📜 License

This project is provided for educational and research purposes.
