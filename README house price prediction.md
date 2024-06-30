House Price Prediction

## 1. Project Overview
This project aims to develop a predictive model for house prices using various data science and machine learning techniques. The primary goal is to accurately forecast house prices based on a range of features such as location, size, and amenities.

## 2. Installation Guidelines

1. **Clone the repository**
git clone https://github.com/LittleBoy-r/KT24602-Group-Project.git

2. **Navigate to the project directory**
cd house-price-prediction

3. **Install the required dependencies**
pip install **name of library**

**pandas** : For data manipulation and analysis.
**numpy** : For numerical operations.
**scikit-learn (sklearn)** : For machine learning tasks, including preprocessing, model building, and evaluation.
**matplotlib** : For plotting graphs.
**unittest** : For writing and running tests.

## 3. Usage Guidelines

1. **Prepare the dataset and place it in the appropriate directory**

2. **Run the data preprocessing script**
python preprocess.py

3. **Train the model**
python train.py

4. **Make predictions**
python predict.py --input data/input.csv --output data/output.csv

## 4. Contributions
We welcome contributions from the community! To contribute: 

1. **Fork the repository**

2. **Create a new branch**
git checkout -b feature-name

3. **Make your changes and commit them**
git commit -m "Add new feature"

4. **Push to the branch**
git push origin feature-name

5. **Open a pull request**

## 5. Functionality 
The house price prediction system aims to predict real estate prices based on various features such as location, size, number of rooms, and other relevant factors. Key functionalities include:

**Data Ingestion** : Importing and cleaning data from various sources.
**Feature Engineering**: Transforming raw data into meaningful features for the model.
**Model Training**: Using machine learning algorithms to train the predictive model.
**Prediction**: Providing house price estimates based on input features.
**User Interface**: Offering an easy-to-use interface for users to input data and view predictions.

## 6. Future Enhancement
Potential future enhancements for the project include:

**Enhanced Model Accuracy**: Continuously improving the model by incorporating more advanced algorithms and additional data sources.
**User Interface Improvements**: Making the user interface more intuitive and adding new features for better user experience.

## 7. Unit Testing and Integration
Unit testing involves verifying individual components or functions of a program to ensure they work as expected. Here, we define two main sets of unit tests: one for data cleaning and one for the machine learning pipeline.

**Example of Data Cleaning Unit Tests**
**test_extract_numerical_price**: Verifies that the 'price' column is correctly transformed into numerical values.
**test_replace_parking_lot**: Ensures that '-' values in the 'Parking Lot' column are replaced with 0 and converted to integers.
**test_remove_invalid_bed_bath**: Checks that rows with invalid 'Bedroom' and 'Bathroom' values ('-') are removed.

Each test performs specific assertions to verify the correctness of the corresponding data cleaning steps.

**Machine Learning Pipeline Tests**
**test_pipeline_predict**: This integration test ensures that the pipeline can be fitted to the training data and can predict the target variable for the test data.

Verifies the shape of the predicted values matches the shape of the actual target values.
Ensures the prediction output is a numpy array.
Optionally, checks if the predicted values are within a reasonable range (greater than 0).

## 8. Model Accuracy
After training the model, the accuracy of the predictions is evaluated using the following metrics:

**Mean Absolute Error (MAE)**: Measures the average magnitude of errors in the predictions, without considering their direction. It provides a straightforward measure of prediction accuracy:

mae = mean_absolute_error(actual_value, predicted_value)
r2 = r2_score(actual_value, predicted_value)
print('Mean Absolute Error: ', round(mae, 2))
print('R2 Score: ', round(r2, 5))

The **mean_absolute_error** function calculates the MAE, and the r2_score function calculates the R2 score for the model predictions. The lower the MAE and the higher the R2 score, the better the model's performance.

