# cryogenic-digital-twin

## Overview
This project showcases a comprehensive AI/ML-based Digital Twin for a cryogenic chamber system. The pipeline (mentioned below) is designed to predict, analyze, and detect anomalies in critical system conditions like temperature and pressure:
- Data simulation and preprocessing
- Time-series forecasting with LSTM
- Interactive deployment for real-time analysis
- Anomaly detection for system health monitoring

## Structure
The project is implemented in Jupyter Notebooks, split into the following modules:
- `Data_Generation_and_Collection.ipynb`: Simulates synthetic data representing cryogenic chamber states (temperature, pressure, etc.) to output a time-series dataset (`cryogenic_chamber_data.csv`) and visualizes generated data patterns
- `Preprocessing_and_Exploration.ipynb`: Prepares and explores data for modeling. The processed data is saved: `cryogenic_chamber_data_scaled.csv`
- `Model_Development_and_Training.ipynb`: Trains an LSTM-based time-series model to predict future chamber temperatures. The trained model is saved `cryogenic_temp_predictor.h5`
- `Digital_Twin_Deployment.ipynb`: Deploys the trained model in an interactive Digital Twin. It predicts system states based on user-defined inputs and recent data. The notebook further includes interactive widgets for live system simulation
- `Anomaly_Detection.ipynb`: Detects anomalies using an LSTM autoencoder trained on normal system data by flagging unusual system behaviour with reconstructing error threshold and saves results and the anomaly detection model `cryogenic_autoencoder.h5`

## How to Run

1. Set-up Environment
   1.1 Ensure Python 3.8+ is installed on your system
   1.2 Install all required libraries by running:
      ```bash
      pip install -r requirements.txt
   
3. Run Notebooks
   - Execute the notebooks in order:
     - Data_Generation_and_Collection.ipynb
     - Preprocessing_and_Exploration.ipynb
     - Model_Development_and_Training.ipynb
     - Digital_Twin_Deployment.ipynb
     - Anomaly_Detection.ipynb
       
5. Experiment
   - Test real-time predictions with interactive sliders in Digital_Twin_Deployment.ipynb
   - Visualize and analyze anomalies in Anomaly_Detection.ipynb
