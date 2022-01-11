For part one, we can store the respective data in training and test data sets corresponding to "subject", "activity" and "features".
Then, we name the columns. The columns in the features data set can be named from the main data in "featureNames".
The data in "features","activity" and "subject" are merged and the complete data is now stored in "completeData".

For part two, we extract the column indices that have either mean or std in them and add activity and subject columns to the list and look at the dimension of "completeData".
We then create "extractedData" with the selected columns in "requiredColumns". And again, we look at the dimension of "requiredColumns".

For part three, the activity field in "extractedData" is originally of numeric type. We need to change its type to character so that it can accept activity names.
The activity names are taken from main data "activityLabels". We need to factor the activity variable, once the activity names are updated.

For part four, after examining the "extractedData", we replace the acronyms with their proper labels like:
> Accelerometer for "Acc"
> Magnitude for "Mag"
> Time for "t"
> Frequency for "f"
and so on.

Lastly, for part five, we set Subject as a factor variable.
We create "tidyData" as a data set with average for each activity and subject. Then, we order the enties in "tidyData" and write it into data file 'Tidy.txt' that contains the processed data.