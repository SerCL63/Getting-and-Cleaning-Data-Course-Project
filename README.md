## Getting-and-Cleaning-Data-Course-Project
With this project, data from a Samsung Galaxy S smartphone accelerometer and gyroscope was obtained and cleaned to get a tidy data set that could be analyzed later

This repository contains the following files:

-README.md, this file, which gives a general description of the data set.

-tidy_data.txt, which contains the data set

-CodeBook.md, which describes the data set's contents 

-run_analysis.R, an R script that created the data set

# Study design

The Human Activity Recognition Using Smartphones Data Set had the source data for this project. This data was originally obtained in the following manner: 

"The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain."

The training and test data were merged to create a single data set, and the mean and std. deviation were calculated for each measurement. Then, the mean of the measurements themselves wa obtained for each subject and activity, which in turn produces the final data set.

# Creating the data set
The R script run_analysis.R was used to create the final data set. It implements the following steps:

-Download the data

-Read the data

-Merge the training and the test sets

-Extract measurements on mean and std. deviation for every measurement.

-Name each activity in the data set.

-Label the data set with variable names.

-Create the tidy data set with the average of each variable for each activity/subject.

-Write the data set to the tidy_data.txt file.
The tidy_data.txt in this repository was created by running the run_analysis.R script using R version 3.5.2 (2018-12-20) on Windows 10 64-bit edition.
