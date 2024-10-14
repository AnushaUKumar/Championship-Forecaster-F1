# Formula 1 Race Predictions 2024

## Project Overview
This project utilizes various machine learning models (Linear Regression, Lasso, Ridge, Random Forest, XGBoost, and SVR) to predict Formula 1 race results. The predictions were made for the first race of the 2024 season, and the results were compared with the actual race data.

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

## Models Used
- **Linear Regression**
- **Lasso Regression**
- **Ridge Regression**
- **Random Forest Regressor**
- **XGBoost Regressor**
- **Support Vector Regressor (SVR)**

## Fine-Tuning and Hyperparameter Optimization
Each model was fine-tuned to optimize the performance by adjusting hyperparameters like the regularization strength in Lasso and Ridge, the number of estimators in Random Forest, and the learning rate in XGBoost. Grid search was used for hyperparameter tuning to obtain the best possible accuracy.

## Technologies Used
- Python
- Scikit-learn
- XGBoost
- Matplotlib
- Pandas
- NumPy

## How to Run
To replicate the predictions:
1. Clone this repository.
2. Install the necessary libraries by running:
   ```bash
   pip install -r requirements.txt
