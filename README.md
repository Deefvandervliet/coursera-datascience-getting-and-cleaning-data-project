# coursera-datascience-getting-and-cleaning-data-project

# purpose
The purpose of this project is to demonstrate my ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. The data used is data collected from the accelerometers from the Samsung Galaxy S smartphone

# background
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

#transformation steps:
##The following (transformation) steps were taken to transform the initial dataset

1 Download the dataset from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

2 unzip the dataset into a folder inside the current workdir folder.

3 Merging of the training and the test files inside the dataset to create one data set.

4 Extracts only the measurements on the mean and standard deviation for each measurement.

5 Uses descriptive activity names to name the activities in the data set

6 Appropriately labels the data set with descriptive variable names.

7 From the data set in step 6, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
The data is in "wide" format as described by Wickham; there is a single row for each subject/activity pair, and a single column for each measurement.
This data set can be found in the tidyMeans.txt file, which can be read into R with read.table("tidyMeans.txt", header = TRUE). A detailed description of the variables can be found in CodeBook.md. The basic naming convention is:

Mean{timeOrFreq}{measurement}{meanOrStd}{XYZ}

Where timeOrFreq is either Time or Frequency, indicating whether the measurement comes from the time or frequency domain, measurement is one of the original measurement features, meanOrStd is either Mean or StdDev, indicating whether the measurement was a mean or standard deviation variable, and XYZ is X, Y, or Z, indicating the axis along which the measurement was taken, or nothing, for magnitude measurements.
