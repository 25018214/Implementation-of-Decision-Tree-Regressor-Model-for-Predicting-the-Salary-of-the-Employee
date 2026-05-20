# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the standard libraries from python.

2.Upload the dataset and check for any null values using .isnull() function.

3.Import LabelEncoder and encode the dataset.

4.Import DecisionTreeRegressor from sklearn and apply to the model from the dataset.

5.Predict the values of the arrays.

6.Import metrics from sklearn and calculate the MSE and R2 of the model from the dataset.

7.Predict the values of array

8.Apply it to the new unknown values.

## Program
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Akash A
RegisterNumber:212225230008

```

```
import pandas as pd
data=pd.read_csv(r"C:\Users\acer\Downloads\Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

```

<img width="682" height="420" alt="595148681-1158d567-d798-4623-99f3-b3206059c3cb" src="https://github.com/user-attachments/assets/9abe4f26-570f-4688-b896-d5a7756bbc47" />
<img width="448" height="371" alt="595148730-72542dd2-01bc-4ae4-bd5e-51fc6069b9fc" src="https://github.com/user-attachments/assets/4cc199cf-bf84-408d-837f-7211396e0298" />


```
x=data[["Position","Level"]]
x.head()
```

<img width="291" height="366" alt="595149084-c1fb1b13-6d43-47f3-a430-759a7c6c23f1" src="https://github.com/user-attachments/assets/ee70f149-40eb-4f41-90cc-248cd2045604" />


```
y=data[["Salary"]]
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse
```

<img width="242" height="78" alt="595149330-76f07d61-cc3c-4d1f-b660-62dc87a7bc78" src="https://github.com/user-attachments/assets/5ba17e98-8fc9-496c-8e3c-34c8d605aadc" />


```
r2=metrics.r2_score(y_test,y_pred)
r2
```

<img width="497" height="87" alt="595149418-83f02130-339f-4b16-b45a-69d7f831e90c" src="https://github.com/user-attachments/assets/d35bcd86-0274-4c46-8f06-491cf34fffbb" />




## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
