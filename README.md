
## Reddit Social Media Analysis: Inflation Discourse


A data pipeline and analysis notebook that collects Reddit posts and comments about inflation from finance- and news-related subreddits, cleans the text, and applies NLP techniques (word frequency, sentiment analysis, and topic modeling) to explore how the topic is being discussed.

## Table of Contents
Overview
Requirements
Setup
Usage
Project Structure
Notes & Limitations
License
Overview

The notebook (social_media_Analysis.ipynb) walks through an end-to-end pipeline:

## Data collection 
Pulls up to 100 hot posts and 10,000 comments from target subreddits using the Reddit API (via PRAW).

## Filtering & sampling 
Reduces the raw dataset to a manageable sample (100 posts, up to 30 comments each) and saves it as JSON.

## Subreddit analysis 
Counts and visualizes how often posts/comments come from each target subreddit (economy, finance, personalfinance, CryptoCurrency, StockMarket, worldnews, news, politics).

## Text cleaning 
Lowercases, strips URLs/handles/hashtags/digits, tokenizes (via NLTK's TweetTokenizer), removes stopwords, and stems tokens (via PorterStemmer).

## Word frequency analysis 
Extracts top terms and generates a custom stopword list from the most common words in the dataset.

## Length analysis 
Visualizes the distribution of post/comment lengths with a boxplot.

## Sentiment analysis 
Scores comments using both VADER (nltk.sentiment) and TextBlob, classifying them as positive/neutral/negative and tracking sentiment over time.

## Time series analysis 
Plots daily and hourly posting/commenting activity over the last 30 days.

## Topic modeling 
Trains an LDA model (via gensim) on cleaned comments and renders a word cloud grid for each discovered topic.

## Requirements
Python 3.12 (or compatible 3.x)
A Reddit API application (client ID and secret) — see Reddit's app registration guide
