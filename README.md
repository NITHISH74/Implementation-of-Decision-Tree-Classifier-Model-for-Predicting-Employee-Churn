# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm:

## Step 1: 
Import the required libraries.
## Step 2: 
Upload and read the dataset.
## Step 3:
Check for any null values using the isnull() function.
## Step 4:
From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.
## Step 5:
Find the accuracy of the model and predict the required values by importing the required module from sklearn.
## Step 6:
Check the trained model.




## Program:
```python
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: NITHISHWAR S
RegisterNumber:  212221230071
/*
import pandas as pd
d=pd.read_csv("Employee (1).csv")
d.head()
d.info()
d.isnull().sum()
d["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
l=LabelEncoder()
d["salary"]=l.fit_transform(d["salary"])
d.head()
x=d[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
y=d["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)

from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
acc=metrics.accuracy_score(y_test,y_pred)
acc 
dt.predict([[.5,.8,9,260,6,0,1,2]])


```

## Output:
## Initial Dataset:
![image](https://user-images.githubusercontent.com/94164665/173245844-b7965fa5-c744-4221-90c3-b25b67bdffe2.png)

## Dataset information:
![image](https://user-images.githubusercontent.com/94164665/173245872-6bb28f98-7c45-4b68-9de3-36a3cdc2baa5.png)
![image](https://user-images.githubusercontent.com/94164665/173245884-ada2710c-1a30-441d-a2a2-f327ab130b85.png)
## Left column value count:
![image](https://user-images.githubusercontent.com/94164665/173245897-0b4af7ed-0690-469d-b29b-f5183a70dfdf.png)
## Encoded Dataset:
![image](https://user-images.githubusercontent.com/94164665/173245910-dd541975-3f51-44c3-8732-44506716874e.png)

## X set:
![image](https://user-images.githubusercontent.com/94164665/173246041-1e7a0171-cc9c-4f42-87f7-68901b59e352.png)

## Y values:
![image](https://user-images.githubusercontent.com/94164665/173246066-b883e5fb-0597-4739-838b-b1b1a63975c1.png)
## Accuracy score:
![image](https://user-images.githubusercontent.com/94164665/173246183-6f7cb4bb-3597-4516-aa20-4f81808bb75e.png)

## Result value of Model when tested:
![image](https://user-images.githubusercontent.com/94164665/173246218-8b3c7219-09ab-4533-8856-745eebc553f9.png)




## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
