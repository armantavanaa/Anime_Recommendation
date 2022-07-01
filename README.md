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

## Hyperparameter Tuning

Here is our final hyperparameters that improved our model the best.

- Batch_size = 128
- Dropout_rate = 0.5
- hidden_units = 50
- Inference_only = False
- L2_emb = 0.0
- Lr = 0.001
- Maxlen = 50
- N_users = 100000
- Num_blocks = 2
- Num_epochs = 50
- Num_heads = 1

## Result

We were able to achieve:

- Test Hit Rate @ k=10: 0.89252

- NDCG @ k=10(Normalized Discounted Cumulative Gain): 0.99495

As an example we chose Shingeki no Kyojin (Attack on Titan) for our model to predict the top n (10) closest animes to it. Here is the list of closet animes to Attack on Titan we got.

- Please find the full list [here](https://github.com/armantavanaa/Anime_Recommendation/blob/main/lawrence_eda.ipynb)

<img size='200px' src="/images/result.png" alt="Employee data" title="Employee Data title">

