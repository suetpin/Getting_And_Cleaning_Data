This file consists of description about the variables and other information used in the script run_analysis.R

### Project Description

The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. 
The goal is to prepare tidy data that can be used for later analysis.

###Collection of the raw data

The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. Reading the website information is helpful for this course project.
It can be obtrained [here.](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

###Original data source
The data source for this project can be download [here.](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) 

###Variables and relevent information

1. dataActivityTest
	* read data from y_test.txt
	* class = data frame
	* dim = 2947 x 1
2. dataActivityTrain
	read data from y_train.txt
	class = data frame
	dim = 7352 x 1
3. dataSubjectTest
	* read data from subject_test.txt
	* class = data frame
	* dim = 2947 x 1
4. dataSubjectTrain
	* read data from subject_train.txt
	* class = data frame
	* dim = 7352 x 1
5. dataFeaturesTest
	* read data from X_test.txt
	* class = data frame 
	* dim = 2947 x 561
6. dataFeaturesTrain
	* read data from X_train.txt
	* class = data frame
	* dim = 7352 x 561
7. dataSubject 
	* combine dataSubjectTrain and dataSubjectTest
	* class = data frame
	* dim = 10299 x 1
8. dataActivity
	* combine dataActivityTrain and dataActivityTest
	* class = data frame
	* dim = 10299 x 1
9. dataFeatures
	* combine dataFeaturesTrain and dataFeaturesTest
	* class = data frame
	* dim = 10299 x 561
10. dataCombine 
	* combine dataSubject and dataActivity
	* class = data frame
	* dim = 10299 x 2
11. Data
	* combine dataFeatures and dataCombine
	* class = data frame
	* dim = 10299 x 68
12. subdataFeaturesNames
	* select only **mean** and **std** from dataFeaturesNames$V2
	* total of 66
13. selectedNames
	* append subdataFeaturesNames with **subject** and **activity**
	* class = character
	* total of 68
14. Data
	* subset the **Data** from 11 by **selectedNames** from 13	
	* class = data frame
	* dim = 10299 x 68
15. activityLabels
	* read data from activity_labels.txt
	* total of 6 different activities
16. Data$activity
	* data with descriptive activity names	
17. Data2 
	* tidy data with descriptive variable names
	* dim = 180 x 68

prepared by Suet Pin
