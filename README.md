# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
register no: 212225230061
Developed by : R Dinesh karthick
```
import numpy as np
import matplotlib.pyplot as plt

# Preprocessing input data
X = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
Y = np.array([1, 3, 2, 5, 7, 8, 8, 9, 10, 12])

# Scatter plot of input data
plt.scatter(X, Y)
plt.show()
```
```
# Building the model
X_mean = np.mean(X)
Y_mean = np.mean(Y)

num = 0
den = 0

for i in range(len(X)):
    num += (X[i] - X_mean) * (Y[i] - Y_mean)
    den += (X[i] - X_mean) ** 2

m = num / den          # slope
c = Y_mean - m * X_mean  # intercept

print(m, c)
```
```
# Making predictions
Y_pred = m * X + c
print(Y_pred)

# Plotting regression line
plt.scatter(X, Y)
plt.scatter(X, Y_pred, color='red')
plt.plot([min(X), max(X)], [min(Y_pred), max(Y_pred)], color='red')
plt.show()
```


## Output
<img width="974" height="773" alt="Screenshot 2026-02-14 084155" src="https://github.com/user-attachments/assets/32e97362-4e0e-4fba-a3e7-318227161d3a" />

<img width="513" height="380" alt="Screenshot 2026-02-14 084225" src="https://github.com/user-attachments/assets/ca21d8d8-79f2-48cb-aca3-8ab00ac9d1de" />

<img width="816" height="768" alt="Screenshot 2026-02-14 084246" src="https://github.com/user-attachments/assets/f54f3a02-5b83-4ab3-8a9a-160696175a39" />




## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
