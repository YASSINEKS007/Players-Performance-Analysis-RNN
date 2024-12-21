# Sports Performance Analysis Using Player Tracking Data and RNN Networks

This project analyzes the performance of Premier League players by utilizing historical match data and applying Recurrent Neural Networks (RNNs) to predict their performance. The goal is to forecast a player's performance in an upcoming match based on their past performances, specifically focusing on metrics like goals scored, assists, and other relevant statistics.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Project Setup](#project-setup)
3. [Data Collection](#data-collection)
4. [Data Preparation](#data-preparation)
5. [Model Development](#model-development)
6. [Evaluation](#evaluation)
7. [Conclusion](#conclusion)

---

## Introduction

This project involves web scraping to gather historical match data for Premier League players. The collected data is then cleaned and transformed into a suitable format for machine learning. A Recurrent Neural Network (RNN) model is trained on the historical data to predict the number of goals a player will score in the next match based on their performance over the last nine games.

---

## Project Setup

To run this project, make sure you have the following dependencies installed:

- Python 3.x
- TensorFlow
- scikit-learn
- pandas
- numpy
- BeautifulSoup4
- requests
- matplotlib
- tabulate

## Data Collection

### Web Scraping

The data collection process involves scraping match data from the Premier League statistics page. The following steps were followed:

1. **Get Match Links**: All match links for the 2018-2019 season were scraped using BeautifulSoup.
2. **Scrape Player Data**: For each match, player statistics such as goals scored, assists, tackles, and more were scraped.
3. **Data Storage**: The scraped data was saved into a CSV file for further processing.

## Data Preparation

### Data Cleaning and Transformation

1. **Data Loading**: The collected CSV file containing player statistics is loaded into a pandas DataFrame.
2. **Data Preprocessing**: Missing values, outliers, and erroneous data points were handled and removed.
3. **Feature Engineering**: New features were created based on player performance in previous matches, such as the number of goals, assists, and other relevant statistics.
4. **Normalization**: The data was normalized to ensure consistency across all features before feeding it into the model.

---

## Model Development

### RNN Model

An RNN was developed to predict player performance in future matches. The process for model development includes the following steps:

1. **Data Splitting**: The data was split into training and testing sets.
2. **Model Architecture**: The RNN model was designed with the following layers:
   - **LSTM Layers**: To capture temporal dependencies in player performance over time.
   - **Dense Layers**: To provide the final output prediction.
3. **Model Training**: The model was trained on the historical performance data using a supervised learning approach.
4. **Hyperparameter Tuning**: The model’s hyperparameters such as learning rate, batch size, and number of epochs were tuned to achieve optimal performance.

## Evaluation

The model's performance was evaluated using the following metrics:

1. **Mean Squared Error (MSE)**: Measures the average squared difference between the predicted and actual player performances.
2. **Mean Absolute Error (MAE)**: Measures the average magnitude of errors in the predictions, without considering their direction.
3. **Visual Evaluation**: The predicted vs actual player performance were plotted for visual assessment.

