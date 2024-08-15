# Sentiment Analysis with LSTM on IMDB Movie Reviews

## Overview

This project demonstrates the use of a Long Short-Term Memory (LSTM) neural network to perform sentiment analysis on the IMDB movie review dataset. The goal of this project is to predict whether a movie review is positive or negative based on its text content.

## Project Structure

- `imdb_sentiment_analysis.ipynb`: The main Python script that loads the IMDB dataset, preprocesses the data, builds the LSTM model, trains it, and evaluates its performance.
- `README.md`: Project documentation (this file).

## Model Architecture

The model consists of the following layers:

1. **Embedding Layer**: Converts word indices into dense vectors of fixed size.
2. **LSTM Layer**: The first LSTM layer returns sequences, allowing the next LSTM layer to process the data.
3. **Dropout Layer**: Helps prevent overfitting by randomly setting a fraction of input units to 0 at each update during training time.
4. **LSTM Layer**: The second LSTM layer processes the sequence and outputs a single vector.
5. **Dropout Layer**: Further reduces overfitting.
6. **Dense Layer**: Fully connected layer with a sigmoid activation function to output the probability of the review being positive.

## Dataset

The model uses the IMDB movie review dataset, which is a widely used benchmark for sentiment classification tasks. The dataset contains 25,000 highly polarized movie reviews for training and 25,000 for testing.

- **Maximum number of words considered**: 20,000
- **Maximum review length**: 100 words (reviews are padded or truncated to this length)
