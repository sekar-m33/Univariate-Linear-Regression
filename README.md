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
```py
import numpy as np
import matplotlib.pyplot as plt
x=np.array([0,1,2,3,4,5,6,7,8,9])
y=np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()

x_mean=np.mean(x)
y_mean=np.mean(y)

num=0
den=0
for i in range(len(x)):
    num +=(x[i]-x_mean)*(y[i]-y_mean)
    den +=(x[i]-x_mean)**2
m=num/den
c=y_mean-m*x_mean
print(m,c)

y_pred= m*x+c
print(y_pred)
plt.scatter(x,y)
plt.plot([min(x),max(x)],[min(y_pred),max(y_pred)],color="red")
plt.show
```
## Output
<img width="1424" height="700" alt="image" src="https://github.com/user-attachments/assets/7d07d530-4c1a-4ffe-aacd-cde9fb3b1f33" />
<img width="1415" height="290" alt="image" src="https://github.com/user-attachments/assets/6f08ebfc-79a8-467b-8892-2b004003d844" />
<img width="1410" height="747" alt="image" src="https://github.com/user-attachments/assets/b3e5d522-2970-40c7-89e5-270bb931e9d0" />

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
