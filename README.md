# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
Step 1. Start the Program.

Step 2. Import the necessary packages.

Step 3. Read the given csv file and display the few contents of the data.

Step 4. Assign the features for x and y respectively.

Step 5. Split the x and y sets into train and test sets.

Step 6. Convert the Alphabetical data to numeric using CountVectorizer.

Step 7. Predict the number of spam in the data using SVC (C-Support Vector Classification) method of SVM (Support vector machine) in sklearn library.

Step 8. Find the accuracy of the model.

Step 9. End the Program. 

## Program:
```

/*
Program to implement the SVM For Spam Mail Detection..

Developed by :REVANTH.P

RegisterNumber: 212223040143
*/


import pandas as pd

data=pd.read_csv("Exp_11_spam.csv",encoding='windows-1252')

data.head()

dat.info()

data.isnull().sum()

x=data["v1"].values

y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test= train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer

#CountVectorizer is a method to convert text to numerical data. The text is transformed to a sparse matrix

cv=CountVectorizer()

x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy

```

## Output:

HEAD FUNCTION :

![image](https://github.com/user-attachments/assets/cfbceb85-b409-4a0c-980a-17db58ff04cc)

DATA INFORMATION :

![image](https://github.com/user-attachments/assets/ee43b100-c6bb-4f2d-98c4-518dab7b1939)

Y-PREDICT :

![image](https://github.com/user-attachments/assets/3d6fb57c-6659-4dd9-9c7e-6aa8159b0e33)

ACCURACY :

![image](https://github.com/user-attachments/assets/1d2209a4-8bb2-40ca-9583-1bfdb98e023b)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
