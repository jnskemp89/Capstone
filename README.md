### Capstone Project: Classification of Steam User Reviews

#### Question                                                      
Given the title of a game, text of a review, overall sentiment (positive or negative), and a count of how many other users found the review helpful, can I train a model to predict the title of a game given the contents of an incoming review?

#### Data
Using python code found from https://github.com/aesuli/steam-crawler, I scraped user reviews from the Steam website (letting the script run for several days before interrupting). Once the data was read in, I decided to parse down to the top 10 most reviewed games represented in order to aid my model with being able to categorize properly. This also helped to normalize the number of reviews for each game, as they varied from 1 review to almost 88,000.

![screenshot_percentage](https://user-images.githubusercontent.com/42395482/57573579-92df5a80-73ef-11e9-8936-58e3131963e9.png)

The resulting dataframe gives the game title and review text, along with several other rows that were not used. 

![screenshot_dataframe](https://user-images.githubusercontent.com/42395482/57573578-92df5a80-73ef-11e9-9571-9e7467f86d22.png)

Basic preprocessing was done for the review texts, including:
* Removing blank reviews
* Removing non-alpha
* Forcing lowercase
* Removing stopwords (the, is, at, which, on, etc.)

