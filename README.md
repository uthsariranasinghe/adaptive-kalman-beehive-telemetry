# adaptive-kalman-beehive-telemetry
Adaptive Measurement Noise for Robust Kalman Filtering in Smart Beehive Telemetry
# Adaptive Kalman Filtering for Smart Beehive Telemetry

## What This Is
This repository contains code for adaptive measurement-noise 
Kalman filtering applied to multimodal smart beehive telemetry 
data (temperature, humidity, and audio). The framework includes:
- Linear Kalman Filter (fixed-R)
- Adaptive-R Kalman Filter with NIS-based gating
- Extended Kalman Filter (EKF)
- Ensemble Kalman Filter (EnKF)
- ARIMA/SARIMAX baseline

## Dataset
This project uses the publicly available MSPB dataset:
Zhu et al., 2024. DOI: 10.1038/s41597-024-03695-1

Download the dataset and place it in the `data/` folder 
before running the notebooks.

## Requirements
- Python 3.8 or higher

Install dependencies:
pip install -r requirements.txt

## How to Run
Run the notebooks in this order:

1. 01_preprocessing.ipynb  
   → Cleans raw telemetry, handles missing values, 
     aligns to 15-minute grid, applies quality control

2. 02_kalman_filters.ipynb  
   → Runs all filter implementations on the 
     preprocessed data

3. 03_evaluation.ipynb  
   → Computes accuracy, calibration metrics, 
     NIS diagnostics, and generates all plots




## License
MIT License
