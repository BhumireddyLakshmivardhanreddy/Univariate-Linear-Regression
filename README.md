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
```python
#Program to implement univariate Linear Regression to fit a straight line using least squares.
#Developed by: BHUMIREDDY LAKSHMI VARDHAN REDDY
#register number: 212223240016
import numpy as np 
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)
plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()
```
## Output
![Univariate linear](https://github.com/BhumireddyLakshmivardhanreddy/Univariate-Linear-Regression/assets/148514637/3cd60e7a-9161-4734-97b1-78c829d8b9a3)
![Univariate linear 2](https://github.com/BhumireddyLakshmivardhanreddy/Univariate-Linear-Regression/assets/148514637/d109082a-e731-48ab-93eb-3f3d1f62a0e3)
![Univariate linear1](https://github.com/BhumireddyLakshmivardhanreddy/Univariate-Linear-Regression/assets/148514637/38b7276d-813e-40c5-b153-5bfb8c8bfbb9)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
