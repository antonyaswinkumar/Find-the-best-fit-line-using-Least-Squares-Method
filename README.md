# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 

<img width="557" height="208" alt="Screenshot 2026-05-14 093408" src="https://github.com/user-attachments/assets/fa4a90b5-0c8e-4c72-bd9c-823416df7b25" />

4. Compute the y -intercept of the line by using the formula:

<img width="491" height="197" alt="Screenshot 2026-05-14 093514" src="https://github.com/user-attachments/assets/e01e0e84-a2d3-44c1-8bfa-cd2bef702721" />

6. Use the slope m and the y -intercept to form the equation of the line.
7. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
## Program to implement univariate Linear Regression to fit a straight line using least squares.
## Developed by: ANTONY ASWIN KUMAR L
## RegisterNumber:  212225040024

import numpy as np
import matplotlib.pyplot as plt

#getting input from user
x = np.array(eval(input("Enter the independent variable (x): ")))  
y = np.array(eval(input("Enter the dependent variable (y): ")))    

# Number of observations
n = len(x)

# Calculate slope (m) and intercept (c)
m = (n * np.sum(x * y) - np.sum(x) * np.sum(y)) / (n * np.sum(x ** 2) - (np.sum(x)) ** 2)
c = (np.sum(y) - m * np.sum(x)) / n

print(f"Slope, m: {m}")
print(f"Intercept, c: {c}")

# Predict y values
y_pred = m * x + c
print(f"The predicted values are: {y_pred}")

# Plot the data points and regression line
plt.scatter(x, y, color='blue', label='Actual data')
plt.plot(x, y_pred, color='red', label='Fitted line')
plt.xlabel('X')
plt.ylabel('Y')
plt.title('Univariate Linear Regression using Least Squares')
plt.legend()
plt.show()

```

## Output:


<img width="920" height="707" alt="Screenshot 2026-05-14 093913" src="https://github.com/user-attachments/assets/ab4e8061-5f0a-49e0-81e9-57561ccb2f35" />


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming is executed successfully.
