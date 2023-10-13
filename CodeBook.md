This Code Book describes the variables, the data, and any transformations or work that you performed to clean up the data

## Download The Data Set
  - Dataset downloaded and extracted under the folder called 'UCI HAR Dataset'

## Assign each data to variables 
  - 'features' <- 'features.txt' :561 rows, 2 columns
  - 'activities' <- 'activities.txt' :6 rows, 2 columns
  - 'subject_test' <- 'test/subject_test.txt':2947 rows, 1 column
  - 'x_test' <- 'test/X_test.txt' :2947 rows, 1 column
  - 'y_test' <- 'test/y_test' :2497 rows, 1 column
  - 'subject_train' <- 'train/subject_train.txt' :7352 rows, 1 column
  - 'x_train' <- 'train/X_train.txt' :7352 rows, 561 column
  - 'y_train' <- 'train/y_train.txt' :7532 rows, 1 column

## Merges training and test sets to create one set
  - 'X' using **rbind**('X_train', 'X_test')
  - 'Y' using **rbind**('y_train', 'y_test')
  - 'Subject' using **rbind**('subject_train', 'subject_test')
  - 'Merged_Data' using **cbind**('Subject', 'Y', 'X')
