## This ReadMe file describes how the script "run_analysis.R" created to process data 
## on Human Activity Recognition Using Smartphones Dataset is working.

### Step1:Downloads "Human Activity Recognition Using Smartphones Dataset" from UCI Machine Learning Site.

### Step2:Reads TEST ("X_test.txt", "y_test.txt", "subject_test.txt") and TRAIN ("X_train.txt", 
### "y_train.txt", "subject_train.txt") Data sets into R.

### Step3:Merges TEST an TRAIN data into 3 data sets "X_test_train", "y_test_train"
### and "subject_test_train".

### Step4:Creates data set with only the variables on the mean and standard deviation. This by reading 
### "features.txt" data and creating a logical vector containg only mean and standard deviation descriptions.
### This vector is later on used to select only the needed variables with measurments from the "X_test_train".

### Step5:Creates the final "(un)tidy" dataset. This be merging "activity labels" with "y_test_train" data sets
### based on common id to correctly label all activities and name them accordingly. Name the columns of the
### "subject_test_train" and bind 3 data sets ("filtered_X_test_train" ,"y_test_train_activity_labeled",
### "subject_test_train") into one (data).

### Step6: Creates the final "tidy" data set
### Transforms the data from the wide into the long data set by applying the melt function by Activity &
### Subjects.Calculates means of every variable by applying dcast functin by Subject and Activity.
### Exports the recalculated "tidy" data into txt file.
