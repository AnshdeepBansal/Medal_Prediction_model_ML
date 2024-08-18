# Medal_Prediction_model_ML
## Overview

This project is a simple machine learning model aimed at predicting the number of medals that a team will win based on various factors such as the number of athletes, previous medals won, and the average age of the team. The dataset used in this project consists of historical data on Olympic teams.

## Dataset

The dataset used in this project is stored in a CSV file named `teams.csv`. It contains the following columns:

- `team`: The name of the team.
- `country`: The country the team represents.
- `year`: The year of the Olympic games.
- `athletes`: The number of athletes in the team.
- `age`: The average age of the team members.
- `prev_medals`: The number of medals the team won in previous Olympics.
- `medals`: The number of medals the team won in the current Olympics.

## Project Structure

The project is structured into several key steps:

1. **Data Loading and Cleaning:**
    - The dataset is loaded using Pandas.
    - Columns relevant to the analysis are selected.
    - The dataset is checked for missing values, and any rows with missing data are removed.

2. **Exploratory Data Analysis (EDA):**
    - The correlations between the number of medals and other variables are calculated.
    - Seaborn is used to create regression plots for visualizing relationships between `athletes`, `prev_medals`, `age`, and `medals`.
    - A histogram is plotted to visualize the distribution of medals.

3. **Data Splitting:**
    - The data is split into a training set (data before 2012) and a test set (data from 2012 onwards).

4. **Model Training:**
    - A Linear Regression model from scikit-learn is used.
    - The model is trained using the `athletes` and `prev_medals` columns as predictors.

5. **Model Prediction:**
    - Predictions are made on the test data.
    - Negative predictions are set to zero and rounded to the nearest whole number.

6. **Error Analysis:**
    - The mean absolute error between the predicted and actual medal counts is calculated.
    - Errors are further analyzed by team, and the error ratio (error by team divided by average medals by team) is computed and visualized.

7. **Further Improvements:**
    - The project suggests adding more predictors and trying different models like Random Forest to improve the prediction accuracy.

## Requirements

To run this project, you need to have the following Python libraries installed:

- pandas
- seaborn
- scikit-learn
- numpy

## Usage

1. Clone the repository or download the notebook file.
2. Ensure the `teams.csv` file is in the same directory as the notebook.
3. Run the notebook cell by cell to load the data, train the model, and make predictions.
4. Review the error analysis to understand the model's performance.

## Future Work

- **Add more predictors**: Explore additional features that might improve the prediction accuracy.
- **Try different models**: Implement other machine learning models like Random Forest or Gradient Boosting to compare performance.

## Conclusion

This project serves as an introductory exploration into using linear regression for predicting outcomes based on historical data. It also provides a foundation for further experimentation with more complex models and features.
