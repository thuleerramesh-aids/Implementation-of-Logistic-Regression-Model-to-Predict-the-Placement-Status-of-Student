# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
**Step 1:** Load and preprocess data – Import libraries, read dataset, drop salary column, and convert categorical data to numeric.

**Step 2:** Split dataset – Separate features and target, then divide into training and testing sets.

**Step 3:** Train model – Create and fit the logistic regression model using training data.

**Step 4:** Evaluate and visualize – Calculate accuracy and plot the logistic regression curve.


## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: THULEER R
RegisterNumber:212225230285

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
data = pd.read_csv("PlacementData.csv")
data = data.drop("salary", axis=1)
data = pd.get_dummies(data, drop_first=True)
X = data.drop("status_Placed", axis=1)
y = data["status_Placed"]
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
model = LogisticRegression(max_iter=1000)
model.fit(X_train, y_train)
print("Accuracy:", model.score(X_test, y_test))
X1 = X.iloc[:, 0].values.reshape(-1, 1)
model_plot = LogisticRegression(max_iter=1000)
model_plot.fit(X1, y)
plt.scatter(X1, y, color='blue')
x_values = np.linspace(X1.min(), X1.max(), 100)
y_values = model_plot.predict_proba(x_values.reshape(-1,1))[:,1]
plt.plot(x_values, y_values)
plt.xlabel("Feature")
plt.ylabel("Probability")
plt.title("Logistic Regression Curve")
plt.show()
*/
```

## Output:
<img width="493" height="371" alt="image" src="https://github.com/user-attachments/assets/c2ba2d3f-05aa-4674-8dbb-af2f82953942" />



## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
