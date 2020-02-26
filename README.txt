# Trip Activity Recommendation System
John Canque

- [Data](#data)
- [EDA](#eda)
- [Model](#model)
- [Final Recommendation System](#sys)
- [Futher Steps](#steps)


## Project Goals
The goal of this project is to help plan future trips with activities that you most enjoy at home. Looking at the most popular places is an approach, but getting something customized to activities that you like will make the trip enjoyable and memorable.


## Data Collection <a name='data'></a>
I used selenium and beautiful soup to scrape all activities for NYC and London from [Tripadvisor](https://www.tripadvisor.com/). I got the following information for each activity:
- Name
- Number of Reviews
- Ranking in City
- Address
- About section
- Up to 60 latest comments
- Suggested Duration

## EDA <a name='eda'></a>
### Data Cleaning
I used NLP 


### Data Exploration
As part of the data exploration, one of the more interesting things I found was the wide range of returns and risk. In a market where most prices have been correlated, I was surprised to see how many funds had performance and risk profiles that were more than 3 standard deviations away from the mean.


### Risk Predictions
As part of the EDA, I wanted to see if I can predict the risk (using Monthly Value at Risk) using the many features of each fund. I used Decision Trees, Random Forests, and Linear Regression to evaluate.


## Recommender Model <a name='model'></a>
I used NLP on the top 25 holdings of each fund to focus on the holdings with the most important frequencies(tf-idf). Then I vectorized into a matrix and added the matrix to my dataframe with the fund features. Finally I used cosine similarity to build the similarity matrix.
 

## Final Recommendation System <a name='sys'></a>
For the final recommender, the user inputs a mutual fund and will get the 10 most similar funds. The user can also filter using any of the features on the fund, ie. can look for cheapest funds in the Healthcare space while focusing on the risk metrics.

I built a front-end using streamlit - here is a look at how it works:

## Further Steps <a name='steps'></a>
- Put app live online
- Add functionality to take in descriptors as user input.
- Add business functionality:
  - Allow for fund families to create portfolios based on their funds based on user's specifications
  - Allow for clients to upload full portfolios to get recommendations
