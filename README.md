# Predictive Maintenance Case Study
### A case study using a random forest classification model to predict machine failures.

## Case Study Premise
### Challenge:
_Temperature readings, vibration levels, operational hours, and more. Your mission? To unravel the mysteries within this data and develop a machine learning model that can predict when a machine is on the brink of
failure. By doing so, you can help FutureTech transition from reactive repairs to proactive maintenance, ensuring the gears of Technopolis never stop turning._

### Objective:
Develop a machine learning model that can predict when a machine is on the brink of failure.

### Concepts Covered:
1. **Machine Learning Forms:** Supervised learning can be used to implement the functionality that determines the ‘failure status’ of the machines by training the models using variables such as ‘temp’, ‘vibration level’ and ‘operational hours’.
2. **Random Forest:** This classifier can be trained on the training set to make predictions on the test set.
3. **Evaluation Metrics:** Make use of classification reports and confusion matrices to assess the performance of the predictive maintenance model.

## Installation
predictive_maintenance.ipynb can be downloaded and run locally with Jupyter Notebook.

The following libraries will need to be installed before running:
- pandas
- scikit-learn
- matplotlib

The dataset used is available on Kaggle and can be downloaded here:

https://www.kaggle.com/datasets/shivamb/machine-predictive-maintenance-classification

>[!IMPORTANT]
>The dataset should be named 'predictive_maintenance.csv' and placed into the same folder as predictive_maintenance.ipynb before running.

## Use
This notebook reads the predictive_maintenance.csv file into a pandas dataframe, drops unneccessary columns and maps the 'Type' to integers for use in the predictive model.

The features used are:
- Type
- Air temperature [K]
- Process temperature [K]
- Rotational speed [rpm]
- Torque [Nm]
- Tool wear [min]

The target used is the 'Target' column, which indicates if there was a failure or not.
>[!IMPORTANT]
>The dataset contains two possible targets: 'Target' and 'Failure Type'. As Target is used, Failure Type is dropped in order to avoid leakage.

A train-test split of 80% is used to train and test a random forest classifier model.

The model is then evaluated by returning the accuracy, a classification report and a confusion matrix.

## Credits
predictive_maintenance.ipynb was written by E. Thompson

The predictive maintenance dataset from Kaggle, found [here](https://www.kaggle.com/datasets/shivamb/machine-predictive-maintenance-classification) originates from [UCI](https://archive.ics.uci.edu/ml/datasets/AI4I+2020+Predictive+Maintenance+Dataset)
