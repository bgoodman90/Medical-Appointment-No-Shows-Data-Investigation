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
