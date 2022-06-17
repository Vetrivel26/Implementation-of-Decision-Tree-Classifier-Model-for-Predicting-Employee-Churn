# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
~~~
1.Import the standard libraries. 
2.Upload the dataset and check for any null values using .isnull() function. 
3.Import LabelEncoder and encode the dataset. 
4.Import DecisionTreeClassifier from sklearn and apply the model on the dataset. 
5.Predict the values of array. 
6.Import metrics from sklearn and calculate the accuracy of the model on the dataset. 
7.Predict the values of array. 8.Apply to new unknown values.
~~~
## Program:
```
/*

Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: VETRIVEL S
RegisterNumber:  212221240060
import pandas as pd
data=pd.read_csv("Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics   
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
*/
```

## Output:


![decision tree classifier model](sam.png)
### DATA HEAD
![1](https://user-images.githubusercontent.com/95363138/174314191-285d77cf-9754-47a2-ae45-a5802e72ab35.png)
### DATA INFO
![2](https://user-images.githubusercontent.com/95363138/174314620-ee91bf9f-42c3-4cb0-a2b1-c762cda2c4b9.png)

### DATA ISNULL
![3](https://user-images.githubusercontent.com/95363138/174314630-f3d2ddfb-b423-4d65-bed1-8d5e65ef840e.png)

### DATA LEFT
![4](https://user-images.githubusercontent.com/95363138/174314638-9fef51da-7434-48c9-a3d2-8f36ab6eb6dc.png)

### X HEAD
![5](https://user-images.githubusercontent.com/95363138/174314655-879cdaf6-1d51-4986-b2e1-45d375a434c2.png)

### DATA FIT
![6](https://user-images.githubusercontent.com/95363138/174314669-ba2a9d05-f0e3-471d-b5e0-f35fd27625fd.png)

### ACCURACY
![7](https://user-images.githubusercontent.com/95363138/174314684-f7e08f50-ad2f-497b-a3a3-76ad401128d7.png)

### PREDICTED VALUES
![8](https://user-images.githubusercontent.com/95363138/174314703-4b8703a7-e81c-4dd5-959b-e981ddb43c83.png)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
