# Seoul Bike Rental Prediction (Regression Project)

A practical Machine Learning project predicting public bike rental demand in Seoul using daily weather metrics. This project compares standard Multiple Linear Regression against a Deep Neural Network built with TensorFlow/Keras.

---

## What is Regression? (In Simple Terms)

In Machine Learning, Regression is used when you want to predict a continuous number rather than a category. 

- Classification answers questions like: "Is this email spam or not?" or "Will it rain today? (Yes / No)"
- Regression answers questions like: "What will the temperature be tomorrow?" or "How many bikes will be rented at 12:00 PM today?"

Because the output is an exact count (e.g., 450 bikes, 1,200 bikes), we use regression algorithms to draw mathematical trendlines through historical data points to estimate future demand.

---

## How the Bike Dataset is Used

We use the Seoul Bike Sharing Dataset (from the UCI Machine Learning Repository), which records hourly bike rentals alongside local weather conditions.

### 1. Data Cleaning & Focusing the Problem
- Filtering Peak Time: Instead of analyzing all 24 hours at once, we filter the dataset specifically for 12:00 PM (noon) to model peak midday rental demand.
- Feature Selection: We drop unnecessary columns (like date labels) and drop low-correlation features (`wind`, `visibility`, `functional`) to keep the model focused on the most important drivers: Temperature, Humidity, Dew Point, Solar Radiation, Rain, and Snow.

### 2. The Models We Built
1. Multiple Linear Regression (scikit-learn): Fits a straight baseline line through multi-dimensional weather data ($y = w_1x_1 + w_2x_2 + \dots + b$).
2. Deep Neural Network (TensorFlow/Keras): Uses hidden dense layers with `ReLU` activation functions. This allows the model to learn non-linear patterns—like how bike demand rises as it gets warmer, but drops off if it gets uncomfortably hot or starts raining heavily.

---

## What You Learn From This Project

1. How to Frame an ML Problem:
   - Narrowing down noisy datasets (focusing on 12 PM demand) makes models much more accurate than trying to predict everything at once.

2. Why Feature Scaling & Normalization Matter:
   - Temperature ranges from -20°C to 40°C, while Humidity ranges from 0% to 100%.
   - Neural networks struggle when inputs have wildly different numeric ranges. Using `tf.keras.layers.Normalization` standardizes all features so the model trains smoothly without gradient issues.

3. Baseline vs. Deep Learning:
   - Linear Regression gives a fast, interpretable starting point.
   - Neural Networks capture subtle curved relationships that straight lines miss, but require careful hyperparameter tuning (learning rates, epoch counts).

4. Model Evaluation & Diagnostics:
   - Mean Squared Error (MSE): Measuring how far off our predictions are on average (penalizing larger mistakes heavily).
   - True vs. Predicted Plots: Graphing true bike counts against predicted counts along an ideal $y = x$ diagonal line to visually inspect over-prediction or under-prediction patterns.

---

## Folder Structure

```text
seoul-bike-demand/
├── bikes_regression.ipynb     # Interactive Google Colab exploratory notebook
├── seoul_bike_regression.py   # Refactored, modular Python script
└── README.md                  # Project documentation
