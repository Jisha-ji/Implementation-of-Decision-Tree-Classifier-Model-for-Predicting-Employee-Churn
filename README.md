# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Start the program.

2.Import pandas module and import the required data set.

3.Find the null values and count them.

4.Count number of left values.

5.From sklearn import LabelEncoder to convert string values to numerical values.

6.From sklearn.model_selection import train_test_split.

7.Assign the train dataset and test dataset.

8.From sklearn.tree import DecisionTreeClassifier.

9.Use criteria as entropy.

10.From sklearn import metrics.

11.Find the accuracy of our model and predict the require values.

12.End the program. 

## Program:
```
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: JISHA BOSSNE SJ
RegisterNumber:  212224230106

```
```
import pandas as pd
data=pd.read_csv("/content/Employee (1).csv")
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
```
## Output:

Data.head():

<img width="524" height="377" alt="328614684-b7704ad6-9b7c-4d44-bb50-b02cda461721" src="https://github.com/user-attachments/assets/1f33ebb8-1505-4f4d-858c-563cdf4744b5" />



Data.info():

<img width="524" height="377" alt="328614684-b7704ad6-9b7c-4d44-bb50-b02cda461721" src="https://github.com/user-attachments/assets/17e1eb9c-6414-426f-b782-5da78ecd2e00" />


isnull() and sum():

<img width="317" height="251" alt="328614779-673f7e80-404c-4884-9cec-cb25d5319056" src="https://github.com/user-attachments/assets/ebd17e77-00b5-4c61-a631-f372c612f825" />


Data Value Counts():

<img width="266" height="85" alt="328614838-7e3b45df-a46a-4817-8aad-284ce5112b18" src="https://github.com/user-attachments/assets/747d0cc2-6086-43d6-957c-5022222341bb" />


Data.head() for salary:

<img width="1241" height="221" alt="328614960-fc253d0f-08cb-40ae-a87d-dca204a30af8" src="https://github.com/user-attachments/assets/7ad94558-1061-472c-bd3a-c043a99e9972" />


x.head:

<img width="1015" height="200" alt="328615069-23629d0d-1496-4083-9974-d8e67a9714be" src="https://github.com/user-attachments/assets/8a845cbf-9113-44ae-bca6-a8b0a3a5b20e" />


Accuracy Value:

<img width="111" height="34" alt="328615883-31074d56-b702-4696-8373-44d982ca1d40" src="https://github.com/user-attachments/assets/ff99d890-04f5-4016-a8a7-d5500567c3f2" />


Data Prediction:

<img width="479" height="86" alt="328615830-f3d4c1ef-123c-4c1e-bd27-9bae684e013c" src="https://github.com/user-attachments/assets/fce6c99d-5d7b-41b5-a92b-114a4e7c5c45" />

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
