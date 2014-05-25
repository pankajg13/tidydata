## GETTING AND CLEANING DATA: COURSE PROJECT

# STEP 1: Merges the training and the test sets to create one data set.

* First getting the working directory
* Loading the data.table package into R
* Reading the file feature.txt from the .zip file provided during the project in to R using the read.table() function; from this we will get the variable names
* Reading the X_train.txt file in to R with the respective column names which are in feature.txt file
* Reading the X_test.txt file in to R with the respective column names which are in feature.txt file
* Combining both the X data (X_train and X_test) in to one matrix using rbind() function

* Reading the subject_train.txt file from the same .zip file using the read.table() function and assign the the column variable name to be Subject
* Reading the subject_ttest.txt file from the same .zip file using the read.table() function and assign the the column variable name to be Subject
* Combining both the subject data (subject_train and subject_test) in to one vector using the rbind() function

* Reading the Y_train.txt file in to R with the respective column names which are in feature.txt file
* Reading the Y_test.txt file in to R with the respective column names which are in feature.txt file
* Combining both the Y data (Y_train and Y_test) in to one matrix using rbind() function

* Combining all the three matrices in to one big matrix or table using the cbind() function forming the original data set.


# STEP 2: Extracts only the measurements on the mean and standard deviation for each measurement.

* Getting the columns with mean() variable for mean
* Getting the columns with std() variable for standard deviation
* Extracting the data with mean() and std() columns from the original data set


# STEP 3: Uses descriptive activity names to name the activities in the data set

* Changing to activity numeric value to activity labels provided in the same .zip file (one by one; didn't find the appropriate function, tried merge also but fails)


# STEP 4: Appropriately labels the data set with descriptive activity names.

* Appropriate labelling of data variables using the gsub() function


# STEP 5: Creates a second, independent tidy data set with the average of each variable for each activity and each subject.

* Used: Original data set for getting the tidy data
* Loading the reshape2 package into R
* Melting the data in to long data format using the melt() function
*Converting the long data set into wide data set using the dcast() function and using fun.aggregate = mean
* Writing the tidy data set in to text file using the write.table() function
* Displaying the output as a tidy data set.