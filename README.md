# 3rd-Capstone
# Objective
The goal of this project is to create a classification system for movies. There are many movies with a myriad of genres. However, a movie does not have one genre since it can be an action and sci-fi or just be an action movie. Thus, classifying movies to fit them neatly into one category isn't easy. Because of the variety of genres and sometimes new genres being created, categorizing movies can be an arduous task. Thus this project was done to facilitate the work and make it easier.

# Target Audience and Why
The target audiences could be an archivist or new streaming companies that want to categorize their movie correction way. Streaming services are expanding and sorting through different genres for audiences or searching for one is an important task.

# The Data
This dataset was chosen as it was the most numerous. 
 IMDB while does contain many movies, but the summary on it was too short to be used.
-         Kaggle
 
# Data Cleaning
In this classification system, the output is the genre. Thus, it is important to distinguish what genre each movie contains. In addition, many movies contain unnecessary words and names that are only useful in limited scope.
The first problem was the genre was, while looking like a list, a string. Because of this, the machine understood each genre as a long text and couldn’t separate different genres. As a solution, the strings had to be converted to a list.
The second problem was making sure to track what genre each movie contained. Since a movie could have multiple genres or be singular, I had to make sure to track them properly. The solution, create a dummy variable so tracking each genre would be quite simple.
The third issue was certain overviews containing too many unnecessary words, mostly proper nouns. The solution was going through each overview and eliminating compound words like “won’t “ or “can’t”. And utilizing nltk’s tagging, I was able to tag words that contain NNP and get rid of them.

# EDA

For EDA I went through many different factors that could lead to predicting movie genres, such as the length of the movie summary for each genre or the connection between each genre. However, these connections were loose and didn’t amount to anything.
![image](https://user-images.githubusercontent.com/43226667/208692194-0a2dda8c-ce46-4119-96b8-092318c3bba5.png)
![image](https://user-images.githubusercontent.com/43226667/208692314-3fae070e-7a5d-4d07-81fa-59c9c8545e50.png)




Another thing I explored was looking at each movie genre and which one was the most numerous.
Finally, I went through each movie genre to see which words would be numerous and see if it was usable, using a word cloud.



# Modeling
For modeling, I used MultiLabelBinarizera the output wouldn’t just be one. Since there was more than one label, LabelGinarizer couldn’t be used.
In addition, I had to cut down the genre to three most numerous ones, drama, action, and comedy. The reason being, the data wasn’t enough as each summary was too short and there weren’t enough movies.


# Counter vs TF ID

For the vectorizer, Counter led to better results overall by a bit, except for KNN. Perhaps because of how short each summary was; thus the number of words had more weight.
![image](https://user-images.githubusercontent.com/43226667/208692362-f70561e2-b2ee-41e5-8412-35ebad645d8d.png)




# Improvements
I felt that overall data was lacking and I would like to use additional data or a longer summary. The longer summary could have given TFIDF more weight, allowing more accurate results. The fact that for accuracy, genres had to be limited is the area that could be improved the most. 
