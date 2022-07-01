# Anime_Recommendation

Files this repo contains:
- [EDA Notebook](https://github.com/armantavanaa/Anime_Recommendation/blob/main/lawrence_eda.ipynb)
- [Model](https://github.com/armantavanaa/Anime_Recommendation/blob/main/model.py)
- [Presentation slides](https://github.com/armantavanaa/Anime_Recommendation/blob/main/Final_Presentation.pdf)
- [Main](https://github.com/armantavanaa/Anime_Recommendation/blob/main/main.py)
- [Util](https://github.com/armantavanaa/Anime_Recommendation/blob/main/utils.py)

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


![foxdemo](https://www.semanticscholar.org/paper/Fusing-Similarity-Models-with-Markov-Chains-for-He-McAuley/fea7e2bcbe852bcb33ce70a4d57664e954f0e82a)

## EDA:

We found a lot of missing users and items in the dataset after performing EDA for which we had to solve in order for our model to run.
