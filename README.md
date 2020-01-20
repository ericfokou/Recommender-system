

# Recommender system
> This project provides an implementation of **user-based** and **item-based** Collaborative filtering algorithm from scratch.

Here we used the MovieLens movie ratings dataset: [https://grouplens.org/datasets/movielens/]([MovieLens]) .


## algorithms description

The code is organized in class with functions to perform transformations and operations: fit, predict, evaluate.

### 1. user-based recommendation algorithm

Details on our implementation:

* The parameters of the class are as follows:    
    * ratings: the rating matrix (userId, movieId, rating) - input data
    * movies: movies names - input data
    * tags: Users tags - input data
    * similarity = 'cosine' or 'distances'
    * List of the numbers of neighbors to be tested Ex: [5, 10, 50]. The parameter with the best result will be selected automatically
    * Size in percent of test data Ex 0.1 for 10%
    * score: Score to use for evaluating model on test data. "precision", "recall", "f1_score"
    * top_n: Number of videos to recommend
    
* Predictions are made using the following formula:

    <img src="https://github.com/ericfokou/Recommender-system/blob/master/Images/Capture.PNG">
    
    avec:

		u: the user to whom we should recommend videos
		i: the video to recommend
		s (u, i): the calculated recommendation score
		W_uv: the similarity between user u and v
		r_u: the average score of user u
		r_vi: user rating v on video i
    
### 2.  item-based  recommendation algorithm

Details on our implementation:

* The parameters of the class are as follows:  

	 * ratings: the rating matrix (userId, movieId, rating) - input data
	 * movies: movies names - input data
	 * tags: Users tags - input data
	 * similarity = 'cosine' or 'distances'
	 * List of the numbers of neighbors to be tested Ex: [5, 10, 50]. The parameter with the best result will be selected automatically
	 * Size in percent of test data Ex 0.1 for 10%
	 * score: Score to use for evaluating model on test data. "precision", "recall", "f1_score"
	 * top_n: Number of videos to recommend


* Predictions are made using the following formula:

    <img src="https://github.com/ericfokou/Recommender-system/blob/master/Images/Capture1.PNG">
    
    avec:

         u: the user to whom we should recommend videos
         i: the video to recommend
         N (i, u): videos similar to videos i among videos rated by u
         s (u, i): the calculated recommendation score
         W_ij: the similarity between videos i and j
         r_j: the average of the notes of the video j
         r_ui: user rating u on video i
     
 

## Requirement

- Python 3.7.1
- numpy 1.16.4
- pandas 0.24.2
- matplotlib 1.16.4
- sklearn 0.22.1


## Usage example

launch Jupyter notebook into terminal:

    $ jupyter notebook

Then open notebook [Notebook.ipynb]([https://github.com/ericfokou/Recommender-system/blob/master/Notebook.ipynb])

## Release History

* 0.0.dev0
    * First development  release 

## Questions?

If you find a bug, feel free to write me [fokoub@gmail.com](mailto:fokoub@gmail.com).

## Contributing

Fork it:

	$ git clone https://github.com/ericfokou/Recommender-system

Then create your feature branch and commit your changes.

## Support

Eric FOKOU 

- email: [fokoub@gmail.com](mailto:fokoub@gmail.com)
- Twitter: <a href="http://twitter.com/fokou_eric" target="_blank">`@fokou_eric`</a>



