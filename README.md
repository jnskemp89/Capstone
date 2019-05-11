### Capstone Project: Classification of Steam User Reviews

#### Question                                                      
Given the title of a game, text of a review, overall sentiment (positive or negative), and a count of how many other users found the review helpful, can I train a model to predict the title of a game given the contents of an incoming review?

#### Data
Using python code found from https://github.com/aesuli/steam-crawler, I scraped user reviews from the Steam website (letting the script run for several days before interrupting). Once the data was read in, I decided to parse down to the top 10 most reviewed games represented in order to aid my model with being able to categorize properly. This also helped to normalize the number of reviews for each game, as they varied from 1 review to almost 88,000.

![Screenshot](./screenshot_percentage.png)

The resulting dataframe gives the game title and review text, along with several other rows that were not used. 

![Screenshot](./screenshot_dataframe.png)

