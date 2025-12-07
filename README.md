# Air Pollution Forecasting Using LSTM

## Description
This project implements an **LSTM (Long Short-Term Memory)** model to predict air pollution levels (PM2.5 concentration) for the next hour using current weather conditions and pollution data. The model has been trained using both:

- **Uni-variate approach:** Using only one feature for prediction
- **Multi-variate approach:** Using multiple features for prediction

---

## Dataset
The project uses the **Air Quality dataset** collected at the US Embassy in Beijing, China, which reports hourly weather and pollution levels over five years. The dataset includes:

- Date-time
- PM2.5 concentration (pollution level)
- Weather parameters: Dew point, temperature, pressure, wind direction, wind speed
- Cumulative hours of snow and rain

---

## Tech Stack
- **Language:** Python  
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn  
- **Deep Learning Framework:** TensorFlow/Keras (for LSTM)

---

## Project Steps

### 1. Data Preparation
- Replace missing (NA) values  
- Parse date-time into pandas DataFrame index  
- Specify clear column names  

### 2. Data Visualization
- Create boxplots for feature distribution  
- Plot correlation matrix to understand relationships  

### 3. LSTM Data Preparation
- Normalize data  
- Transform dataset into a supervised learning problem (creating input-output pairs)  

### 4. Model Fitting
- Split data into training and testing sets  
- Split into input (X) and output (y)  
- Reshape data into 3D format for LSTM  
- Define 3-layer LSTM architecture with 50 neurons per layer and 1-neuron output layer  
- Add 20% dropout after each layer for regularization  

### 5. Model Evaluation
- Make predictions on test data  
- Invert scaling to get original PM2.5 values  
- Plot actual vs predicted PM2.5 values  
- Calculate **RMSE (Root Mean Squared Error)** and **MAPE (Mean Absolute Percentage Error)**  

---

## Results
- Line graph showing predicted vs actual PM2.5 values  
- Performance metrics: RMSE, MAPE  

---

## Future Work

- Include additional weather features or external pollution factors
- Deploy the model for real-time air quality prediction
- Compare with other time-series forecasting models like GRU, ARIMA, XGBoost

