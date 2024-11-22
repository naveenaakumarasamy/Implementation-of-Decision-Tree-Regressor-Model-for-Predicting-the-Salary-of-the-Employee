# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import libraries: Load necessary libraries (pandas, sklearn).
2. Load dataset: Read the Salary.csv file using pandas
3. Inspect data: Use head() and info() to understand the dataset structure and types.
4. Check missing values: Verify null values using.isnull().sum().
5. Encode categorical variables: Transform the Position column into numeric form using LabelEncoder
6. Define features and target: Separate features (x: Position and Level) and target (y: Salary ).
7. Split data: Divide the dataset into training and test sets using train_test_split.
8. Initialize Decision Tree: Create a DecisionTreeRegressor model.
9. Train the model: Fit the regressor on training data (x_train, y_train).
10. Predict on test set: Generate predictions for the test set (x_test).
11. Evaluate performance: Calculate metrics (Mean Squared Error and R2 Score) to assess model accuracy.
12. Predict new data: Use the trained model to predict salary for a new input ([5, 6]).
## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Naveenaa A K
RegisterNumber:  212222230094
*/
```
```
import pandas as pd

data=pd.read_csv("/content/Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder

le=LabelEncoder()

data["Position"]=le.fit_transform(data["Position"])

data.head()

x=data[["Position", "Level"]]

y=data["Salary"]

from sklearn.model_selection import train_test_split

x_train,x_test,y_train, y_test=train_test_split(x, y, test_size=0.2, random_state=2)

from sklearn.tree import DecisionTreeRegressor

dt=Decision TreeRegressor()

dt.fit(x_train, y_train)

y_pred=dt.predict(x_test)

from sklearn import metrics

mse=metrics.mean_squared_error(y_test,y_pred) mse

462500000.0

r2=metrics.r2_score(y_test,y_pred)

r2



dt.predict([[5,6]])


```

## Output:
![image](https://github.com/user-attachments/assets/b7adc02f-3d9f-402e-8449-bbeac322d8a7)
![image](https://github.com/user-attachments/assets/2065aa35-23e8-4ba2-823b-4db77be1a90f)
![image](https://github.com/user-attachments/assets/f9000e5c-a572-4d45-94c2-0b81399be0d0)










## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
