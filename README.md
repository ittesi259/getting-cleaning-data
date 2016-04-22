This README file discusses the Getting and Cleaning Data Course Project

About the Anlysis files:
  The features are found unlabeled in the x_test.txt file.  Activity labels are found in the y_test.txt file and subject data is in the subject_test.txt file.
  
  The same format is true of the training data found in the x_train.txt, y_train.txt and subject_train.txt file.
  
About the script and the tidy dataset

I created a script called run_analysis.R that merges the test and training sets together. The script assumes the following:

The UCI HAR Dataset must be downloaded and unzipped.
The UCI HAR Dataset must be located in a directory called "UCI HAR Dataset"
After merging the testing and training data, labels are added  and only columns reporting mean values and standard deviation values are kept.

Finally, the script creates a tidy data set that is tab delineated containing the means of all the columns per test subject and per activity. This set is wriiten in the file tidy.txt in this repo

Please see the CodeBook.md file that explains transformations performed and the the resulting variables and data.
