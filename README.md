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
<p align="center">
<img src="https://github.com/rahulk15/images/blob/main/log%20transfromation.png" alt="command">
</p>
<br>
#### After Data transformation. a Data is in lot better shape than the previous
<p align="center">
<img src="https://github.com/rahulk15/images/blob/main/log%20transfromation.png" alt="command">
</p>















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

