# EX-06-Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

  1. Import pandas module and import the required data set.

  2. Find the null values and count them.

  3. Count number of left values.

  4. From sklearn import LabelEncoder to convert string values to numerical values.

  5.From sklearn.model_selection import train_test_split.

  6.From sklearn import metrics.Find the accuracy of our model and predict the require values.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Vikash s
RegisterNumber:  212222240115

import pandas as pd
data = pd.read_csv("/content/Employee.csv")
data.head()
data.info()

data.isnull().sum()

data["left"].value_counts

from sklearn.preprocessing import LabelEncoder
le= LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()

x= data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]

x.head()
y=data["left"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state = 100)


from sklearn.tree import DecisionTreeClassifier
dt = DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)

y_pred = dt.predict(x_test)
from sklearn import metrics

accuracy = metrics.accuracy_score(y_test,y_pred)
accuracy

dt.predict([[0.5,0.8,9,260,6,0,1,2]])
*/
```

## Output:

## 1.DATASET:
![image](https://github.com/vikashsenthil21/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119433834/ace6347d-aa7d-4718-9a63-252b4f5ffd3a)






## 2.df.inf0()
![image](https://github.com/vikashsenthil21/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119433834/6575358e-dc3b-4fe1-8766-416790574860)



## 3.ISNULL:
![image](https://github.com/vikashsenthil21/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119433834/d557481b-8334-4dcf-8beb-7ae3640611fa)



## 4.VALUE COUNTS:
![image](https://github.com/vikashsenthil21/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119433834/f815b8a5-77ae-41c7-be46-4a5a57eb1aaa)



## 5.Dataset transformed head:
![image](https://github.com/vikashsenthil21/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119433834/1600b88f-86d6-48eb-af76-8895732ea41a)




## 6.X.head():
![image](https://github.com/vikashsenthil21/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/119433834/811a8d58-d4e7-4c5d-8f80-e1d4ddf474dd)





## 7.ACCURACY:

![8](https://github.com/Pavithraramasaamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118596964/d90e7c59-cc85-4dcb-b574-7fe1b58b9703)


## 8.PREDICT:

![9](https://github.com/Pavithraramasaamy/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118596964/e275dca9-0f6a-4944-97fe-b359c993582e)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
