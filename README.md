# Airbnb-Boston
This repository contains the Jupyter notebook files used in analysis of Boston Airbnb data (publicly available [here](https://www.kaggle.com/datasets/airbnb/boston))

## Installations
The Anaconda distribution is required to run the code in this repository. 
The necessary libraries to run all the notebooks are: 
- pandas
- numpy
- seaborn
- scipy
- nltk
- scikit-learn
All necessary libraries should come pre-installed with Anaconda, but t may be necessary to download the stopwords and punkt nltk packages.
The version of python used for this investigation is Python 3.10.9. 

## Motivation
This investigation was conducted as part of the first project in the Udacity Data Science Nanodegree. I was interestested in using Boston Airbnb data from 2016-2017 to understand:

1. Which numerical or categorical features are correlated with rating score?
2. Does the rating score and price of a listing depend on the neighbourhood? 
3. Can we distinguish 'good' and 'bad' listings from just the review comments?

## Files in this repository
To gain a comprehensive understanding of this dataset and to answer all of the above questions, it was necessary to split the analysis into 4 different jupyter notebooks:

### Question 1
- Project_1_num_cat_features_analysis.ipynb

### Question 2
- Project_1_neighbourhood_analysis.ipynb

### Question 3
- Project_1_generate_processed_reviews.ipynb
- Project_1_NLP_model.ipynb

## Description of files

### Project_1_numerical_features_analysis.ipynb
This code was used to conduct exploratory data analysis of the listings dataset and to determine which numerical features were correlated with the feature review_scores_rating. Correlated numerical features were identified using a correlation matrix, and violin plots were used to visualize differences in the distributions of review_scores_rating across categorical variables.

### Project_1_neighbourhood_analysis.ipynb
Neighbourhood was analyzed separate to the other categorical variables. In this code, violin plots were used to visualize differences in the distribution of review_scores_rating and price between neighbourhoods, and one-way ANOVA used to verify these differences.

### Project_1_generate_processed_reviews.ipynb
In this project, a natural language processing approach was taken to find if reviews were negative or positive from the review comments. This code uses the CountVectorizer function of the scikit-learn library to convert review comments into a matrix of word counts. 

### Project_1_NLP_model.ipynb
This code uses the output generated by Project_1_generate_processed_reviews.ipynb to train a random forest classification model to classify listings as 'bad' (defined as having a review rating score <= 89, which corresponds to the 25% quantile) or good (review rating score > 89).

## Findings
The findings of this investigation are summarized in this [blog post]()

## Licensing, Authors, Acknowledgements
I would like to thank Airbnb for making this dataset public available. I would also like to acknowledge Charles Rajendran, whose [code](https://medium.com/swlh/text-classification-using-the-bag-of-words-approach-with-nltk-and-scikit-learn-9a731e5c4e2f) I referenced to tokenize the review comments. 
