# Final Project – Jithendra Seneviratne  

This project uses both the [Beer Recommender Data](https://snap.stanford.edu/data/web-BeerAdvocate.html) as well as the [Jester dataset](http://eigentaste.berkeley.edu/about.html) to run various models and evaluate their performance. We will use an AWS EC2 instance to gain the processing power needed to manipulate very large sparse matrices.

[See Model Selection work here](https://github.com/jitsen-design/CUNY_DATA_606_Submissions/blob/master/Data_612/Final_Project/final_model_selection.ipynb)

Let's also manufacture a user who likes stouts to see if the model can actually predict the user's taste!

We already know that the optimal number of weights for the Beer Advocate data is ten (see previous project [here](https://github.com/jitsen-design/CUNY_DATA_606_Submissions/blob/master/Data_612/Assignment_5/Assignment_5.ipynb)). As an additonal exercise, we'll use Apache Spark to evaluate the optimal number of training weights for the following datasets.

* Book Review Data [(From a previous exercise)](https://www.kaggle.com/philippsp/book-recommender-collaborative-filtering-shiny/data)
* Jester Dataset (Used in this exercise)

[See Spark work here](https://github.com/jitsen-design/CUNY_DATA_606_Submissions/blob/master/Data_612/Final_Project/final_spark.ipynb)

### Objectives:
*	Use cloud computing for efficiency 
*   Check sparsity of both datasets
*	Use different models in the Surprise package to decide ideal algorithm (using RMSE)
*	Compare model performance with levels of spartsity
*   Fabricate user (myself) and see predictions on my ratings (using different models)
*	Look at performance metrics other than RMSE by tuning the minimum number of ratings (manoipulating sparsity)
*	Additional exercise: Look at ideal number of weights for different datasets using Apache Spark


### Metrics Other Than RMSE

We'll explore ideas such as Personalization and Coverage below. Documentation for the [Recmetrics package](https://towardsdatascience.com/evaluation-metrics-for-recommender-systems-df56c6611093) suggest that maximizing personalization and coverage is desirable. 

#### Coverage
This is the % of recommendations the model can make on the testset. 

#### Personalization
This is the level of personalized recommendations the algorithm spits back. This might be of particular value to users, as unique and accurate recommendations are better than simply accuate recommendations.

#### Hyper-Parameter
We'll use the minimum number of ratings the user has provided as parameter and retrieve RMSE, Coverage and Personalization for different filtered models