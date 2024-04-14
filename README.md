# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries.
2.Upload the csv file and read the dataset. 3.Check for any null values using the isnull() function.
3.From sklearn.tree inport DecisionTreeRegressor.
4.Import metrics and calculate the Mean squared error.
5.Apply metrics to the dataset, and predict the output.
## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: v.sanjay
RegisterNumber:  212223230188
*/
```


```
import pandas as pd
data=pd.read_csv("C:/Users/admin/Desktop/Salary.csv")
data.head()
```

```
data.info()
```

```
data.isnull().sum()
```

```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data['Position']=le.fit_transform(data['Position'])
data.head()
```

```
x=data[['Position','Level']]
y=data['Salary']
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier()
dt.fit(x_train,y_train)
y_predict=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_predict)
mse
```
```
r2=metrics.r2_score(y_test,y_predict)
r2
```

```
dt.predict([[5,6]])
```

## OUTPUT:

## df.head()

![image](https://github.com/sanjayy2431/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/149365143/3293b7de-0326-408f-8f73-424b654b224d)

## df.info()

![image](https://github.com/sanjayy2431/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/149365143/09988f91-43df-4784-8df9-615664d78bf2)

## data.isnull().sum()

![image](https://github.com/sanjayy2431/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/149365143/20fb64f3-534f-41de-94ba-933c425356b2)

## data.head()for position

![image](https://github.com/sanjayy2431/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/149365143/fec45cb6-b7c9-44f3-b863-1c67eb4158c0)

## MSE value

![image](https://github.com/sanjayy2431/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/149365143/fec45cb6-b7c9-44f3-b863-1c67eb4158c0)

## R2 value

![image](https://github.com/sanjayy2431/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/149365143/6ce9a84c-d867-42a7-82d0-13f3741dd02f)

## Prediction value

![image](https://github.com/sanjayy2431/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/149365143/3cf92e12-cbfc-4f9c-94ff-3f9cd3a06eac)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
