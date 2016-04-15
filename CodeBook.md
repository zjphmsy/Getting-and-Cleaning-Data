Source of the Data :

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Description of the Data :

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Data Set Information

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

The dataset includes the following files:

'README.txt'
'features_info.txt': Shows information about the variables used on the feature vector.
'features.txt': List of all features.
'activity_labels.txt': Links the class labels with their activity name.
'train/X_train.txt': Training set.
'train/y_train.txt': Training labels.
'test/X_test.txt': Test set.
'test/y_test.txt': Test labels.
After setting the source directory with setwd(), read into tables the data in the files and created :

SubjectTrain
SubjectTest
ActivityTrain
ActivityTest
DataTrain
DataTest

Step 1. Merges the training and the test sets to create one data set.

Merge Activity and Subject files by row binding and rename variables. Merge Data Training and Test files. Rename variables. Rename columns for Activity. Merge columns : created DataTable with cbind.

Step 2. Extracts only the measurements on the mean and standard deviation for each measurement.

Extract from Features file only mean and standard deviation : created DataFeaturesMeanStd. Add subject and activity number. Subset into DataTable.

Step 3. Uses descriptive activity names to name the activities in the data set.

Added activity names into DataTable. Created DataAggregate to sort activities.

Step 4. Appropriately labels the data set with descriptive variable names.

Used gsub to clean up data labels.

Step 5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

Created an independent tidy data set with write.table .
