# Airbnb-Boston
This repository contains the Jupyter notebook files used in analysis of Boston Airbnb data (publicly available [here](https://www.kaggle.com/datasets/airbnb/boston))

## Installations
The Anaconda distribution is required to run the code in this repository. All necessary libraries should come pre-installed with Anaconda. 
The version of python used for this investigation is Python 3.10.9. 

## Motivation
This investigation was conducted as part of the first project in the Udacity Data Science Nanodegree. I was interestested in using Boston Airbnb data from 2017 to understand:

1. Which numerical and categorical features correlate with rating score?
2. Does neighbourhood have a correlation with rating score and price? 
3. Can we find negative and positive reviews based on review comments alone?
4. How accurately can we predict rating score (without features which are clearly directly related)

## Files in this repository
There are 6 notebooks available here to showcase work related to the above questions:

### Question 1
- Project_1_categorical_features_analysis.ipynb
- Project_1_numerical_features_analysis.ipynb

### Question 2
- Project_1_neighbourhood_analysis.ipynb

### Question 3
- Project_1_generate_processed_reviews.ipynb
- Project_1_NLP_model.ipynb

### Question 4
- Project_1_complete_model.ipynb

## Description of files

### Project_1_numerical_features_analysis.ipynb
This code was used to determine which numerical features were correlated with the feature review_scores_rating. Correlated features were determined using a correlation matrix.

### Project_1_categorical_features_analysis.ipynb
This code was used to determine which categorical features were related with review_scores_rating. Violin plots were used to visualize differences in the distributions of review_scores_rating between each category.

### Project_1_neighbourhood_analysis.ipynb
Neighbourhood was analyzed separate to the other categorical variables. In this code, violin plots were used to visualize differences in the distribution of review_scores_rating and price between neighbourhoods, and one-way ANOVA used to verify these differences.

### Project_1_generate_processed_reviews.ipynb
In this project, a natural language processing approach was taken to find if reviews were negative or positive from the review comments. This code uses the CountVectorizer function of the scikit-learn library to convert review comments into a matrix of word counts. 

### Project_1_NLP_model.ipynb
This code uses the output generated by Project_1_generate_processed_reviews.ipynb to train a random forest classification model to classify reviews as bad (defined as <= 80, which corresponds to 10% quantile) or good (>80).

### Project_1_complete_model.ipynb
This code extends on Project_1_NLP_model.ipynb, taking in the other categorical and numerical features which were determined to be correlated with review_scores_rating and also using them to train the model. 

## Findings
The findings of this investigation are summarized here:

## Licensing, Authors, Acknowledgements
I would like to thank Airbnb for making this dataset public available. I would also like to thank Charles Rajendran, whose [code](https://medium.com/swlh/text-classification-using-the-bag-of-words-approach-with-nltk-and-scikit-learn-9a731e5c4e2f) I referenced to tokenize the review comments. 
