---
title: "CodeBook"
output: html_document
Description: CodeBook.md will provide explanation on the variables, that is what the variables represent (eg the measure, etc).
---
Data Science Coursera - Getting and Cleaning Data: Course Project

### General Information about the Tidy Data
- Tidy data set is contained in a single text file (eg: "tidyData_AvgMeasuresByActivityAndSubject.txt").
- Tidy data set text file is created by the run_analysis.R script (see README.md for more info about "recipe").
- Text file consists of the average of each measurement variable for each activity and each subject.
- The measurement variables in text file are a range of measurements taken from sensor signals (accelerometer and gyroscope) in experiments, that specifically consist of those estimated using mean and standard deviation functions on the data. All other measured data was removed from final data set.
- Finally the data in text file uses variable and value names that are consistent with "tidy data good practices" convention.


### Tidy Data Set Variable Names
| ## |  Variable Names (column names) in Tidy Data Set
|----|:---------------------------------------------------------------------------
| 01 |   "activityname"
| 02 |	 "subjectidentifier"
| 03 |	 "timebodyaccelerometermeanvaluex"
| 04 |	 "timebodyaccelerometermeanvaluey"
| 05 |	 "timebodyaccelerometermeanvaluez"
| 06 |	 "timegravityaccelerometermeanvaluex"
| 07 |	 "timegravityaccelerometermeanvaluey"
| 08 |	 "timegravityaccelerometermeanvaluez"
| 09 |	 "timebodyaccelerometerjerkmeanvaluex"
| 10 |	 "timebodyaccelerometerjerkmeanvaluey"
| 11 |	 "timebodyaccelerometerjerkmeanvaluez"
| 12 |	 "timebodygyroscopemeanvaluex"
| 13 |	 "timebodygyroscopemeanvaluey"
| 14 |	 "timebodygyroscopemeanvaluez"
| 15 |	 "timebodygyroscopejerkmeanvaluex"
| 16 |	 "timebodygyroscopejerkmeanvaluey"
| 17 |	 "timebodygyroscopejerkmeanvaluez"
| 18 |	 "timebodyaccelerometermagnitudemeanvalue"
| 19 |	 "timegravityaccelerometermagnitudemeanvalue"
| 20 |	 "timebodyaccelerometerjerkmagnitudemeanvalue"
| 21 |	 "timebodygyroscopemagnitudemeanvalue"
| 22 |	 "timebodygyroscopejerkmagnitudemeanvalue"
| 23 |	 "frequencydomainsignalbodyaccelerometermeanvaluex"
| 24 |	 "frequencydomainsignalbodyaccelerometermeanvaluey"
| 25 |	 "frequencydomainsignalbodyaccelerometermeanvaluez"
| 26 |	 "frequencydomainsignalbodyaccelerometerjerkmeanvaluex"
| 27 |	 "frequencydomainsignalbodyaccelerometerjerkmeanvaluey"
| 28 |	 "frequencydomainsignalbodyaccelerometerjerkmeanvaluez"
| 29 |	 "frequencydomainsignalbodygyroscopemeanvaluex"
| 30 |	 "frequencydomainsignalbodygyroscopemeanvaluey"
| 31 |	 "frequencydomainsignalbodygyroscopemeanvaluez"
| 32 |	 "frequencydomainsignalbodyaccelerometermagnitudemeanvalue"
| 33 |	 "frequencydomainsignalbodybodyaccelerometerjerkmagnitudemeanvalue"
| 34 |	 "frequencydomainsignalbodybodygyroscopemagnitudemeanvalue"
| 35 |	 "frequencydomainsignalbodybodygyroscopejerkmagnitudemeanvalue"
| 36 |	 "timebodyaccelerometerstandarddeviationx"
| 37 |	 "timebodyaccelerometerstandarddeviationy"
| 38 |	 "timebodyaccelerometerstandarddeviationz"
| 39 |	 "timegravityaccelerometerstandarddeviationx"
| 40 |	 "timegravityaccelerometerstandarddeviationy"
| 41 |	 "timegravityaccelerometerstandarddeviationz"
| 42 |	 "timebodyaccelerometerjerkstandarddeviationx"
| 43 |	 "timebodyaccelerometerjerkstandarddeviationy"
| 44 |	 "timebodyaccelerometerjerkstandarddeviationz"
| 45 |	 "timebodygyroscopestandarddeviationx"
| 46 |	 "timebodygyroscopestandarddeviationy"
| 47 |	 "timebodygyroscopestandarddeviationz"
| 48 |	 "timebodygyroscopejerkstandarddeviationx"
| 49 |	 "timebodygyroscopejerkstandarddeviationy"
| 50 |	 "timebodygyroscopejerkstandarddeviationz"
| 51 |	 "timebodyaccelerometermagnitudestandarddeviation"
| 52 |	 "timegravityaccelerometermagnitudestandarddeviation"
| 53 |	 "timebodyaccelerometerjerkmagnitudestandarddeviation"
| 54 |	 "timebodygyroscopemagnitudestandarddeviation"
| 55 |	 "timebodygyroscopejerkmagnitudestandarddeviation"
| 56 |	 "frequencydomainsignalbodyaccelerometerstandarddeviationx"
| 57 |	 "frequencydomainsignalbodyaccelerometerstandarddeviationy"
| 58 |	 "frequencydomainsignalbodyaccelerometerstandarddeviationz"
| 59 |	 "frequencydomainsignalbodyaccelerometerjerkstandarddeviationx"
| 60 |	 "frequencydomainsignalbodyaccelerometerjerkstandarddeviationy"
| 61 |	 "frequencydomainsignalbodyaccelerometerjerkstandarddeviationz"
| 62 |	 "frequencydomainsignalbodygyroscopestandarddeviationx"
| 63 |	 "frequencydomainsignalbodygyroscopestandarddeviationy" 
| 64 |	 "frequencydomainsignalbodygyroscopestandarddeviationz"
| 65 |	 "frequencydomainsignalbodyaccelerometermagnitudestandarddeviation" 
| 66 |	 "frequencydomainsignalbodybodyaccelerometerjerkmagnitudestandarddeviation"
| 67 |	 "frequencydomainsignalbodybodygyroscopemagnitudestandarddeviation" 
| 68 |	 "frequencydomainsignalbodybodygyroscopejerkmagnitudestandarddeviation"


### Tidy Data Set Variable Descriptions
##### 1. "activityname"
- Name pf activity performed by people in study wearing a smartphone (Samsung Galaxy S II) on the waist.
- Values (8 in total): "WALKING", "WALKING_UPSTAIRS", "WALKING_DOWNSTAIRS", "SITTING, STANDING", "LAYING"

##### 2. "subjectidentifier"
- An identifier of the subject who carried out the experiment.
- Values (30 in total): range from 1 to 30 in interger increments. NOTE: No additional data was provided for the values that will allow more descriptive translation.

##### 3. thru 68. [All Measurement Variables]
- These are the measurement variables that represent the various triaxial acceleration from the **accelerometer** (total acceleration) and the estimated body acceleration as well as the triaxial angular velocity from the **gyroscope**. For both accelerometer and gyroscope measurements, there was a time and frequency domain variable as well as the 3-axial (x, y and z) components that are measured and appear in the tidy dataset.
- Values: The values are the calculated averages of all measurement data for each of the activities and subjects.
