# Flight-Price-Prediction

This project aims to predict the price of flights based on various features such as airline, journey date, source, destination, and travel duration. Using a dataset of flight information, we apply machine learning techniques to train a model capable of estimating flight prices accurately.

Problem Overview
The goal of this project is to build a predictive model that can forecast flight prices based on several input features. This model could be used by travel agencies, airlines, or individuals to estimate the cost of a flight based on various factors. The dataset used for this project is composed of multiple flight records with the following features:

Airline: Name of the airline operating the flight.

Date_of_Journey: Date when the flight is scheduled.

Source: The city from which the flight departs.

Destination: The city where the flight lands.

Route: The path taken by the flight with possible layovers.

Dep_Time: Departure time of the flight.

Arrival_Time: Arrival time at the destination.

Duration: The total time of the flight.

Total_Stops: Number of stops on the flight.

Additional_Info: Additional details about the flight (e.g., meals, baggage).

Price: The price of the flight ticket.

Approach
1. Data Preprocessing
The first step was to clean and preprocess the data:

We handled missing or incorrect data entries.

Converted time features like Duration into a numeric format (total minutes).

Extracted date features from Date_of_Journey, such as year, month, day, and day of the week.

2. Exploratory Data Analysis (EDA)
We performed a thorough analysis of the data to understand the distribution of key features, relationships between variables, and potential patterns that could influence flight prices:

We visualized the distribution of flight prices, airlines, and journey durations.

We also examined the Additional_Info column to understand different flight options like meals, layovers, and baggage inclusion.

3. Feature Engineering
We created new features from the Duration and Date_of_Journey columns to improve the model’s performance.

The Duration column was converted into total minutes.

The Date_of_Journey was split into individual components like year, month, day, and day_of_the_week.

4. Model Training
We used the following machine learning techniques:

XGBoost: A powerful gradient boosting algorithm used for regression tasks.

Hyperparameter tuning was done using GridSearchCV to find the best model parameters.

5. Model Evaluation
The model's performance was evaluated using:

RMSE (Root Mean Squared Error)

MSE (Mean Squared Error)

We also evaluated feature importance using the trained XGBoost model to identify the most influential features on the flight price prediction.

6. Saving the Model
The final trained model and the scaler were saved using joblib for later use, allowing deployment or further prediction tasks.
Flight_Price_Prediction.ipynb: The Jupyter notebook containing the analysis, model training, and evaluation.

Data_Train.xlsx: The dataset used for training the model.

best_xgb_model.joblib: The trained XGBoost model.

scaler.joblib: The scaler used to standardize data before model prediction.
