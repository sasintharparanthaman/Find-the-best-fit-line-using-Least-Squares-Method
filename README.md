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
Developed by: Sasinthar P
RegisterNumber:  212223230199
*/
import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input()))
Y=np.array(eval(input()))
Xmean=np.mean(X)
Ymean=np.mean(Y)
num,den=0,0 # num = numerator, den = denomenator
for i in range(len(X)):
  num+=(X[i]-Xmean)*(Y[i]-Ymean)
  den+=(X[i]-Xmean)**2
m=num/den
c=Ymean-m*Xmean
print(m,c)
Y_pred=m*X+c
print(Y_pred)
plt.scatter(X,Y)
plt.plot(X,Y_pred,color="red")
plt.show()
```

## Output:

## input values are 
![Screenshot 2024-09-27 190358](https://github.com/user-attachments/assets/ef2965ca-df4a-423f-a34e-0c37f72e742c)


## slope:
![Screenshot 2024-09-27 190405](https://github.com/user-attachments/assets/832d6778-2626-4c42-bcfb-87b0c0ceec2e)


## y_intercept:
![Screenshot 2024-09-27 190415](https://github.com/user-attachments/assets/1bb1dc5a-6b6b-48c4-a55e-830aa9b98c6a)


## y_predict:
![Screenshot 2024-09-27 191657](https://github.com/user-attachments/assets/48ef3c13-4946-4d9a-aadc-0f8a0def32b0)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
