# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

step 1: Start

step 2: Get the independent variable X and dependent variable Y.

step 3: Calculate the mean of the X -values and the mean of the Y -values.

step 4: Find the slope m of the line of best fit using the formula.

<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">

step 5: Compute the y -intercept of the line by using the formula:

<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">

step 6: Use the slope m and the y -intercept to form the equation of the line.

step 7: Obtain the straight line equation Y=mX+b and plot the scatterplot.

step 8: Stop

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Baskar.U
RegisterNumber: 212223220013
*/
```
```py
import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
X_mean=np.mean(X)
print(X_mean)
Y_mean=np.mean(Y)
print(Y_mean)
num=0
denum=0
for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denum+=(X[i]-X_mean)**2
m=num/denum
print(m)
b=Y_mean - m*X_mean
print(b)
Y_pred=m*X+b
print(Y_pred)
plt.scatter(X,Y,color='blue')
plt.plot(X,Y_pred,color='yellow') 
plt.show() 

```

## Output:

```
x:           6,10,2,3,4,5
y:           81,23,40,64,54,43
(m,b):       -2.650000000000001 64.08333333333334
y_predicted: [48.18333333 37.58333333 58.78333333 56.13333333 53.48333333 50.83333333]
```

![image](https://github.com/user-attachments/assets/d91839cc-0ce9-41c3-9161-2c1c264da6b6)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
