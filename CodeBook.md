CodeBook for the Course Project for Getting and Cleaning Data on Coursera
===========

The goals of this document are to provide information about the variables (including units!) in the tidy data set, summaries calculations and any other relevant information.

###  Variables and units

id: identifies the subject who performed the activity for each window sample. Its range is from 1 to 30.

ActivityLabel: activity name (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING)

ActivityCode: activity class (1, 2, 3, 4, 5, 6) labels with corresponds to ActivityLabel

For the following columns a complete description is given:

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

tBodyAcc-XYZ (units:  'g' gravity units)
tGravityAcc-XYZ (units:  'g' gravity units)
tBodyAccJerk-XYZ (units:  'g' gravity units)
tBodyGyro-XYZ (units: radians/second)
tBodyGyroJerk-XYZ (units: radians/second)
tBodyAccMag (units:  'g' gravity units)
tGravityAccMag (units:  'g' gravity units)
tBodyAccJerkMag (units:  'g' gravity units)
tBodyGyroMag (units: radians/second)
tBodyGyroJerkMag (units: radians/second)
fBodyAcc-XYZ (units:  'g' gravity units)
fBodyAccJerk-XYZ (units:  'g' gravity units)
fBodyGyro-XYZ (units: radians/second)
fBodyAccMag (units:  'g' gravity units)
fBodyAccJerkMag (units:  'g' gravity units)
fBodyGyroMag (units: radians/second)
fBodyGyroJerkMag (units: radians/second)

The set of variables that were estimated from these signals are: 

mean(): Mean of the mean of each variable for each activity for both test and train data
std(): Mean of the standard deviation of each variable for each activity for both test and train data

The tidy data sets contains only means of measurement for each activity for both test and train data for each subject.


### Summary of how the data were tidied

Please read the comments in the script ('run_analysis.R') for step-by-step explanations.

The main manipulations which were applied to the data are summarized here: 

1. Added 'id', 'ActivityCode', 'ActivityLabel' and 'settype' (test vs train) to the data set
1. Merged the training and the test sets to create one data set.
1. Extracted only the measurements on the mean and standard deviation for each measurement. 
1. Created a new data set with the average of each variable for each activity and each subject.



