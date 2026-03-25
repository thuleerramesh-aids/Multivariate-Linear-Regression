# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
<br>

### Step2
<br>

### Step3
<br>

### Step4
<br>

### Step5
<br>

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

### Insert your output

<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
