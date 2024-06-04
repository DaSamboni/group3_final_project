# group3_final_project

Our dataset was obtained from Kaggle where we found a .csv file detailing films released from 1980 through 2020. Our goal was to explore movies across the decades and try to identify any trends in terms of what makes a movie “successful”. Our definition of success in this context comes down to the ratio between a film’s budget and its gross value; that being any film with a gross:budget ratio equal to or greater than 3:1 is considered a success for the purposes of this project.
Throughout our work we utilized Pandas, Tableau, PySpark, Spark SQL, and Google Colab to perform our analysis.
Attempt to build a model to predict future film success based off our dataset.
Our data arrived in one .csv file, making importation simple. We transformed the data by adding a column for each row’s gross:budget ratio, off of which we created a boolean column titled “Success” which read the ratio figures and filled in a pass or fail for each film.
Other ETL work includes reformatting the release date column so we could just pull the year of release for each movie, creating columns which display the average IMDB user ratings (1-10) for the director, main writer, and main star in each film, and dropping rows for films which did not reach the 1000 user rating threshold.

Algorithms Used: Random Forest, Neural Networks and K Nearest Neighbors 

Random Forest:
Based on the confusion matrix the high number of True Positives and True Negatives indicates that the model is performing well in identifying both successful and unsuccessful movies accurately. 
The model demonstrates strong predictive capabilities, but further optimization may be necessary to improve recall for successful movies and achieve even higher accuracy.

Neural Networks:
The accuracy score of  0.8980 implies that the model correctly classified around 89.80% of the movies in the test dataset. It indicates that the model is quite effective in distinguishing between successful and unsuccessful movies based on their features. The loss value of approximately 0.2830 reflects the average discrepancy between the model's predicted outcomes and the actual outcomes in the test dataset.

K Nearest Neighbors:

Upon review, the KNN model did not work particularly well for our dataset. While increasing the K value during testing brings the True Negative prediction score to near perfection, the True Positive outcome is almost always missed.
Essentially, the more nearest neighbors (K-value) we added, the more this model was predicting that every film would be unsuccessful.

Trend Analysis and Visualization:

The United States has the greatest financial influence on successful movies, and of those, the most popular genre being Action movies. This play a great role in the success and popularity of these types of movies.

Disney topped the average gross figures by a wide margin, especially in the PG-13 film bracket. We theorize that this is due to Disney having a rather limited history of producing films rated in the PG-13 bracket, but the Pirates of the Caribbean series strongly buffs their earnings there.

Limitations:
The Dataset. Although a lot of data. Lot of it needed no be clean:
For instance many null values/lack of numerical values, duplicates, and etc.
Data Set only went to 2020.
Revenue Source. Data only included revenue earned through the theaters/box office.
