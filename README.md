# cementStrengthPrediction
we have to identify the how much pressure can handle one meter cube of that concrete block
<br><br>

# Index

* [Problem statement](#problem-statement)
* [Goal of this Project](#goal-of-this-Project)
* [Glimpse of Dataset](#glimpse-of-Dataset)

### EDA
* [Check the missing values](#Check-the-missing-values)
* [Data Distribution](#data-distribution)
* [Data Transformation](#data-transformation)
* [check for outliers](#check-for-outliers) 
* [Features related with Target column](#features-related-with-target-column)
* [Correaltion using Heatmap](#correaltion-using-heatmap)



### Training Data Description
* [Architecture](#architecture)
* [Data Description](#data-description)
* Data Validation 
* Data Insertion in Database
* Model Training 

### Prediction Data Description
* Data Validation  
* Data Insertion in Database 
* Prediction 


## Demo project

## Problem Statement
### our problem statement is to predict the compressive strength of a cement block

### compressive strength: **how much pressure that one meter cube of that concrete block can handle**
<br>
<br>


## Goal of this Project
### why we need this ?
**if you are building something very tall building, bridges. they need to handle lot of pressure
	in that case if the block is not going to good. then your structure wont be durable . they wont be able
bear the road that they are design to bear. that's the reason we need compressive strength of cement.
  problem statement is based on quantity of different materials**
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

# Exploratory Data Analysis (EDA)  
<br>
<br>
  
  
  



## Check the missing values

* There is no missing value
  <p align="center">
<img src="https://github.com/rahulk15/images/blob/main/cement%20missing%20values.png" alt="command">
</p>
<br>
<br>
<br>
<br>

## Data Distribution

### For Some column there is some skewness present in the data
  <p align="center">
<img src="https://github.com/rahulk15/images/blob/main/cement%20Data%20Dirsibution.png" alt="command">
</p>
<br>
<br>
<br>
<br>

## Data Transformation
#### To remove this Skewness we are doing log transfromaton
#### Before doing log transformation, let's add 1 to each value in everycolumn. because some of the coluns of values are Zero so that we don't get exception while calculationg the log for value 0
* Here is the code :
<p align="center">
<img src="https://github.com/rahulk15/images/blob/main/code%20of%20log%20transformation.png" alt="command">
</p>

#### After Data transformation. a Data is in lot better shape than the previous
<p align="center">
<img src="https://github.com/rahulk15/images/blob/main/log%20transfromation.png" alt="command">
</p>
<br>
<br>
<br>
<br>

## check for outliers
#### mostly our data is good. very less outliers are there.so don't need to remove
<p align="center">
<img src="https://github.com/rahulk15/images/blob/main/outliers.png" alt="command">
</p>
<br>
<br>
<br>
<br>


## Features related with Target column
#### Well the relationship doesn't look particularly linear but we will try using Linear Regression and see how it works on our data. We will also Random forest regressor and compare our results from both the models.
<p align="center">
<img src="https://github.com/rahulk15/images/blob/main/cement%20correltion.png" alt="command">
</p>
<br>
<br>
<br>
<br>

## Correaltion using Heatmap
Highest correltion betwen features is 0.62
#### None of our columns seem to be correlated.
<p align="center">
<img src="https://github.com/rahulk15/images/blob/main/cement%20coreation%20with%20headmap.png" alt="command">
</p>
<br>
<br>
<br>
<br>


## Architecture
<p align="center">
<img src="https://github.com/rahulk15/images/blob/main/cement%20architecture.png" alt="command">
</p>
<br>
<br>
<br>
<br>



## Data Description
#### Given is the variable name, variable type, the measurement unit and a brief description. 
#### The concrete compressive strength is the regression problem. The order of this listing 
#### corresponds to the order of numerals along the rows of the database. 


 Name  	 Data Type   	 Measurement 	 Description|
| -------------------| ------------- | ------------- |-----------|
|Cement (component 1)|quantitative|kg in a m3 mixture|Input Variable|
| Blast Furnace Slag (component 2)  | quantitative  |kg in a m3 mixture|Input Variable-- Blast furnace slag is a nonmetallic coproduct produced in the process. It consists 								primarily of silicates, aluminosilicates, and calcium-alumina-silicates|
| Blast Furnace Slag (component 2)  |quantitative|kg in a m3 mixture|Input Variable- it is a coal combustion product that is composed of the particulates (fine particles of 											burned fuel) that are driven out of coal-fired boilers together with the flue gases. |
|Water (component 4)| quantitative  |kg in a m3 mixture|Input Variable|
| Superplasticizer (component 5)  | quantitative|kg in a m3 mixture|Input Variable--Superplasticizers (SP's), also known as high range water reducers, are additives used in 								making high strength concrete. Their addition to concrete or mortar allows the reduction of the water to cement ratio 								without negatively affecting the workability of the mixture, and enables the production of self-consolidating concrete 									and high performance concrete|
|Coarse Aggregate (component 6)|quantitative	|kg in a m3 mixture|Input Variable-- construction aggregate, or simply "aggregate", is a broad category of coarse to medium 					grained particulate material used in construction, including sand, gravel, crushed stone, slag, recycled concrete and geosynthetic aggregates|
|Fine Aggregate (component 7)|quantitative|kg in a m3 mixture|Input Variable—Similar to coarse aggregate, the constitution is much finer.|
|Age|quantitative|Day (1~365)|Input Variable|
|Concrete compressive strength|	quantitative|MPa|Output Variable|
<br>
<br>
<br>
<br>


## Data Validation 
#### Apart from training files, we also require a "schema" file from the client, which contains all the relevant information about the training files such as: Name of the files, Length of Date value in FileName, Length of Time value in FileName, Number of Columns, Name of the Columns, and their datatype.
### In this step, we perform different sets of validation on the given set of training files.  
#### 1. Name Validation- We validate the name of the files based on the given name in the schema file. We have created a regex pattern as per the name given in the schema file to use for validation. After validating the pattern in the name, we check for the length of date in the file name as well as the length of time in the file name. If all the values are as per requirement, we move such files to "Good_Data_Folder" else we move such files to "Bad_Data_Folder."
#### 2. Number of Columns - We validate the number of columns present in the files, and if it doesn't match with the value given in the schema file, then the file is moved to "Bad_Data_Folder."






## Glimpse of Dataset
  <p align="center">
<img src="https://github.com/rahulk15/images/blob/main/Screenshot%202021-04-16%20223124.png" alt="command">
</p>

