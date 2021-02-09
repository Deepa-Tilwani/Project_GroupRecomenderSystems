# Group-movie-recommender-system

This is a group project. I had created this project with other two team members for my assignment submission.

We tried to implement a Group Recommender System based on the following paper:

http://www.sciencedirect.com/science/article/pii/S0020025516300196

In this project, we created a Recommender System based matrix factorization for a group of users.
In order to calculate user and movie factors, we first perform Stochastic Gradient Matrix Factorization based on the user-movie rating matrix.
We generate user groups of three different sizes. Small (3 members), medium (5 members) and large (10 members) and predict group ratings using the following methods.
1. After factorization: where we aggregate user factors into group factors after factorization.
2. Before Factorization(BF): where we assemble user ratings to a virtual user. We calculate group factors using simple ridge regression.
3. Weighted Before Factorization(WBF): Same as BF except that no. of movies watched by users are taken as weights. We solve it using weighted ridge regression method.
    
Finally we evaluate our project (getting roughly 80 % precision)


## Dataset used for this project can be downloaded from this link:
Dataset: https://grouplens.org/datasets/movielens/100k/


The notebook can be run directly on jupyter.

## Pre-requesites: 
We are using pandas, numpy, scipy and warnings modules. Install them by
running.
```
pip install numpy
pip install pandas
pip install scipy
```
The arguments are entered in the config.conf file that is present in the configuration file.
Same folder as well. Hyperparameters for matrix factorisation, group sizes, and
No. The generated groups can be changed in the config file.

