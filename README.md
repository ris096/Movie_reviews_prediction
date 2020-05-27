# Movie reviews prediction
The objective of this project is to predict how a user will rate a movie they haven't watched based on how they've rated other movies  
The dataset used to create this model is the [MovieLens 100k dataset](https://grouplens.org/datasets/movielens/100k/) by Grouplens  

## My approach
I have used a collaborative filtering model as a basis for my predictive model, where I created an embedding matrix of size 40 for each user as well as movie, and trained the embedding weights using Stochastic Gradient Descent. The learning rate finder method of fastai library was used to determine the optimal learning rate. To implement learning rate annealing, one-cycle-learning method was used, which uses a different learning rate for each mini-batch. The shape of the learning rate v/s mini-batch # is an 'inverted-U', with the maximum learning rate being determined from the learning rate finder tool

## Final performance  
The model has a MSE of 0.81
