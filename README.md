# Student Performance Prediction

This project demonstrates how to use machine learning to predict student performance using data from a student performance dataset. The code preprocesses the data, trains a linear regression model, and evaluates its accuracy.

## Dataset

The dataset used in this script is available for download from the UCI Machine Learning Repository.. The specific dataset is student-mat.csv and contains information about students and their academic performance.

## Data Preprocessing

The data preprocessing steps in this project include:

- **Loading Data**: The data is loaded from a CSV file named `student-mat.csv` using the pandas library. The data is read with a semicolon (`;`) as the separator.

- **Selecting Columns**: The data is filtered to only include the columns relevant to the model: `'absences'`, `'Medu'`, `'G2'`, `'G3'`, and `'sex'`.

- **Mapping Categorical Data**: The `sex` column contains categorical data with values `'F'` for female and `'M'` for male. The code converts this categorical data to numerical data (`0` for female and `1` for male) by creating a new column `n_sex`.

- **Defining Features and Target**: The features (`X`) are defined as all columns in the DataFrame except for the target (`G3`) and the original `sex` column. The target (`y`) is defined as the `G3` column, which represents the students' final grades.

- **Splitting Data**: The data is split into training and testing sets using the `train_test_split` function from scikit-learn. The test set size is set to 10% of the total data, and the random seed is set for reproducibility.

## Model Training and Evaluation

The code trains a linear regression model using the training data and evaluates its accuracy using the testing data. The model's accuracy is printed as the output.

## Dependencies

The following Python libraries are required to run the code:

- `numpy`
- `pandas`
- `matplotlib`
- `scikit-learn`
- `joblib` (used for saving the model)

  ## Conclusion

The script demonstrates how to preprocess data and train a linear regression model to predict student performance. The final model's accuracy is provided as feedback for the model's performance. Further improvements can be made through advanced feature engineering, model tuning, and using more complex models for higher accuracy.
