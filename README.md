# Plagiarism-Detector

## Introduction
A Plagiarism Detector that examines a text file and performs binary classification; labeling a file as plagiarized or not; depending on how similar that text file is to a provided source text. 

This is part of the Udacity Machine Learning Engineer Nanodegree program.

## Description
Detecting plagiarism is an active area of research, and the differences between paraphrased answers and original work are not so obvious.

Steps include:
1. Data Exploration
2. Feature Engineering, including text pre-processing and train/test split
3. Train and Deployment of Model in Amazon SageMaer

## Feature Engineering
One of the ways to detect plagiarism is by computing **similarity features** that measure how similar a text is compared to the source text. 

### Containment
The extent of similarity between two texts (input and source) based on their n-gram intersection. 

To calculate containment:
1. Calculate the n-gram **intersection** between the input and source text.
2. Add up the number of common terms. 
3. Get the normalized containment from dividing the value obtained in step 2 by the number of n-grams in the input text.

### Longest Common Subsequence
Finding the longest common subsequence of words that appear left to right in both texts. 

The words do not have to be exactly continuous, just in left to right order. 

Then determine the normalized LCS from dividing the LCS value by the length of the input text. 

## Dataset
You may find the dataset used for model training and evaluation [here](https://ir.shef.ac.uk/cloughie/resources/plagiarism_corpus.html).

**Citation for data**: Clough, P. and Stevenson, M. Developing A Corpus of Plagiarised Short Answers, Language Resources and Evaluation: Special Issue on Plagiarism and Authorship Analysis, In Press.
