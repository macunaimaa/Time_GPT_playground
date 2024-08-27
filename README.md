# Time_GPT_playground
## Time Series Analysis and Anomaly Detection

This repository contains Jupyter notebooks for time series forecasting and anomaly detection using the Nixtla API. The main focus is on predicting future values of the S&P 500 index and detecting anomalies in voltage data from a motor.

## Table of Contents

- [Introduction](#introduction)
- [Project Structure](#project-structure)
- [Requirements](#requirements)
- [Usage](#usage)
  - [Time Series Forecasting](#time-series-forecasting)
  - [Anomaly Detection](#anomaly-detection)
- [Explanation of TimeGPT](#explanation-of-timegpt)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project explores two primary use cases:

1. **Time Series Forecasting**: Predicting future values of the S&P 500 index using advanced time series models.
2. **Anomaly Detection**: Detecting anomalies in voltage readings from a motor, which can be useful for predictive maintenance and fault detection.

Both tasks are implemented using the Nixtla API, leveraging its powerful `TimeGPT` model for forecasting and built-in anomaly detection capabilities.

## Project Structure

- `sp_analysiss.ipynb`: Jupyter notebook for time series forecasting of the S&P 500 index.
- `motor_analysis.ipynb`: Jupyter notebook for detecting anomalies in voltage data from a motor.
- `data/`: Directory containing datasets used in the analysis.

## Requirements

- Python 3.x
- Jupyter Notebook
- Nixtla Python package

Install the required Python packages using:

```bash
pip install nixtla pandas numpy matplotlib
```

## Usage
### Time Series Forecasting

The notebook `sp_analysiss.ipynb` focuses on forecasting the S&P 500 index. The steps involved are:

- **Loading the Dataset**: The S&P 500 index data is loaded from a CSV file.
- **Data Visualization**: The dataset is visualized to understand trends and patterns.
- **Forecasting with TimeGPT**: The TimeGPT model from Nixtla is used to predict future values of the S&P 500 index.
- **Evaluation**: The forecasted values are compared with real values to calculate prediction error and visualize accuracy.

### Anomaly Detection

The notebook motor_analysis.ipynb is used for detecting anomalies in motor voltage data. The workflow includes:

- **Loading the Dataset**: Voltage data is loaded from a text file and preprocessed.
- **Data Cleaning and Transformation**: The data is cleaned, and mean voltage is calculated for different phases.
- **Anomaly Detection**: Anomalies are detected using Nixtla's anomaly detection function.
- **Visualization**: Voltage data and detected anomalies are visualized to identify irregular patterns.

## Explanation of TimeGPT

TimeGPT is a time series forecasting model developed by Nixtla. It uses advanced machine learning techniques, possibly leveraging the principles of the Transformer architecture, to make accurate predictions on time series data. TimeGPT is designed to handle various types of time series data, making it a versatile tool for forecasting tasks.

## Results
Time Series Forecasting: Achieved accurate predictions for the S&P 500 index. The mean absolute error between predicted and real values is calculated to assess performance.
Anomaly Detection: Successfully identified anomalies in voltage data, providing insights into potential faults or irregularities in the motor.
Contributing
Contributions are welcome! Please fork the repository and submit a pull request for any improvements or bug fixes.

## License
This project is licensed under the MIT License. See the LICENSE file for more information.