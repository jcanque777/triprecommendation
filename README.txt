Trip Recommendation System README

# TripAdvisor Recommendation
John Canque

- [Data](#data)
- [EDA](#eda)
- [Model](#model)
- [Final Recommendation System](#sys)
- [Futher Steps](#steps)

## Project Goals
The goal of this project is to make it easier to plan trips to cities that one is not aware of. Planning vacations can be such a fun activity, but sometimes a little help is appreciated. You are given a couple recommended activities based on activities that you like in NYC.

## Data Collection <a name='data'></a>
I used selenium and beautiful soup to scrape Things To Do from [TripAdvisor]([https://www.tripadvisor.com/](https://www.tripadvisor.com/)). I got the following information for each activity:
- Name
- Number of Reviews
- Average Review
- Ranking in City
- Address
- Certificate of Excellence Award
- Up to the last 60 comments
- Stock Market Capitalization
- and 5 other variables

## EDA <a name='eda'></a>
### Data Cleaning
I chose to drop activities that were missing reviews.  Since TripAdvisor is a global website, I only kept English words. In the future, I would include in my scrape a function to automatically translate words. 

### Data Exploration

### Risk Predictions

## Recommender Model <a name='model'></a>
I used NLP on the top 25 holdings of each fund to focus on the holdings with the most important frequencies(tf-idf). Then I vectorized into a matrix and added the matrix to my dataframe with the activity characteristics. Finally I used cosine similarity to build the similarity matrix.
 

## Final Recommendation System <a name='sys'></a>
For the final recommender, the user inputs a NYC activity and will get the 10 most similar funds. The user can also filter using any of the features on the activity, ie. can look for rankings, certificate of excellence.

I built a front-end using streamlit - here is a look at how it works:

## Further Steps <a name='steps'></a>
- Put app live online
- Add functionality to take in descriptors as user input.
