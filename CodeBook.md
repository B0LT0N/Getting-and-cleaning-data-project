* This Code Book indicates all the variables and summaries calculated, along with units, and any other relevant information.

* Dataset downloaded and extracted under the folder called UCI HAR Dataset

* Variables:
  * features <- features.txt : The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ.
  * activities <- activity_labels.txt : List of activities performed when the corresponding measurements were taken and its codes (labels)
  * subject_test <- test/subject_test.txt : Contains test data of 9/30 volunteer test subjects being observed
  * x_test <- test/X_test.txt : Contains recorded features test data
  * y_test <- test/y_test.txt : Contains test data of activities code labels
  * subject_train <- test/subject_train.txt: Contains train data of 21/30 volunteer subjects being observed
  * x_train <- test/X_train.txt: Contains recorded features train data
  * y_train <- test/y_train.txt :contains train data of activities’code labels
  * X: is created by merging x_train and x_test using rbind() function
  * Y: is created by merging y_train and y_test using rbind() function
  * Subject: is created by merging subject_train and subject_test using rbind() function
  * MergedData: is created by merging Subject, Y and X using cbind() function
  * TidyData: is created by subsetting MergedData, selecting subject, code and the measurements on the mean and standard deviation for each measurement
<br/><br/>
* Labels the data set with descriptive variable names:
  * Code column in TidyData renamed into activities
  * Acc in column’s name replaced by Accelerometer
  * Gyro in column’s name replaced by Gyroscope
  * BodyBody in column’s name replaced by Body
  * Mag in column’s name replaced by Magnitude
  * ^f in column’s name replaced by Frequency
  * ^t in column’s name replaced by Time
<br/><br/>
* FinalData: is created by sumarizing TidyData taking the means of each variable for each activity and each subject, after groupped by subject and activity

* Export FinalData into FinalData.txt file.
