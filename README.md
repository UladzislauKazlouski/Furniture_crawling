-----------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------
Running the Code
To run this project, follow these steps:
Ensure all required libraries are installed (pandas, torch, transformers, flask, etc.)
Download the trained model and place it in the furniture_ner_model directory
Ensure cleaned_furniture_products.json is present in the working directory

Then RUN CODE_inicilization.ipynb
-----------------------------------------------------------------------------------------------------------------------------
Note |
---- |
This README assumes that all previous stages (web crawling, data cleaning, model training) have been completed and the necessary files are available. Make sure to run the entire pipeline from web crawling to model training before using the web application

-----------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------
This project involves web crawling, data cleaning, named entity recognition (NER) model training, and a web application for searching furniture products extracted from various websites.
Project Stages
1. Web Crawling and Data Collection
Uses aiohttp for asynchronous web crawling
Fetches content from furniture-related websites
Stores raw data in a CSV file
2. Data Cleaning and Preprocessing
Removes HTML tags, special characters, and irrelevant content
Applies text normalization techniques (lowercasing, lemmatization)
Filters out short or empty texts
Saves cleaned data to cleaned_furniture_data.csv
3. Data Labeling
Uses spaCy for initial tokenization
Labels tokens with furniture-related tags (B-PRODUCT, I-PRODUCT, O)
Saves labeled data in JSON format
4. NER Model Training
Uses BERT for token classification
Implements custom dataset and data loaders
Performs hyperparameter optimization using Optuna
Trains the model using the best hyperparameters
Saves the trained model to furniture_ner_model directory
5. Furniture Name Extraction
Applies the trained NER model to extract furniture names from new websites
Cleans and normalizes extracted product names
Saves results to cleaned_furniture_products.json
6. Web Application
Implements a Flask web application for searching extracted furniture products
Provides a simple user interface for entering website URLs and displaying results
