# Anime_Recommendation

Files this repo contains:
- [EDA Notebook](https://github.com/armantavanaa/Anime_Recommendation/blob/main/lawrence_eda.ipynb)
- [Model](https://github.com/armantavanaa/Anime_Recommendation/blob/main/model.py)
- [Presentation slides](https://github.com/armantavanaa/Anime_Recommendation/blob/main/Final_Presentation.pdf)
- [Main](https://github.com/armantavanaa/Anime_Recommendation/blob/main/main.py)
- [Util](https://github.com/armantavanaa/Anime_Recommendation/blob/main/utils.py)

## Description

In this project we developed Self-Attentive Sequential Recommendation system that would recommend animes to users based on their history. We then found the closest animes to each other by finding the distance between them. Lastly, we predicted the top n animes for users.

## Goal:

- Our main goal was to build a Self-Attentive Sequential Recommendation system by using self-attention based sequential model (SASrec)
- Learn how Animes are similar to each other
- Apply multihead attention to sequence of animes
- Pass through feedforward network to predict top n animes 
- Use various deep learning techniques
  - Dropout
  - Layer normalization
  - Cyclical learning rates
  

### Sequential Recommendation

We decided to build a sequential recommendation over a simple recommendation to take into account recency as it is very important since a lot of users' taste changes over time. So, this technique would allow us to better recommend animes to users.

<img size='200px' src="/images/rec_seq.png" alt="Employee data" title="Employee Data title">


## EDA:

We found a lot of missing users and items in the dataset after performing EDA for which we had to solve in order for our model to run.

## Model

- Try to capture the ‘context’ of user activities based on actions they have performed in the past
- Two current approaches
  - Markov Chains: Predicts a user’s next actions based on last actions
  - RNN: Predict using longer-term semantics
- SASRec balances these two approaches 
  - Capture long term semantics
  - Use an attention mechanism to predict using relatively few actions
    - Only predict using ‘relevant’ items from a user’s history

