# BrainStation-Capstone


## Introduction

  IMDb is a website that contains information on thousands of movies and shows that have been released over the years. Each movie or show has its own description and genre to go along with it. Through the perspective of someone who make’s their own movie or show, you would want to adequately create a description that captures the genre of your work. The importance of this subject matter is that if a movie’s genre is labeled appropriately, it would gain the attraction of viewers who are interested in that particular genre. However, if a movie is labeled inappropriately, it may throw off a viewer who watches a movie thinking its of a particular genre, but instead was something that they are not interested in. Predicting the genre of a movie/show using the description is the core of the problem that I will be trying to solve in this project.
  
## Description of this Repository

### Environment Requirements
In this folder, you will find a .yml file that contains the required environment in order to run all of the notebooks successfully.

### Visualizations
In this folder, there are a some samples of visualizations taken from some of the notebooks.

### Data
This folder contains the original data taken from [Kaggle](https://www.kaggle.com/datasets/hijest/genre-classification-dataset-imdb), as well as the processed data, and the training and testing I created for the modeling process.

### Models
This folder contains just one file, which is the best performing model I created in notebook 3.1.

### 1) Cleaning & EDA
This notebook contains the first layer of cleaning and preprocessing the data, as well as creating visualizations such as the distribution of the data, and how many times a genre appears in the data.

### 2) Data Preprocessing
In this notebook, I dive further preprocessing the data by removing stopwords, vectorizing the data, and gaining more insights from creating visualizations like the chart below. This chart here shows the most weighted tokens in the genre of `documentary`

<img src="https://github.com/andrew-alarcon17/BrainStation-Capstone/blob/master/Visualizations/TFIDF.png" width="500">

### 3.1) Logistic Regression
This notebook goes through the first round of Logistic Regression modeling, where I make a model with optimal hyper parameters using Grid Search, and a model with reduced dimensions of the data set using Principal Component Analysis.

### 3.2) Logistic Regression 2
In this notebook, I rerun the Logistic Regression PCA model using a dataset that excludes 3 genres. These genres were `game show`, `war`, and `news`, and they were dropped because they lacked enough data entries. I wanted to experiment to see if this new model would perform better than the models made in the previous notebook.

### 4) Random Forest
This notebook focuses on constructing and optimizing a Random Forest Classifier to predict the genre of a data entry.

### 5) Best Model
This notebook goes on to recreate the best performing model and pickling it to be used for production.

## Conclusion & Next Steps

In this report, I documented the steps I took in order to run machine learning models to classify the genres of movies based off of their descriptions. I cleaned and preprocessed the data by removing any unwanted stop words and punctuation, and vectorized the data with the TF-IDF Vectorizer to gather the most relevant words in the dataset. My final model ended up being a Logistic Regression model that had a training accuracy of 51.5% and a testing accuracy of around 49.9%.

There are a few possible next steps after this project is finished. One would be to deploy this model onto a web app using Flask and Heroku that allows anyone to enter a movie/show description and have it classified using this Logistic Regression model. Another possible step would be to create an even better model using Recurrent Neural Networks via GPT3 and OpenAI. This model would then be used for production on a web app like how I mentioned previously.
