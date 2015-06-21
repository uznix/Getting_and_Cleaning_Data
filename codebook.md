# Coursera - Getting and Cleaning Data - Course Project

## Source Data

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

A full description of the data used in the project is available at 
[The UCI Machine Learning Repository](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)


## Code description

The script creates a directory "UCI HAR Dataset", unzips there the raw data, and sets it as the working directory.
Then reads the folowing data files and assigns the varible names:
* activity_labels.txt
* features.txt
* subject_test.txt
* X_test.txt
* y_test.txt
* subject_train.txt
* X_train.txt
* y_train.txt

### 1. Merge the training and the test sets to create one data set.
Script merges all data files into one data set and removes the raw data from the memory.

### 2. Extracts only the measurements on the mean and standard deviation for each measurement. 
Search for text "mean" and "stdv" in "features" and subset data containing them.

### 3. Uses descriptive activity names to name the activities in the data set
Merge data subset with the  activity names table.

### 4. Appropriately labels the data set with descriptive variable names. 
Search and replace patterns to clean up the variable names.

### 5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
Extracts data with the average of each veriable for each activity and subject and creates new data set.
Writes the new data set in text file "tidy_data.txt" in the working directory.


## Output file

The dataset "tidy_data.txt" is the result of cleaning and subsetting data from the original data.
It contains 68 variables.
The first variable "Subject" denotes the subject number that performed an activity. In total there are 30 subjects.
The second variable "Activity" denotes the activity performed by the subject. There are six types of activity:
* WALKING
* WALKING_UPSTAIRS
* WALKING_DOWNSTAIRS
* SITTING
* STANDING
* LAYING

A total of 66 features (the estimated mean) were selected from the original data.
The full description of the features is available in the file "features_info.txt", included with the original dataset.
