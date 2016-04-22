Getting and Cleaning Data Course Project CodeBook - Randy Proctor

Data Set Description (Provided by UCI Machine Learning Repository)
  The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

  The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

  Attribute Information

  For each record in the dataset it is provided:

  Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
  Triaxial Angular velocity from the gyroscope.
  A 561-feature vector with time and frequency domain variables.
  Its activity label.
  An identifier of the subject who carried out the experiment.
  
Requirement 1. Merge the training and the test together

After setting the source directory for the files, read into tables the data located in

features.txt
activity_labels.txt
subject_train.txt
x_train.txt
y_train.txt
subject_test.txt
x_test.txt
y_test.txt

I assigned column names and created one set merging first the testing files and training files, then merging together the 2 datasets that I had made

Requirement 2. Extract only the measurements on the mean and standard deviation for each measurement.
Created a logcal vector that contains TRUE values for the ID, mean and stdev columns and FALSE values for the others. Subset this data to keep only the necessary columns.

Requirement 3
Use descriptive activity names to name the activities of the data set
I merged the data subset with the activityType table to include the descriptive names

Requirement 4
Appropriately label the data set with descriptive activity names
I used the gsub function to clean up the labels to be more tidy.

Requirement 5.  Create a second, independant tidy set with average of each variable for each activity and subject
Per the project instructions, we need to produce only a data set with the average of each veriable for each activity and subject


Variable Explanations:
The following variables result in the tidy.txt Output:
Please note the Mean and StdDev were taken for each variable and is designated as such in the format <variable>Mean or variable<StdDev>
For conciseness I will only list each measurement once.

Activity ID - The ID Number of the Activity
subjectID - ID number of the subject
timeBodyAccMagnitude
timeGravityAccMagnitude
timeBodyAccJerkMagnitude
timeBodyGyroMagnitude
timeBodyGyroJerkMagnitude
freqBodyAccMagnitude
freqBodyAccJerkMagnitude
freqGyroMagnitude
freqBodyGyroJerkMagnitude
activityType
