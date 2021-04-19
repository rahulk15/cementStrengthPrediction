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
* [Problem Statement](#problem-statement)
* Architecture
* Data Description
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

















## Glimpse of Dataset
  <p align="center">
<img src="https://github.com/rahulk15/images/blob/main/Screenshot%202021-04-16%20223124.png" alt="command">
</p>


| First Header  | Second Header | First Header  |
| ------------- | ------------- | ------------- |
| Content Cell  | Content Cell  |		|
| Content Cell  | Content Cell  |		|
| First Header  | Second Header |		|
| Content Cell  | Content Cell  |		|
| Content Cell  | Content Cell  |		|

