# Medical-Appointment-No-Shows-Data-Investigation
Doing independent data analysis project investigating Medical Appointment No Shows data set (on Kaggle)
Data set can be found here: https://www.kaggle.com/joniarroba/noshowappointments/discussion/38330#latest-288579

With this project I am going to create some defined functions to more efficiently re-use code in the future to analyze data.

This seems to be a difficult data set.  The best fitting model so far is K-nearest neighbours when using PCA to reduce down to 1 component:

For K-Nearest Neighbours with PCA

The best parameter choice is:  {'kneighborsclassifier__n_neighbors': 10, 'pca__n_components': 1}

The best score is: 0.791

CV accuracy: 0.789 +/- 0.002

Test accuracy: 0.791

This most likely suggests that most of the data points are not helpful at deciding whether or not someone will show up to an appointment (which is still interesting).  My next step will be to look at the basic statistics of the data.


I have recently discovered that the data was updated or that there was a separate file with more data on Kaggle.  The new coding file will have a 2 at the end of its name.  The data now has more features, and the data set is larger (close to 300,000 after deleting outliers).

For now my best result is:
For K-Nearest Neighbours with PCA
The best parameter choice is:  {'kneighborsclassifier__n_neighbors': 9, 'pca__n_components': 7}
The best score is: 0.664
CV accuracy: 0.665 +/- 0.002
Test accuracy: 0.667

It is interesting how despite there being more data that there is such a difference in a result from the last data set.  I am unsure why this might be, but regardless I am going to treat this as the actual data set from now on.  More to come soon.
