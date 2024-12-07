# Power-Generation-Prediction-Model-Overview


Overview
This repository contains a machine learning and deep learning-based project to predict generated power (kW) using weather and environmental features. The dataset includes various meteorological features such as temperature, humidity, wind speed, and cloud cover, and the goal is to predict the power generated based on these factors.

The project includes:

Feature engineering and data preprocessing
Model training using traditional machine learning algorithms (Random Forest, Gradient Boosting, Linear Regression, etc.)
Deep learning models (LSTM, Bidirectional LSTM, etc.)
Visualizations to analyze relationships between features and target variable
Model evaluation using different metrics (e.g., R², MAE, NMAE)
Features
The dataset includes the following features:

temperature_2_m_above_gnd: Temperature at 2 meters above the ground (°C)
relative_humidity_2_m_above_gnd: Humidity at 2 meters above the ground (%)
mean_sea_level_pressure_MSL: Pressure at mean sea level (hPa)
total_precipitation_sfc: Total precipitation at the surface (mm)
snowfall_amount_sfc: Snowfall amount at the surface (mm)
total_cloud_cover_sfc: Total cloud cover at the surface (%)
high_cloud_cover_high_cld_lay: High-level cloud cover (%)
medium_cloud_cover_mid_cld_lay: Medium-level cloud cover (%)
low_cloud_cover_low_cld_lay: Low-level cloud cover (%)
shortwave_radiation_backwards_sfc: Shortwave radiation at the surface (W/m²)
wind_direction_10_m_above_gnd: Wind direction at 10 meters above the ground (°)
wind_speed_80_m_above_gnd: Wind speed at 80 meters above the ground (m/s)
wind_direction_80_m_above_gnd: Wind direction at 80 meters above the ground (°)
wind_speed_900_mb: Wind speed at 900mb (m/s)
wind_direction_900_mb: Wind direction at 900mb (°)
wind_gust_10_m_above_gnd: Wind gust at 10 meters above the ground (m/s)
angle_of_incidence: Angle of incidence of sunlight (°)
zenith: Zenith angle (°)
azimuth: Azimuth angle (°)
generated_power_kw: Target variable representing generated power in kilowatts (kW)
Prerequisites
The following libraries are required to run the code:

pandas
numpy
sklearn
tensorflow
matplotlib
seaborn
lightgbm
You can install the dependencies using the following command:

bash
Copy code
pip install -r requirements.txt
Alternatively, you can install the libraries individually:

bash
Copy code
pip install pandas numpy scikit-learn tensorflow matplotlib seaborn lightgbm
Dataset
The dataset is assumed to be in CSV format and should include the features listed above. Ensure that your dataset file is named data.csv or modify the code accordingly to load the dataset from the correct file path.

Code Structure
data_preprocessing.py: Handles data loading, normalization, and splitting into train and test sets.
models.py: Defines and trains multiple models (Random Forest, Gradient Boosting, Linear Regression, Lasso, etc.).
lstm_model.py: Contains the LSTM, Bidirectional LSTM, and Stacked LSTM models for time-series prediction.
visualizations.py: Generates plots to explore the relationships between features and the target variable.
main.py: The entry point for executing the script and running the models.
Usage
Data Preprocessing: Before training, make sure to load the dataset into the variable data. The code assumes the dataset is stored in a variable data.

Training the Models: The script trains both traditional machine learning models and deep learning models on the dataset. Run the following command to train the models:

bash
Copy code
python main.py
Evaluate the Models: After training the models, you can evaluate their performance using the Mean Absolute Error (MAE) and Normalized MAE (NMAE), along with the R² Score for LightGBM and other models.

Visualizations: The code generates multiple plots to visualize data distributions and relationships, including:

Histograms of features
Boxplots for feature distributions
Correlation matrix heatmap
Scatter plots for the target vs. features
Pairwise relationships using pairplots
Time series plots (if temporal data is available)
You can tweak the visualizations to explore different aspects of the data.

Example Output
When you run the code, you will get the following outputs:

Model Evaluation: The performance of the models will be printed, showing metrics like R² score, MAE, and NMAE.
Plots: Various plots will be displayed showing feature distributions, correlations, and relationships between the features and the target variable.
Training History: For LSTM models, the training and validation loss will be plotted for each epoch.
Example:
Here is an example of using a traditional machine learning model and a deep learning model:

Traditional Model: Random Forest Regressor
bash
Copy code
Model: Random Forest
Regression Accuracy (%) = 91.12%
Deep Learning Model: Bidirectional LSTM
bash
Copy code
Model: Bidirectional LSTM
Regression Accuracy (%) = 89.45%
Troubleshooting
Out of Memory: If you encounter memory issues when training deep learning models, try reducing the batch size or the number of units in the LSTM layers.
Missing Values: Ensure there are no missing values in the dataset. You can handle missing values by using data.fillna() or data.dropna().
Model Convergence: If the deep learning model is not converging, you may need to adjust the learning rate or add dropout layers to avoid overfitting.
Contributing
If you'd like to contribute to the project, feel free to fork the repository and submit a pull request. Please ensure that your changes follow the coding standards used in the project and provide proper documentation.
