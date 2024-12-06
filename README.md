# Machine-Learning-project
Garment Worker Productivity Prediction using Machine Leaning Models

GARMENT WORKER PRODUCTIVITY PREDICTION 
Introduction
This project focuses on predicting productivity levels in the garment manufacturing industry. Using operational data such as work-in-progress (WIP), overtime, and incentives, you will develop a machine-learning model to forecast productivity. Your work will directly contribute to optimizing resource allocation and improving operational efficiency. Essential tasks include data preparation, analysis, and building models using logistic regression, random forests, and gradient-boosting techniques.
Loading the libraries
 ![image](https://github.com/user-attachments/assets/df758683-dc94-429f-9d8e-cf2264e540db)

Loading the data set  
![image](https://github.com/user-attachments/assets/5ba69fda-569d-4be5-b51a-ec71bd7a8fb4)
Getting information about the data 
 
![image](https://github.com/user-attachments/assets/c8fc3bf3-3a47-41c0-b5ac-f3d5b4166175)
![image](https://github.com/user-attachments/assets/ed77d81d-4069-4977-8011-b6de585eab63)

Type of dataset 
![image](https://github.com/user-attachments/assets/308da5b3-b5d4-4e6b-8de5-ba4495e326a4)

Cleaning the dataset by looking for duplicates , null values and One Hot Encoding
 ![image](https://github.com/user-attachments/assets/a73a5ed7-cc1b-4286-98ba-9f809bbcc1f1)

 ![image](https://github.com/user-attachments/assets/4bd7bf56-4551-409c-a84f-401417be098b)

Fixing the null values and checking for outliers using scatter plot  
 ![image](https://github.com/user-attachments/assets/170bea53-6661-43f3-93b2-e9ba47b21dcc)
 ![image](https://github.com/user-attachments/assets/54b305c9-a1dd-442c-8d6f-8db1024d712b)
 ![image](https://github.com/user-attachments/assets/f81cee14-ef0b-4022-adcb-bcd23cec2d60)

Standardization 
![image](https://github.com/user-attachments/assets/bffc095a-85f7-429b-bf31-19f74c575c04)

Pipeline
![image](https://github.com/user-attachments/assets/8b0e9373-5e8a-482b-a7db-40f2945b8d1d)

 Heatmap      
 ![image](https://github.com/user-attachments/assets/dab7a287-1126-4ef0-9fa5-31161392f231)
 Machine Learning Models
![image](https://github.com/user-attachments/assets/76be6910-0b58-4342-8b71-d82966a97a34)
![image](https://github.com/user-attachments/assets/f8ff36fe-3b9c-4464-9236-0fa51e12c56f)
![image](https://github.com/user-attachments/assets/1099286e-8383-42b6-bafd-22c2cff5c83f)
![image](https://github.com/user-attachments/assets/606f4a10-e0f6-49aa-a514-28e56a6c0f56)

Data Understanding and Preprocessing
This data is in CSV format. I had to import some libraries so that I could perform some analysis of the data. I imported the data into my Jupiter notebook. The data set had 15 columns and 1197 rows, so it's a small dataset.
The data had both categorical and numerical data types. The categorical dataset includes the date, quarter, department, and day, while the numerical data set had the rest of the dataset.
The data provided had many errors, so as a Machine Learning specialist, the first thing you should do to the raw data provided is to clean it.
1.	Data cleaning is done by removing any duplicate values that might be there. Luckily for me, this data was not duplicated. The values were also well aligned in the columns, so there was no need to use trim or proper to make the data look presentable.
2.	Handling missing values. This is another way of cleaning data values, where you deal with the null values. This is done in different ways depending on the dataset set available. In this dataset, wip had null values, so we used the median to fill the null values. There is another method where you delete the null values. This is where the null values are so many, and the data set is so enormous that deleting the null row will not affect our data.
3.	Detecting outliers. The best method to detect outliers is using a boxplot or scatter plot, as you can see the outliers visually. From  idle_time, the outliers were ID [615,617,650,654], and I dropped them. The outliers were [1130,1133] on incentive, so I did drop them.
4.	Scaling . This is where we use another normalization or standardization to run our model. Standardization is best because it makes our data set properties of a typical standard distribution where the mean is usually zero and the standard deviation is 1. I performed standardization on smv 'over_time,' and the values ranged from 1 to 0. It helps models that are sensitive to features to perform better
5.	Encoding. This is done to categorical data that is nominal. I performed it on departs and quarters. The encoding makes the categorical data numerical, and the machine learning models can interpret them.
6.	Dropping the data set. I did drop some columns that were not useful in the data set, such as date and day.
Visualization
To better understand the relationship between the features and the target value, you need to plot some diagrams. A heat map is the best way to visualize the correlation between all the numerical features and the target. 

Modelling
A variety of machine models are going to be created to help in the prediction. The models include linear, lasso, random Forest Regressor, and Gradient boosting. We must split the data into X and y to conduct the modeling. Our  X = 'team,' 'targeted_productivity,' 'smv,' 'over_time,' 'incentive,' 'idle_time,' 'idle_men,' 'no_of_style_change,' 'no_of_workers' and y = ['actual_productivity']. Then, we use this to get the MAE, MSE, and R2  
