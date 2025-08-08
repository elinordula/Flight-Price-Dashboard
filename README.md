# Flight-Price-Dashboard

Flight Price Predictor
Overview
Flight Price Predictor is a machine learning-based web application that predicts the price of a flight ticket based on various user inputs such as airline, source city, destination, travel class, stops, and the number of days left until departure.

The application is built using Python libraries including Pandas, Scikit-learn, and XGBoost, and features a user-friendly interface developed with Gradio. This allows users to get predictions without writing any code.

Dataset Used
The dataset includes flight booking data with the following columns:

Airline (e.g., IndiGo, GO_FIRST)

Source City (e.g., Chennai, Delhi)

Destination City (e.g., Mumbai, Bangalore)

Departure Time (Morning, Afternoon, Evening, Night)

Stops (Non-stop, One, Two+)

Class (Economy, Business)

Days Left (Days remaining until departure)

Price (Target variable — the actual ticket price)

Features Used for Prediction
The model uses the following input features:

airline

source_city

destination_city

departure_time

stops

class

days_left

These features are chosen based on their relevance and availability at the time of booking.

How It Works
1. Data Preprocessing
Cleaned the data and selected relevant columns

Handled categorical variables using Label Encoding

Split the data into training and testing sets (80/20 split)

2. Model Training
Trained a RandomForestRegressor model

Performed evaluation on test data

Saved the model (price_model.pkl) and encoders (price_encoders.pkl) using joblib

3. Gradio Interface
Developed an interactive web interface using Gradio Blocks

Inputs are taken via dropdowns and sliders

Prediction is displayed as the estimated ticket price

Example Inputs and Outputs
Airline	Source City	Destination City	Departure Time	Stops	Class	Days Left	Predicted Price
GO_FIRST	Chennai	Bangalore	Afternoon	One	Business	10	₹5412.50
IndiGo	Delhi	Mumbai	Morning	Non-stop	Economy	20	₹3125.00

Tools and Libraries Used
Python

Pandas

Scikit-learn

XGBoost

Gradio

Joblib

How to Run the Project
Open the notebook in Google Colab.

Upload the dataset (airlines_flights_data.csv).

Run the cells for:

Data preprocessing

Model training

Saving the model and encoders

Gradio app interface

Launch the Gradio app to predict flight prices interactively.

Use Cases
Personal travel cost estimation

Airline fare benchmarking

Integration into travel booking apps

Educational demonstration of regression models

About
This project demonstrates how machine learning regression models can be applied to real-world pricing problems with a clean UI for practical use.

