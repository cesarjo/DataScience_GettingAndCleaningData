---
Title: "README"
Output: html_document
Description: README.md file will explain how the run_analysis.R script works. An overview on how script processes the data in order to obtain the tidy data output. 
---
Data Science Coursera - Getting and Cleaning Data: Course Project

### General Workflow
1. Download the raw dataset from [here](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip).
2. Extract all data (.txt) files to "UCI HAR Dataset" directory on the working directory.
3. Run the run_analysis.R script from working directory.
4. R script outputs the tidy dataset as a text file, created at the working directory when R script is finished running.
5. Refer to CodeBook.md file for the tidy dataset variable names and descriptions.


### Recipe to Get and Clean Raw Data (how the R script works)

#### 0. Read in all relevant datasets into R:
- Read txt files into R:
- In total 8 text files are used collect all the raw data for creating tidy dataset (see table below).

###### Text file datasets as corresponding to data.frame dimensions (in R) after read.table() operation:
|X) |  Text File Name              | Brief Description                      |Table Dimension|
|---|:-----------------------------|:---------------------------------------|--------------:|
|1) | 'features.txt'               | List of all features.                  |   561 x 2     |
|2) | 'activity_labels.txt'        | Links class labels with activity name. |   6 x 2       |
|3) | 'train/X_train.txt'          | Training set.                          |   7352 x 561  | 
|4) | 'train/y_train.txt'          | Training activity labels. 1 thru 6.    |   7352 x 1    |
|5) | 'train/subject_train.txt'    | Identifies training subject. 1-30.     |   2947 x 1    |
|6) | 'test/X_test.txt'            | Test set.                              |   2947 x 561  |
|7) | 'test/y_test.txt'            | Test activity labels. 1 thru 6.        |   2947 x 1    |
|8) | 'test/subject_test.txt'      | Identifies test subject. 1 thru 30.    |   2947 x 1    |


#### 1. Merge the training and the test sets to create one data set:
- Use features data to replace generic variable (column) names (eg V1, V2, etc) with actual feature name.
- Add variable name "ActivityLabel" to column name.
- Add vaiable name "SubjectIdentifier" to column name.
- Combine activity, subject and measurement data with column binding for EACH of training data and test data.
- Merge training data and test data with row binding.
- End up with a data.frame of all the merged data.

#### 2. Extract only the measurements on the mean and standard deviation for each measurement:
- Add both the activity and subject data to new columns before extracting data.
- Extract the data that matches (by column name) mean() and std() measurement data.
- End up with a data.frame of all extracted data.

#### 3. Use descriptive activity names to name the activities in the data set:
- Create vector to store all activity names with index corresponding to correct activity id.
- Replace all activity ids in data.frame activity column with the dscriptive activity name using vector.

#### 4. Appropriately label the data set with descriptive variable names: 
- Create a temp vector that holds all column names (next will update these names).
- Following transformations are applied to the variable names in temp vector:
 1) Convert names to lower case
 2) Replace dash "-" chars with <no space>.
 3) Replace "Acc" with "accelerometer".
 4) Replace "Gyro" with "gyroscope".
 5) Replace "Mag" with "magnitude".
 6) Replace "mean()" with "meanvalue".
 7) Replace "std()" with "standarddeviation".
 8) Replace "t" when first letter of name with "time".
 9) Replace "f" when first letter of name with "frequencydomainsignal".
 10) Replace "mergedData.ActivityLabel" with "activityname".
 11) Replace "mergedData.SubjectIdentifier" with "subjectidentifier".
- Overwrite data frame with new descriptive variable (column) names from vector.

#### 5. From the data set in step 4, create a second, independent tidy data set 
- Melt data in data.frame by id = activity and subject.
- Cast the melted data by activty and subject identifier, and calculating the average of each variable for activity and subject variations.
- Write the new tidy data table to a .txt file.

