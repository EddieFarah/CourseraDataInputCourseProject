Data Source
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Files included

CodeBook.md -- codebook describing variables, the data and transformations
run_analysis.R -- actual R code

Step 1:

Read all the test and training files: y_test.txt, subject_test.txt and X_test.txt.
Combine the files to a data frame in the form of subjects, labels, the rest of the data.
Step 2:

Read the features from features.txt and filter it to only leave features that are either means ("mean()") or standard deviations ("std()"). The reason for leaving out meanFreq() is that the goal for this step is to only include means and standard deviations of measurements, of which meanFreq() is neither.
A new data frame is then created that includes subjects, labels and the described features.
Step 3:

Read the activity labels from activity_labels.txt and replace the numbers with the text.
Step 4:

Make a column list (includig "subjects" and "label" at the start)
Tidy-fy the list by removing all non-alphanumeric characters and converting the result to lowercase
Apply the now-good-columnnames to the data frame
Step 5:

Create a new data frame by finding the mean for each combination of subject and label. It's done by aggregate() function
Final step:

Write the new tidy set into a text file called tidy2.txt, formatted similarly to the original files.
