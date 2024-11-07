# HEMS-Illuminate
---

# Home Energy Management System (HEMS)

## Overview

The **Home Energy Management System (HEMS)** is a system designed to optimize residential energy consumption by integrating solar energy, grid tariff forecasting, and battery storage management. The goal is to minimize energy costs, reduce grid dependency, and maximize the use of renewable solar energy within a smart home environment.

This system uses machine learning models and optimization algorithms to predict energy consumption, solar generation, and tariff rates, and dynamically schedules appliance usage to reduce overall electricity costs.

- **Backend**: [HEMS Backend](https://github.com/MelvinYG/Illuminate-Backend)
- **Frontend**: [HEMS Frontend](https://github.com/MelvinYG/Illuminate)
- **ML and Optimization Models**: [HEMS ML & Optimization](https://github.com/mysteman/Illuminate-ML-Optimization-models)

## Features

- **Energy Optimization**: Smart scheduling of household appliances like Dishwasher, Pump, and Washing Machine based on time-of-use (ToU) tariffs and solar generation forecasts.
- **Battery Management**: Optimizes battery charging and discharging cycles to minimize grid usage and ensure adequate backup energy during peak hours.
- **Solar and Tariff Forecasting**: Uses machine learning to predict solar energy production and grid tariff rates, allowing for dynamic energy consumption decisions.
- **Real-time Data Visualization**: Provides users with real-time insights into solar generation, energy consumption, and cost savings via a web-based dashboard.
- **Cost Savings**: Achieved up to 30% reduction in energy costs by optimizing appliance usage and battery storage based on real-time data.

## Technologies

- **Languages**: Python (for backend logic, machine learning models), JavaScript (React JS for frontend)
- **Libraries/Frameworks**: 
  - **Python**: Pandas, NumPy, PuLP, TensorFlow, Plotly
  - **JavaScript**: React JS, Axios
- **Database**: None (Uses real-time data input for forecasting and optimization)
- **Tools**: Jupyter (for development), Git (for version control)

## How It Works

The system works by optimizing the energy usage of various devices in a home based on the following inputs:

1. **Solar Generation Forecast**: A 24-hour prediction of solar energy production based on weather data.
2. **Grid Tariff Forecast**: A 24-hour forecast of the electricity tariff rates from the grid.
3. **Battery Storage**: A storage system with a limited capacity used for storing excess solar energy.
4. **Device Energy Consumption**: The wattage requirements and runtime schedules for household devices such as a dishwasher, washing machine, and pump.

The system uses the following steps to optimize energy usage:

1. **Forecasting**: Predicts solar generation and grid tariff rates.
2. **Optimization**: Uses **Mixed Integer Linear Programming (MILP)** and **Machine Learning (LSTM, Random Forest)** models to optimize device usage, battery charging, and discharging cycles.
3. **Scheduling**: Schedules device operations during off-peak hours and ensures optimal use of solar energy.
4. **Visualization**: Provides real-time insights into energy consumption, solar utilization, and cost savings via a web-based interface.

## Optimization Models

- **Machine Learning Models**: 
  - **LSTM (Long Short-Term Memory)**: Predicts solar generation and energy consumption patterns over time.
  - **Random Forest**: Predicts grid tariff rates based on historical data.
  
- **Optimization Model**: 
  - **Mixed Integer Linear Programming (MILP)**: Used to decide on the optimal charging and discharging of the battery and the scheduling of appliances based on dynamic tariff rates.

## Usage

1. **Monitor Energy Usage**: View real-time data about energy consumption, solar generation, and battery state-of-charge.
2. **Optimize Energy Consumption**: The system will automatically adjust the appliance runtime and battery charging/discharging based on forecasted data.
3. **View Savings**: The dashboard provides insights on energy cost savings from solar utilization and optimized grid usage.

## Example Results

| Hour | Grid Power (kW) | Charging Rate (kW) | Discharging Rate (kW) | Battery SOC (%) |
|------|-----------------|---------------------|------------------------|-----------------|
| 0    | 0.0             | 1.0                 | 0.0                    | 151.0           |
| 1    | 0.0             | 1.0                 | 0.0                    | 152.0           |
| 2    | 0.0             | 1.0                 | 0.0                    | 153.0           |
| 3    | 0.0             | 1.0                 | 0.0                    | 154.0           |

**Total Grid Cost**: $0.00  
**Peak Power Used from Grid**: 0.0 kW  
**Total Solar Utilization**: 18%

---
