This Markdown file provides descriptions of the datasets from the course project, the steps required to obtain the tidy dataset, as well as the tidy dataset in a text file.

Introduction

This course project uses the data collected from the accelerometers on a Samsung Galaxy S smartphone. The various accelerometer readings were gathered from 30 volunteers (subjects) while they were performing different activities. When a subject took an action at a specific time, 561 features were used to describe that action.

The datasets can be obtained via the link below: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

The dataset includes the following files:

features_info.txt Shows information about the variables used on the feature vector.

features.txt List of all features.

activity_labels.txt Links the class labels with their activity name.

train/X_train.txt Training set.

train/y_train.txt Training labels.

test/X_test.txt Test set.

test/y_test.txt Test labels.

The following files are available for the train and test data:

train/subject_train.txt Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30.

train/Inertial Signals/total_acc_x_train.txt The acceleration signal from the smartphone accelerometer X axis in standard gravity units g. Every row shows a 128 element vector. The same description applies for the total_acc_x_train.txt and total_acc_z_train.txt files for the Y and Z axis.

train/Inertial Signals/body_acc_x_train.txt The body acceleration signal obtained by subtracting the gravity from the total acceleration.

train/Inertial Signals/body_gyro_x_train.txt The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second.

A full description is available at the site where the data was obtained: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

The purpose of this project is to demonstrate one�s ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis.

Data text files used

The following text files from the dataset were used for creating the final tidied dataset:

subject_train.txt and subject_test.txt
y_train.txt and y_test.txt
X_train.txt and X_test.txt
features.txt
activity_labels.txt
Variables included with tidied dataset

In the tidied dataset, there are 21 variables used for describing what is being obtained at a particular time. These are:

Subject.Number: Subject ID
Activity.ID: Activity ID between 1 to 6
Activity: The activity labels

tBodyAccMag-mean(): The average body acceleration magnitude

tGravityAccMag-mean(): The average gravity acceleration magnitude

tBodyAccJerkMag-mean(): The average body jerk signal

tBodyGyroMag-mean(): The average body acceleration magnitude

tBodyGyroJerkMag-mean(): The average jerk signal

fBodyAccMag-mean(): Signal 4 after the FFT was applied

fBodyBodyAccJerkMag-mean(): Signal 6 after the FFT was applied

fBodyBodyGyroMag-mean(): Signal 7 after the FFT was applied

fBodyBodyGyroJerkMag-mean(): Signal 8 after the FFT was applied

tBodyAccMag-std(): The standard deviation of the acceleration magnitude

tGravityAccMag-std(): The standard deviation gravity acceleration magnitude

tBodyAccJerkMag-std(): The standard devition of the body jerk signal

tBodyGyroMag-std(): The standard deviation body acceleration magnitude

tBodyGyroJerkMag-std(): The standard deviation jerk signal

fBodyAccMag-std(): Signal 13 after the FFT was applied

fBodyBodyAccJerkMag-std(): Signal 15 after the FFT was applied

fBodyBodyGyroMag-std(): Signal 16 after the FFT was applied

fBodyBodyGyroJerkMag-std(): Signal 17 after the FFT was applied

Steps of tidying data

Read all the files in your directory into R as tables and create traning and test data frames.
Merge training and test dataset.
Create a tidy dataset with the average of each variable for each activity and each subject.
Save the tidied data into directory.
The final data frame

The data was exported as a text file. There are a total of 180 rows and 68 columns in the file. The R code for creating this dataset is included in this repo: run_analysis.R.
