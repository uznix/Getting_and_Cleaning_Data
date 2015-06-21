# Coursera - Getting and Cleaning Data - Course Project

The goal of the project is to collect, clean and prepare a tidy data that can be used for later analysis.
A full description of the data used in the project is available at 
[The UCI Machine Learning Repository](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)
To run the script you have to install the library "plyr".

## Running the project

To run the project:
1. Create a directory for the project.
2. Set it as the working directory in R, using setwd("path to the directory").
3. Download the raw data from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip to the working directory.
4. Download the script "run_analysis.R" to the working directory. 
5. Run the script, using source("run_analysis.R")

The script creates a directory "UCI HAR Dataset" with the raw data.
The output file "tidy_data.txt" with the mean values of all variables will be created in the working directory.
The information about the variables is available in the codebook.md file.
