# Real-Time Anomaly Detection in Data Streams

## Project Overview
This project implements a real-time anomaly detection system for continuous data streams using the Z-score algorithm. It's designed to identify unusual patterns or outliers in streaming data, which could represent various metrics such as financial transactions, system performance indicators, or sensor readings.

## Features
- Real-time anomaly detection using the Z-score algorithm
- Simulated data stream generation with injected anomalies
- Live visualization of the data stream and detected anomalies
- Adaptable to concept drift and seasonal variations

## Project Structure
The project consists of the following Python files:
- **main.py**: The entry point of the application. It orchestrates the data simulation, anomaly detection, and visualization.
- **simulation.py**: A standalone script for running the simulation without visualization, useful for testing or batch processing.
- **visualization.py**: Handles real-time plotting of the data stream and detected anomalies.
- **zscore_anomaly_detection.py**: Implements the Z-score algorithm for detecting anomalies in the data stream.
- **data_stream_simulator.py**: Generates a simulated data stream with occasional anomalies.

## Requirements
- Python 3.x
- NumPy
- Matplotlib

## Installation
Ensure you have Python 3.x installed on your system.

Install the required libraries:
```bash
pip install numpy matplotlib
```

## Usage

### To run the main application with visualization:
This will start the simulation and open a matplotlib window showing the real-time data stream and detected anomalies.

### To run the simulation without visualization:
This will run the simulation and print the detected anomalies to the console.

## Customization

You can adjust the parameters of the Z-score algorithm in `zscore_anomaly_detection.py`:

- **window_size**: The number of recent data points to consider (default: 100)
- **threshold**: The Z-score threshold for anomaly detection (default: 3)

Modify the data generation process in `data_stream_simulator.py` to simulate different types of data streams.

## How It Works

1. The `DataStreamSimulator` generates a continuous stream of data points, occasionally injecting anomalies.
2. The `ZScoreAnomalyDetector` processes each data point, calculating its Z-score based on recent data.
3. If a data point's Z-score exceeds the threshold, it's flagged as an anomaly.
4. The `Visualizer` plots the data stream in real-time, highlighting detected anomalies.

## Why Z-Score?

The Z-score method was chosen for its simplicity, efficiency, and ability to adapt to changing data patterns.

