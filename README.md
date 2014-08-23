Clean Data Project
==================

Course Project for Getting and Cleaning Data at Coursea/Johns Hopkins

For this data set I begin with the information in the train directory. I subset X_train based on the columns needed (which were specificed as the mean/mean() and standard deviation/std() columns. This left me with 68 columns instead of 561. 

I then applied the activity labels (as opposed to the numbers 1-6) to that subset. To finish this folder I used cbind to join all the bits of data together. 

I repeated this exact process for the test folder. 

Once that was accomplished I used rbind to join the data from the test and train folders together. 

At this point I used the features.txt file to create column labels for the joined data frame. 

Next was the aggregate() function to group by Subject and Activity and get the mean/average for each Subject's readings for that Activity label. I ordered this aggregated data frame by Subject and then Activity. 

The last code I included was the write.table() function which produces "results.txt" that contains my tidy data set. 

