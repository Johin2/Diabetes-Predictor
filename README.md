# Diabetes-Predictor

The code begins by importing the necessary libraries such as scikit-learn (sklearn), pandas, plotly, numpy, and joblib. These libraries provide functions for data manipulation, model evaluation, visualization, and model persistence.

Next, it reads a diabetes prediction dataset from a CSV file into a pandas DataFrame, df. The dataset contains various features such as age, hypertension, heart disease, BMI, HbA1c level, blood glucose level, smoking history, and the target variable, diabetes.

To gain insights into the dataset, it creates a 3D scatter plot using plotly.express. The plot visualizes the relationship between gender, diabetes, and blood glucose level.

Further preprocessing steps involve one-hot encoding categorical variables using pandas' get_dummies function. It creates binary columns for each category, converting categorical variables into numerical form for model training.

To identify features with weak correlation to the target variable, it computes the correlation matrix and extracts features with an absolute correlation coefficient less than 0.1. These features are considered non-related and are subsequently dropped from the DataFrame.

The dataset is split into input features (X) and the target variable (y). The train_test_split function from sklearn.model_selection is used to split the data into training and testing sets.

A logistic regression model is initialized and trained using the training data. Cross-validation is performed to evaluate the model's accuracy, mean squared error, and recall using different scoring metrics.

The mean scores are computed and displayed on the console.

To demonstrate how the trained model can be used for prediction, a custom input is created, representing a hypothetical patient's characteristics. The trained model is then used to predict whether the patient has diabetes or not based on the input.

The model is saved to disk using joblib.dump, allowing it to be reused later without retraining.

The code also provides a graphical user interface (GUI) using the tkinter library. The GUI allows users to input their age, hypertension status, heart disease status, BMI, HbA1c level, and blood glucose level. When the "Predict" button is clicked, the model predicts whether the user is diabetic or not based on the provided inputs, and the result is displayed in a message box.

This code snippet demonstrates the process of building a logistic regression model for diabetes prediction, performing cross-validation for evaluation, and creating a user-friendly interface for making predictions. It showcases how machine learning techniques can be applied to healthcare data to assist in medical decision-making.

If you have any questions or need further clarification, please feel free to ask!
