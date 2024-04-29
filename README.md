# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
Step 1:Start the program
Step 2: Get the independent variable X and dependent variable Y.
Step 3:Calculate the mean of the X -values and the mean of the Y -values.
Step 4:Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
Step 5:Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
Step 6:Use the slope m and the y -intercept to form the equation of the line.
Step 7:Obtain the straight line equation Y=mX+b and plot the scatterplot.
Step 8:Stop the program
## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Jai Sriram 
RegisterNumber: 212222040057
*/
```
```
import numpy as np
import matplotlib.pyplot as plt

x=np.array(eval(input()))
y=np.array(eval(input()))

x_mean=np.mean(x)
y_mean=np.mean(y)
num=0
denom=0

for i in range(len(x)):
    num+=(x[i]-x_mean)*(y[i]-y_mean)
    denom+=(x[i]-x_mean)**2

m=num/denom

b=y_mean-m*x_mean

print(m,b)

y_predicted=m*x+b
print(y_predicted)

plt.scatter(x,y)
plt.plot(x,y_predicted,color='red')
plt.show()




```

## Output:
<img src="https://github.com/Samuelmariappan/Find-the-best-fit-line-using-Least-Squares-Method/assets/119393030/ad06bd3f-42d8-448f-bfb7-20ba94f5ff02 height=450 width=450">



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
