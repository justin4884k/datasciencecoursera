The run_analysis.R gets the data and perform the required steps in the project decription.

1. Download the dataset
	Download the UCI HAR Dataset and extracts the folder
	
2. Assign variables to data
	Variable		Data
	features		feautures.txt
	activities		activity_labels.txt
	subject_test	subject_test.txt
	x_test			x_test.txt
	y_test			y_test.txt
	subject_train	subject_train.txt
	x_train			x_train.txt
	y_train			y_train.txt
	
3. Merge data
	Merges the training and testing data for x, y, and subject as X, Y, and Subject respectively and then merge all 3 datasets into merge_d
	
4. Extracts the mean and standard deviation for each measurement
	subset the merge_d and select subject, code and measurements
	
5. Descriptive activity names to activities in the data set.
	Change the code coumn in the tidydata with activities from the activity column
	
6. change labels where necessary in the tidydata
	old_name		new_name
	code			activities
	Acc				Accelerometer
	Gyro			Gyroscope
	BodyBody		Body
	Mag				Magnitude
	f				Frequency
	t				Time
	
7. Create an independent tidy data set w/ the average of each variable/activity and subject
	FinalData contains summrized tidydata with mean of each activity/subject by grouping subject and activity
	create FinalData.txt