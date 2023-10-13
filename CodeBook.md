This Code Book describes the variables, the data, and any transformations or work that you performed to clean up the data

## 1. Download The Data Set
  - Dataset downloaded and extracted under the folder called **UCI HAR Dataset**

## 2. Assign each data to variables 
  - features <- features.txt :561 rows, 2 columns
  - activities <- activities.txt :6 rows, 2 columns
  - subject_test <- test/subject_test.txt:2947 rows, 1 column
  - x_test <- test/X_test.txt :2947 rows, 1 column
  - y_test <- test/y_test :2497 rows, 1 column
  - subject_train <- train/subject_train.txt :7352 rows, 1 column
  - x_train <- train/X_train.txt :7352 rows, 561 column
  - y_train <- train/y_train.txt :7532 rows, 1 column

## 3. Merges training and test sets to create one set
  - X using **rbind**(X_train, X_test)
  - Y using **rbind**(y_train, y_test)
  - Subject using **rbind**(subject_train, subject_test)
  - Merged_Data using **cbind**(Subject, Y, X)

## 4. Extracts only mesurements on mean and standard deviation for each
  - **TidayData** by subsetting **Merged_Data** seleting only columns **subject**, **code** and measurements on **mean** and standard deviation for each measurement

## 5. Use descriptive activity names to name acitivites in data set
  - Numbers in **code** column of **TidyData** replaced with corresponding activity from second column of **activities**

## 6. Appropriately labels the data set with descriptive variable names
  - code in TidyData column renamed to activites
  - All Acc replaced by Accelerometer
  - All Gyro replaced by Gyroscope
  - All BodyBody replaced by Body
  - All Mag replaced by Magnitude
  - All start with character f replaced with Frequency
  - All start with character t replaced with Time

## 7. Data set in Step 4 creates an independent tidy data set with average variable for activity and subject
  - FinalData created by summarizing TidayData
  - Export FinalData into FinalData.txt file
