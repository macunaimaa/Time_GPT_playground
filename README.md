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
  - [Features and capabilities](#Features-and-capabilities)
  - [Architecture](#Architecture)
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

TimeGPT is a production-ready generative pretrained transformer for time series. It’s capable of accurately predicting various domains such as retail, electricity, finance, and IoT with just a few lines of code.

It is user-friendly and low-code. Users can simply upload their time series data and generate forecasts or detect anomalies with just a single line of code.

TimeGPT is the only out of-the-box foundation model for time series that can be used through our public APIs, through Azure Studio (comming soon) or on your own infrastructure.

### Features and capabilities
Zero-shot Inference: TimeGPT can generate forecasts and detect anomalies straight out of the box, requiring no prior training data. This allows for immediate deployment and quick insights from any time series data.

Fine-tuning: Enhance TimeGPT’s capabilities by fine-tuning the model on your specific datasets, enabling the model to adapt to the nuances of your unique time series data and improving performance on tailored tasks.

API Access: Integrate TimeGPT seamlessly into your applications via our robust API. Upcoming support for Azure Studio will provide even more flexible integration options. Alternatively, deploy TimeGPT on your own infrastructure to maintain full control over your data and workflows.

Add Exogenous Variables: Incorporate additional variables that might influence your predictions to enhance forecast accuracy. (E.g. Special Dates, events or prices)

Multiple Series Forecasting: Simultaneously forecast multiple time series data, optimizing workflows and resources.

Specific Loss Function: Tailor the fine-tuning process by choosing from many loss functions to meet specific performance metrics.

Cross-validation: Implement out of the box cross-validation techniques to ensure model robustness and generalizability.

Prediction Intervals: Provide intervals in your predictions to quantify uncertainty effectively.

Irregular Timestamps: Handle data with irregular timestamps, accommodating non-uniform interval series without preprocessing.

Anomaly Detection: Automatically detect anomalies in time series, and use exogenous features for enhanced performance.

### Architecture
Self-attention, the revolutionary concept introduced by the paper Attention is all you need, is the basis of this foundation model. TimeGPT model is not based on any existing large language model(LLM). Instead, it is independently trained on a vast amount of time series data, and the large transformer model is designed to minimize the forecasting error.


The architecture consists of an encoder-decoder structure with multiple layers, each with residual connections and layer normalization. Finally, a linear layer maps the decoder’s output to the forecasting window dimension. The general intuition is that attention-based mechanisms are able to capture the diversity of past events and correctly extrapolate potential future distributions.

To make prediction, TimeGPT “reads” the input series much like the way humans read a sentence – from left to right. It looks at windows of past data, which we can think of as “tokens”, and predicts what comes next. This prediction is based on patterns the model identifies in past data and extrapolates into the future.


## Results
Time Series Forecasting: Achieved accurate predictions for the S&P 500 index. The mean absolute error between predicted and real values is calculated to assess performance.
Anomaly Detection: Successfully identified anomalies in voltage data, providing insights into potential faults or irregularities in the motor.
Contributing
Contributions are welcome! Please fork the repository and submit a pull request for any improvements or bug fixes.

## License
This project is licensed under the MIT License. See the LICENSE file for more information.