# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
Step 1: Import NumPy and define input data arrays (Weight, Volume, CO₂).

Step 2: Form the feature matrix 
𝑋
X by combining Weight and Volume, and add a column of ones for the intercept.

Step 3: Compute regression coefficients using the normal equation

`(X^T X)^(-1) X^T Y`


Step 4: Predict CO₂ for new input values and print coefficients, intercept, and predicted value.

## Program:
```
import numpy as np

# Example data
Weight = np.array([790, 1160, 929, 865, 1140])
Volume = np.array([1000, 1200, 900, 1100, 1300])
CO2 = np.array([99, 95, 90, 97, 96])

# Simple linear regression using least squares (basic idea)
X = np.column_stack((Weight, Volume))
X = np.c_[np.ones(X.shape[0]), X]  # add intercept

# Compute coefficients using normal equation
beta = np.linalg.inv(X.T @ X) @ X.T @ CO2

print("Coefficients:", beta[1:])
print("Intercept:", beta[0])

# Prediction
new = np.array([1, 3300, 1300])
pred = new @ beta

print("Predicted CO2:", pred)






```
## Output:
<img width="999" height="634" alt="image" src="https://github.com/user-attachments/assets/2107cdb1-9433-4780-969b-602348fe58d9" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
