# Cryogenic-Digital-Twin

## Overview
This project showcases a comprehensive AI/ML-based Digital Twin for a cryogenic chamber system. The pipeline (mentioned below) is designed to predict, analyze, and detect anomalies in critical system conditions like temperature and pressure:
- Data simulation and preprocessing
- Time-series forecasting with LSTM
- Interactive deployment for real-time analysis
- Anomaly detection for system health monitoring

## Quick Look at the Outputs

### Exploratory Data Analysis
![image](https://github.com/user-attachments/assets/e50a4a10-047a-4eed-b901-d76485eb816b)
![image](https://github.com/user-attachments/assets/cd8fac72-a7f0-4d5c-a65b-41822812c3d6)

### Model Training Outputs
![image](https://github.com/user-attachments/assets/51cc68c5-af52-4565-9575-94415ebfd98a)
![image](https://github.com/user-attachments/assets/0633ba53-2154-46f2-b057-4eb2c7d08247)

### Anomaly Detection
![image](https://github.com/user-attachments/assets/a27281e4-42b3-40f2-aa7e-62a4ec503199)

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
  








