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
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: latchaya priyan S
RegisterNumber:  212224230139
*/import numpy as np
import matplotlib.pyplot as plt

x=np.array(eval(input()))
y=np.array(eval(input()))

print("X-values:", x)
print("Y-values:", y)

# Mean of x and y
x_mean = np.mean(x)
y_mean = np.mean(y)

# Calculate slope (m) and intercept (b) using formulas
m = np.sum((x - x_mean) * (y - y_mean)) / np.sum((x - x_mean) ** 2)
b = y_mean - m * x_mean

print(f"Slope (m): {m:.4f}")
print(f"Intercept (b): {b:.4f}")

# Predicted y values
ypred = m * x + b
print("Predicted Y-values:", ypred)

# Plot actual and predicted values
plt.scatter(x, y, color='red', label="Actual values")
plt.plot(x, ypred, color='black', label="Regression line")
plt.xlabel("X")
plt.ylabel("Y")
plt.title("Linear Regression (Formula Based)")
plt.legend()
plt.show()

```

## Output:
<img width="692" height="753" alt="image" src="https://github.com/user-attachments/assets/1e432415-5db3-4105-8a54-5a97c15b53a1" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
