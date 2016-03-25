# Getting-and-Cleaning-Data-project

This is the course project for the Getting and Cleaning Data Coursera course. The R script, run_analysis.R, does the following:


1. First it checks to see if the required "reshape2" has been installed and then loads the "reshape2" package.
2. Download the dataset if it does not already exist in the working directory
3. It then reads all required .txt files and labels the datasets
4. Consquently the appropriate "activity_id"'s and "subject_id"'s are appended to the "test" and the "training" data, which are then   combined into one single data frame.
5. Using the "grep" function, all the columns with mean() and std() values are extracted and then a new data frame, including only the "activity_id", the "subject_id" and the mean() and std() columns, is created.
6. Using the "merge" function, descriptive activity names are merged with the mean/std values dataset, to get one dataset with descriptive activity names.
7. Lastly, with the help of the "melt" and "dcast" functions of the "reshape2" package, the data is converted into a table containing mean values of all the included features, ordered by the activity name and the subject id, and the data is written to the "tidy_movement_data.txt" file.


A description of the "tidy_movement_data.txt" file may be found in the "CodeBook.md" file.
