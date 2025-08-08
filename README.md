# Flight Price Predictor

## Overview

**Flight Price Predictor** is a machine learning-powered web application that estimates flight ticket prices based on several travel details such as airline, cities, departure time, class, number of stops, and days left to travel.

It is built using:

- Python
- Pandas
- Scikit-learn
- XGBoost
- Gradio

The app features a **user-friendly interface** so anyone can interact with the model and get price predictions instantly.

---

## Dataset Used

The dataset includes flight booking data with the following features:

- **Airline** (e.g., IndiGo, GO_FIRST)
- **Source City** (e.g., Chennai, Delhi)
- **Destination City** (e.g., Mumbai, Bangalore)
- **Departure Time** (Morning, Afternoon, Evening, Night)
- **Stops** (Non-stop, One, Two+)
- **Class** (Economy, Business)
- **Days Left** (Days remaining until departure)
- **Price** (Target variable — the actual ticket price)

---

## Features Used in the Model

The model is trained on the following features:

- `airline`
- `source_city`
- `destination_city`
- `departure_time`
- `stops`
- `class`
- `days_left`

These features are selected based on their strong influence on flight prices.

---

## How It Works

### 1. **Data Preprocessing**
- Cleaned and selected relevant columns
- Handled categorical features using **Label Encoding**
- Performed an 80/20 **Train-Test Split**

### 2. **Model Training**
- Trained a `RandomForestRegressor` model
- Saved the model as `price_model.pkl` and encoders as `price_encoders.pkl` using `joblib`

### 3. **Gradio Interface**
- Built a simple, interactive UI using **Gradio Blocks**
- Users enter inputs and get a predicted flight price

---

## Example Inputs and Output

| Airline  | Source City | Destination City | Departure Time | Stops    | Class    | Days Left | Predicted Price |
|----------|-------------|------------------|----------------|----------|----------|------------|-----------------|
| GO_FIRST | Chennai     | Bangalore        | Afternoon      | One      | Business | 10         | ₹5412.50        |
| IndiGo   | Delhi       | Mumbai           | Morning        | Non-stop | Economy  | 20         | ₹3125.00        |

---

## Tools and Libraries Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Gradio
- Joblib

---

## How to Run This Project

1. Open the notebook in **Google Colab**
2. Upload your dataset: `airlines_flights_data.csv`
3. Run the cells for:
    - Data preprocessing
    - Model training
    - Saving model and encoders
    - Launching the Gradio interface
4. Use the UI to interact with the model and get flight price predictions

---

## Use Cases

- **Travel Budget Planning**: Estimate ticket prices before booking
- **Airline Benchmarking**: Compare prices across airlines and routes
- **EdTech**: Demonstrates real-world regression modeling
- **App Integration**: Can be integrated into flight search tools or travel apps

---

## About

This project showcases how a machine learning model can be trained on real-world data and deployed using Gradio to create a practical and visually appealing app.

---


MIT License

