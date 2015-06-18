HARDS Analysis
=====================

## Overview Explanation

This exercise, that I have called HARDS Analysis (Human Activity Recognition Data Set Analysis), consist in analyse and study the data stored in a set of files generated from a experiment, where  a group of 30 people performed a serie of activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING), wearing a smartphone with embedded accelerometer and gyroscope. The goal of this experiment is to study the [Human Activity Recognition] (https://en.wikipedia.org/wiki/Activity_recognition) since today it is easier and cheaper to survey data about it with the used of smartphones.

With the help of this smartphone was possible to get spatial, acceleration, velocity and angular values for the 3-axial, for the six activity performed by the people.

The files mentioned above are contained in a directory called *"UCI HAR Dataset"* and can be downloaded from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip. This directory is structured as follow: 

![UCI HAR Dataset directory](https://github.com/jalvarado1381/HARDS-Analysis/blob/master/UCI_HAR_Dataset_Structure.png "UCI HAR Dataset directory")

As you can see at the image it is compound by two directories called **test** and **train**, containing the data obtained in  the experiment (X_test.txt and X_train.txt files), the README.txt (general information about experiment and the data)  and the files activity_labels.txt, features_info.txt and features.txt (these three last file made up the Code Book).

Our work consist in merge the files X_test.txt and X_train.txt located in the directories **test** and **train** respectively to get a data set from which we're going to take the means() and std() variables to create newly another data set with only those variables, once we have it, it is necessary to generate another new data set with the [average](https://en.wikipedia.org/wiki/Average#Arithmetic_mean) of each variable for each activity and each subject.

##Script Explanation

1.- Merging  the training and the test sets.

2.- Extracting the measurements on the mean and standard deviation for each measurement.

3.- Translating numbers to descritive names, for activities.

4.- Working on variable names.

5.- Creating the new Data Set and and taking it to a file.

##How to execute the script

1.- Clone the repository HARDS-Analysis from github

    git clone https://github.com/jalvarado1381/HARDS-Analysis.git
  
2.- Open the R console  or R Studio and setup the directory HARDS-Analysis, the directory created by the cloned proccess, as your working directory.
  
    Example:
    
        1.-  $ R ## Executing R in your GNU/Linux or Mac command line
   
        2.-  > setwd("PATH_WHERE_YOU_HAVE_THE_REPOSITORY/HARDS-Analysis")
  
3.- Copy the directory "UCI HAR Dataset" to the repository directory HARDS-Analysis

4.- Once the directory "UCI HAR Dataset" is copied into HARDS-Analysis directory execute the following in your R console or R Studio:

    source("run_analysis.R")

##Data set Source
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
