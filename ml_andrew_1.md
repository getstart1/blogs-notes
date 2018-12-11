What is machine learning? 
-- a computer program is said to learn from experience E with respect to some class of tasks T and performance measure P, if it's performance at task T, as measured by P and improves with experience E. 

From my understanding, it is we try to improve the computer's performance on a certain task, and at the same time, measure the performance of the task. 


Gradient Descent:
Gradient descent uses calculus as the calculating method to obtain the minimum change of m and b(in y = mx + b)
minimum change of m = error * m 
minimum change of b = error
Youtube resource: https://www.youtube.com/watch?v=jc2IthslyzM

Learning rate decides if the gradient descent converges and when to converge.  

A blog about learning rate: https://towardsdatascience.com/understanding-learning-rates-and-how-it-improves-performance-in-deep-learning-d0d4059c1c10



Now I understand that there should be 

I want to learn by real life practice. The first thing I want to try is linear regression and gradient descent. I chose a dataset from the following Kaggle website: https://www.kaggle.com/rsadiq/salary/version/1


Machine learning using python: 
how to load data:     https://www.datacamp.com/community/tutorials/pandas-read-csv
important


Training dataset, validation dataset, test dataset:
If the dataset is big enough(not sure how to decide if the dataset is big), we can split dataset into training dataset, validation dataset and training dataset. Otherwise, we can split the dataset only into training dataset and testing dataset.  In this case, we can use other validation process such as cross validation, boostrap... 

Cross validation is the process that rotate to use a partition of the dataset and get the average of the error value. 

What is the difference between validation dataset and testing dataset?: Validation happens before deciding the model and testing dataset happens after the model is decided. 



