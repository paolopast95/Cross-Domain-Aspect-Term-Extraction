# Cross-Domain ATE

This repository contains notebooks for performing Aspect Term Extraction with different approaches.
We performed different tests combining well-known technologies and models. In particular, we focused on:

  - BERT
  - ELMo + Residual Bi-LSTM
  - Word2Vec + Residual Bi-LSTM
  - GloVe + Residual Bi-LSTM
  - ELMo + GRU

We also tried to improve the recommendation process by extracting relevant aspect terms from reviews. In the repository there is also a notebook with the code for extracting all the aspects.

# Installation

All the notebooks were implemented through Google Colab and should run without problems on that platform. All the required libraries are installed via Colab. The only change that should be done in the code is related to the path for the datasets.
In the code there are path like "/content/drive/My Drive/..../dataset.csv". These paths should be modified for the correct execution of the code. 

Concerning the extraction of aspect terms (Notebook "Aspect_Extraction_from_YELP.ipynb"), before extracting aspect terms from yelp dataset and performing sentiment analysis on the atomic sentences, we train a model on all the available datasets. If we don't need to re-train the model, we can skip that phase and load the weights model_weights.weights.

You can download the Yelp dataset and the weights from the following links:

YELP: https://drive.google.com/file/d/1oHmo6pI51RRNQhH5oWVldiOhZ3Octnkh/view?usp=sharing

ELMo weights: https://drive.google.com/file/d/1SzhITFdb2mz6nxt-oDKq5vlGpToD3TST/view?usp=sharing


ATTENTION: before loading the weights we need to define the structure of the neural network. We are only saving the weights, not all the model.

