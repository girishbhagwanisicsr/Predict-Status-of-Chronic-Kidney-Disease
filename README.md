# Predict-Status-of-Chronic-Kidney-Disease
Using XGBoost and RandomizedSeachCV algorithm to predict whether the person has the Chronic Kidney Disease
Problem Statement:

1.Perform Data-Preprocessing & Prepare your data for Analysis & Modelling Purpose As Well.
	Converted Column from object data type to Float data type
	Remove unwanted columns like (ID)   command to remove is df.drop('id',axis=1,inplace=True)    here axis=1 cause we have to drop in vertical way and we have to update our data frame also so inplace=True

2.Apply Data Cleaning Techniques on data & clean your data
		Extract what are my categorical column and what are numerical column
		Now Check whether data has dirtiness or not
		Check How many unique values are there in categorical column and numercial column
3.Check Label Distribution of categorical Data

4.Check How columns are co-related with each other and its impact or target feature
		Using Built-in corr() function
		using heatmap and visualize the values using annot - true


5.Automate Your analysis:-
			Note:-if there is any relation between columns go with scatter()
			Analysing distribution of 'red_blood_cell_count' chronic as well as no-chronic 

Conclusion:-We can get person who does'nt have chronic disease has high red blood cell count

6.Performing exploratary data analysis on the data
7.Perform data cleaning & deal with missing values
			:-If missing value data is small then you can take mean,median and std deviation
				but when data is like total 10000 
						missing 8000
							then you should not take mean,median for consideration
						suppose for the red blood cells if missing values will become normal so its graph will go up so in this scene we have to determine in both the graph will disbalance							generating sample for red blood cell null values then assigning value to null cells  using this function "random_sample_rbcc=data['red blood cell count'].dropna().sample(131)"

8.Automate the filling values of column of the dataset using pre-defined function
					for loop to fill null values with the sample data
9.Feature  Encoding technique on data 
		Sometimes when we pass categorical data to machine learning understanding it doesn't understand the normal/abnormal checked/notchecked so to make machine understand we have to convert these to 0/1 is called feature encoding
		Use from sklearn.preprocessing import LabelEncoder for converting normal to 0	abnormal to 1
		and same for all the columns


Is it is necessary to apply feature encoding?
if there are less categories then you can do label encoding and if the catergories are more than understand the catergories and its thershold values 

10.Selecting best Features for your model using suitable feature importance techniques
		Select some K best feature from some N number of features 
		from sklearn.feature_selection import SelectKbest
		this class will check whether the probability value is less than 0.5 or not
		so based upon probability value it will order all the feature which we exatly need for model building as there are 25 features in our dataset	
11.Store the columns in an array

12.Build a cross-validated model & predict & check accuracy of your model
	
we are using xgboost algorithm
RandomizedSearchCV

Conclusion:-
	Our prediction model is predicting 0.97% accuracy 	
