Machine learning using python: 
how to load data:     https://www.datacamp.com/community/tutorials/pandas-read-csv


I tried linear regression function:
```python
reg = linear_model.LinearRegression()
```

predict function:
```python 
predict([[4]])
```

The bug I encountered was in the predict function, it is expecting 2d array, but I gave 1d array. 



Training dataset, validation dataset, test dataset:
If the dataset is big enough(not sure how to decide if the dataset is big), we can split dataset into training dataset, validation dataset and training dataset. Otherwise, we can split the dataset only into training dataset and testing dataset.  In this case, we can use other validation process such as cross validation, boostrap... 

Cross validation is the process that rotate to use a partition of the dataset and get the average of the error value. 

What is the difference between validation set and testing set?: Validation happens before deciding the model and testing set happens after the model is decided. 

The following is the python code for cross validation:
```python 
scores = cross_val_score(reg, np.array(ds.YearsExperience).reshape(-1, 1), np.array(ds.Salary), cv = 10)
```
cv number can be changed. 10 represents 10 fold cross validation. 