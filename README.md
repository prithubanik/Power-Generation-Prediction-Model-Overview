# Power Generation Prediction Model

## Overview

This repository contains a machine learning and deep learning-based project aimed at predicting **generated power (kW)** using various weather and environmental features. The dataset includes several meteorological features such as temperature, humidity, wind speed, and cloud cover. The goal is to predict the generated power based on these features.

The repository includes:

- **Feature Engineering**: Data preprocessing, normalization, and feature selection
- **Model Training**: Training both traditional machine learning and deep learning models
- **Evaluation**: Model evaluation using various metrics (R², MAE, NMAE)
- **Visualizations**: Analysis of feature relationships through plots and graphs

## Features

The dataset includes the following features:

- `temperature_2_m_above_gnd`: Temperature at 2 meters above the ground (°C)
- `relative_humidity_2_m_above_gnd`: Humidity at 2 meters above the ground (%)
- `mean_sea_level_pressure_MSL`: Pressure at mean sea level (hPa)
- `total_precipitation_sfc`: Total precipitation at the surface (mm)
- `snowfall_amount_sfc`: Snowfall amount at the surface (mm)
- `total_cloud_cover_sfc`: Total cloud cover at the surface (%)
- `high_cloud_cover_high_cld_lay`: High-level cloud cover (%)
- `medium_cloud_cover_mid_cld_lay`: Medium-level cloud cover (%)
- `low_cloud_cover_low_cld_lay`: Low-level cloud cover (%)
- `shortwave_radiation_backwards_sfc`: Shortwave radiation at the surface (W/m²)
- `wind_direction_10_m_above_gnd`: Wind direction at 10 meters above the ground (°)
- `wind_speed_80_m_above_gnd`: Wind speed at 80 meters above the ground (m/s)
- `wind_direction_80_m_above_gnd`: Wind direction at 80 meters above the ground (°)
- `wind_speed_900_mb`: Wind speed at 900mb (m/s)
- `wind_direction_900_mb`: Wind direction at 900mb (°)
- `wind_gust_10_m_above_gnd`: Wind gust at 10 meters above the ground (m/s)
- `angle_of_incidence`: Angle of incidence of sunlight (°)
- `zenith`: Zenith angle (°)
- `azimuth`: Azimuth angle (°)
- `generated_power_kw`: **Target variable** representing generated power in kilowatts (kW)

## Prerequisites

### Libraries
The following libraries are required to run the code:

- `pandas`
- `numpy`
- `scikit-learn`
- `tensorflow`
- `matplotlib`
- `seaborn`
- `lightgbm`

To install the dependencies, you can use:

```bash
pip install -r requirements.txt
