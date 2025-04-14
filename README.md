# aviationcarbonemissionsandcreditsproj
Aviation Carbon Emissions Forecasting and Carbon Credit Trading is a data science project that combines real-time flight and weather data with deep learning and reinforcement learning models. The aim is to support sustainable aviation by automating emissions monitoring and trading decisions.

It simulates an intelligent trading environment where an agent can buy, sell, or hold carbon credits based on real-time emissions data and market dynamics.

# Objectives

- Predict flight emissions using LSTM, GRU, ConvLSTM, and DNN models.
- Develop a custom reinforcement learning environment to simulate carbon credit trading.
- Train PPO, A2C, and SAC agents to learn optimal trading strategies that balance profit and emissions.
- Visualize trading outcomes and model performance.


# Project Flow
1. Data Collection
- Flight Data: Collected using the OpenSky API (includes altitude, velocity, callsign, etc.)
- Weather Data: Collected using the OpenWeatherMap API (temperature, humidity, wind speed)
- Distance & Nearest Airport Calculation: Derived using geolocation and Haversine formula

2. Emissions & Carbon Credit Calculation
- Used domain-specific formulas to compute:
- Fuel Burn Rate
- Fuel Burn (kg)
- CO₂ Emissions (kg)
- Credits Needed
- Credit Cost (USD)

These calculations form the final historical dataset.

3. Emissions Prediction Models
Built multiple models to predict emissions_kg based on flight and weather data:

- LSTM
- GRU
- ConvLSTM
- Deep Neural Network (DNN)

Models were evaluated using: RMSE (Root Mean Squared Error) and R² Score (Coefficient of Determination)

4. Carbon Credit Trading Simulation
- Designed a custom reinforcement learning environment using OpenAI Gym
- Defined actions: Buy, Hold, Sell carbon credits
- Defined reward: Combination of profit and emissions penalty

5. Reinforcement Learning Models
Trained 3 RL agents on the environment:
- PPO (Proximal Policy Optimization)
- A2C (Advantage Actor Critic)
- SAC (Soft Actor Critic)

Evaluated models based on:
- Final balance
- Total emissions
- Reward trends

This framework shows promise for real-time carbon credit optimization in aviation

