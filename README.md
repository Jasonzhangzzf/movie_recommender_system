# movie_recommender_system
## Introduction
This project implements retrieval and ranking models on the original movielens-100k dataset and provides a short demo of how to combine them together 
in a recommender system. It includes two preprocessing notebooks, two model notebooks, and a demo notebook.
<br><br>
The retrieval models use matrix factorization powered by neuralCF and sentence transfomer model on plot embedding similarity.
<br><br>
The ranking models include neuralCF, DSSM, Wide and Deep, and DeepFM.

## Notebook walkthrough
[Preprocessing_1_imdb.ipynb](https://github.com/Jasonzhangzzf/movie_recommender_system/blob/main/Preprocessing_1_imdb.ipynb)
Extracts movie related features from IMDb database and via sentence transformer, including Top2 casts, director, IMDb rating, plot summary, and plot embedding.

[Preprocessing_2_feature_engineering.ipynb](https://github.com/Jasonzhangzzf/movie_recommender_system/blob/main/Preprocessing_2_feature_engineering.ipynb)
Extracts new features from existing datasets, including Bucketizing zipcode, retrieving movie genres, and most importantly, constructing user and movie historical data by timesetamp.

[model_retrieval.ipynb](https://github.com/Jasonzhangzzf/movie_recommender_system/blob/main/model_retrieval.ipynb) Builds a neuralCF retrieval model.

[model_ranking.ipynb](https://github.com/Jasonzhangzzf/movie_recommender_system/blob/main/model_ranking.ipynb) Performs normalization, categorization, one-hot encoding, and embedding 
on numerical and categorical features. Builds neuralCF, DSSM, Wide and Deep, and DeepFM models. Provide an in-depth analysis of result.

[pipeline_demo.ipynb](https://github.com/Jasonzhangzzf/movie_recommender_system/blob/main/pipeline_demo.ipynb) Demos how to recommend movies to a user at a specific timestamp.
Constructs input dataset and pipeline for retrieval and ranking.
