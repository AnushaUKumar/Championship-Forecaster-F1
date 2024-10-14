# F1 Predictor: Formula 1 Race Position Prediction

This project leverages various machine learning models to predict Formula 1 race positions based on historical race data. The project includes model evaluations, hyperparameter tuning, and predictions for future races, identifying the best model for accurate prediction.

## Project Overview

The goal of this project is to predict the finishing position of Formula 1 drivers using historical race data from multiple seasons. The following tasks are performed in the project:

1. **Data Cleaning:**
   - Handles missing values such as '\N' by replacing them with NaN.
   - Converts relevant features to numeric format for model processing.
   
2. **Feature Selection:**
   - Removes irrelevant columns like driver names, circuit references, etc., focusing on numerical features like milliseconds, rank, and grid position.
   
3. **Model Building:**
   - Evaluates multiple regression models:
     - Linear Regression
     - Lasso Regression
     - Ridge Regression
     - Random Forest Regressor
     - Support Vector Regressor (SVR)
     - XGBoost Regressor

4. **Hyperparameter Tuning:**
   - Fine-tunes the hyperparameters of each model using GridSearchCV to find the optimal configuration.
   
5. **Model Evaluation:**
   - Compares the models using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R² Score to determine the best model.
   
6. **New Predictions:**
   - The best model is used to predict future race positions for Formula 1 drivers.

## Dataset

The dataset is a cleaned CSV file, `final_f1.csv`, which contains historical race data. Key features include:

- `raceId`: ID of the race.
- `driverId`: ID of the driver.
- `constructorId`: Constructor team ID.
- `grid`: The starting grid position of the driver.
- `milliseconds`: Time taken to finish the race.
- `rank`: Ranking based on specific criteria (like fastest laps).
- `position`: The final finishing position of the driver.

## Models Used

The following machine learning models are used to predict race positions:

- **Linear Regression**: A basic regression model.
- **Lasso Regression**: Linear model with L1 regularization to prevent overfitting.
- **Ridge Regression**: Linear model with L2 regularization.
- **Random Forest Regressor**: An ensemble model that uses multiple decision trees for prediction.
- **Support Vector Regressor (SVR)**: A regression model using support vector machines.
- **XGBoost Regressor**: An optimized gradient-boosting model, known for its speed and accuracy.

## Model Tuning

Each model is fine-tuned using `GridSearchCV` to optimize its performance.

## Race Prediction Results

The machine learning model successfully predicted the outcomes of the first race of the 2024 Formula 1 season. Below are the actual results compared with the model's predictions:

| Driver            | Actual Position | Predicted Position | Car                                      |
|-------------------|-----------------|--------------------|------------------------------------------|
| Max Verstappen     | 1               | 1                  | Red Bull Racing Honda RBPT               |
| Sergio Perez       | 2               | 2                  | Red Bull Racing Honda RBPT               |
| Charles Leclerc    | 3               | 3                  | Ferrari                                  |
| Oscar Piastri      | 4               | 4                  | McLaren Mercedes                         |
| Fernando Alonso    | 5               | -                  | Aston Martin Aramco Mercedes             |

As shown in the table, the predictions made for the first 2024 race match the actual positions for the top 4 drivers, indicating the accuracy of the model.


## How to Run
To replicate the predictions:
1. Clone this repository.
2. Install the necessary libraries by running:
   ```bash
   pip install -r requirements.txt
