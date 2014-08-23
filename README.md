Clean Data Project
==================

Course Project for Getting and Cleaning Data at Coursea/Johns Hopkins

To utilize the run_analysis.R file you simply need to load it (or copy it) into the working directory containing the Samsung data. If you load it, open the file, check "source on save" and save the file. The "results.txt" file will appear in your file list after a few moments. If you copy the code into R Studio and just hit enter you will also have the "results.txt" file. 

With either approach you will also have all the data frames I created a long the way to ultimately make the results data frame. 

******************************

For this data set I begin with the information in the train directory. I subset X_train based on the columns needed (which were specified as the mean/mean() and standard deviation/std() columns. This left me with 66 (68 in the end - including Subject and Activity) columns instead of 561. 

I then applied the activity labels (as opposed to the numbers 1-6) to that subset. To finish this folder I used cbind to join all the bits of data together. 

I repeated this exact process for the test folder. 

Once that was accomplished I used rbind to join the data from the test and train folders together. 

At this point I used the features.txt file to create column labels for the joined data frame. 

Next was the aggregate() function to group by Subject and Activity and get the mean/average for each Subject's readings for that Activity label. I ordered this aggregated data frame by Subject and then Activity. 

The last code I included was the write.table() function which produces "results.txt" that contains my tidy data set. 

