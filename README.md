# Getting-and-Cleaning-Data-Project
For Getting-and-Cleaning-Data-Project

Summary

This repository includes a single script, run_analysis.R, that merges data from the Human Activity Recognition Using Smartphones Data Set project at the UCI Machine Learning Repository to produce averages values per user per activity for the dataset's mean and standard deviation features. Refer to the included codebook.md for more information.

Usage

Set the working directory to the folder containing the activity recognition dataset. Run the script run_analysis.R. The script produces a single output file, tidy-data.txt, that contains the merged and transformed data.

UCI HAR Dataset - Data files downloaded from "https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip"
* run_analysis.R - R script which contains the data preparation, manipulation and tidy data set creation logic.
* CodeBook.md – Tells about the  run_analysis.R script and tidy data set variable description
* tidydata.txt - Tidy data output based on Coursera project assignment
* README.md - Mark down files to provide high level information on the repository objects.
 run_analysis.R Performs the below
* Merges the training and the test sets to create one data set. :- Load data to table and use command cbind,rbind and combine training and test data sets
* Extracts only the measurements on the mean and standard deviation for each measurement. :- Use grep command to get column indexes for variable name contains "mean()" or "std()"
* Uses descriptive activity names to name the activities in the data set. :- Added new column activity description as factor using merge() and grep()
* Appropriately labels the data set with descriptive variable names. :- Replace with descriptive names using gsub()
* From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject : - Used aggregate() function and order by to arrange in sequence
