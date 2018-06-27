# Medical-Appointment-No-Shows-Data-Investigation
Doing independent data analysis project investigating Medical Appointment No Shows data set (on Kaggle)
Data set can be found here: https://www.kaggle.com/joniarroba/noshowappointments/discussion/38330#latest-288579

With this project I am going to create some defined functions to more efficiently re-use code in the future to analyze data.

I have recently discovered that the data was updated or that there was a separate file with more data on Kaggle.  The new coding file will have a 2 at the end of its name.  The data now has more features, and the data set is larger (close to 300,000 after deleting outliers).

For now my results are:
For K-Nearest Neighbours with PCA
The best parameter choice is:  {'kneighborsclassifier__n_neighbors': 9, 'pca__n_components': 7}
The best score is: 0.664
CV accuracy: 0.665 +/- 0.002
Test accuracy: 0.667

For Random Forest
The best parameter choice is:  {'criterion': 'entropy', 'max_depth': 7, 'max_features': 'auto', 'n_estimators': 5}
The best score is: 0.698
CV accuracy: 0.698 +/- 0.000
Test accuracy: 0.698

Feature importance based on random forest voting can be seen in the figure below.

![alt text](https://github.com/bgoodman90/Medical-Appointment-No-Shows-Data-Investigation/blob/master/NoShowFeatureImportance.png)
