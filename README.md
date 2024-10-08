# Sentiment Analysis with Machine Learning Models

## Overview

This project is focused on performing sentiment analysis on a dataset using various machine learning models. The dataset used in this project is from Twitter, and the goal is to classify the sentiments expressed in tweets into different categories. The models used include:

- **Naive Bayes**
- **Decision Tree**
- **Random Forest**

The project also includes data preprocessing steps such as text cleaning, tokenization, and vectorization. Additionally, it provides functions for predicting sentiments of new text inputs using the trained models.

## Table of Contents

- [Project Structure](#project-structure)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Data Preprocessing](#data-preprocessing)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Predicting Sentiments](#predicting-sentiments)
- [Visualizations](#visualizations)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Project Structure

```
.
├── twitter_training.csv        # The dataset file (ensure this file is in your working directory)
├── sentiment_analysis.ipynb    # Jupyter notebook with the full code and analysis
├── README.md                   # This README file
└── requirements.txt            # Required Python packages
```

## Features

- **Data Loading:** Load and display the dataset with appropriate column names.
- **Data Preprocessing:** Text cleaning, tokenization, removal of stop words, and vectorization using `CountVectorizer`.
- **Model Training:** Train and evaluate models like Naive Bayes, Decision Tree, and Random Forest on the dataset.
- **Prediction Functionality:** Functions to predict sentiments on new text inputs using trained models.
- **Visualizations:** Generate plots like count plots, histograms, pie charts, and confusion matrix heatmaps to visualize data and model performance.

## Requirements

Before running the project, ensure you have the following Python packages installed:

- `pandas`
- `numpy`
- `seaborn`
- `matplotlib`
- `nltk`
- `wordcloud`
- `scikit-learn`

You can install the necessary packages using:

```bash
pip install -r requirements.txt
```

## Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/sentiment-analysis.git
   ```
2. **Navigate to the Project Directory:**
   ```bash
   cd sentiment-analysis
   ```
3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
4. **Run the Jupyter Notebook:**
   ```bash
   jupyter notebook sentiment_analysis.ipynb
   ```

## Data Preprocessing

The dataset is preprocessed to make it suitable for machine learning models:

1. **Text Cleaning:** Removal of punctuation, numbers, and conversion to lowercase.
2. **Tokenization:** Splitting of text into individual words (tokens).
3. **Stop Word Removal:** (Optional) Removing common words that do not contribute to the sentiment.
4. **Vectorization:** Converting text data into numerical vectors using `CountVectorizer`.

## Model Training and Evaluation

The following models are trained and evaluated:

- **Naive Bayes:** A simple yet effective algorithm for text classification tasks.
- **Decision Tree:** A model that splits the data based on feature importance to classify the sentiments.
- **Random Forest:** An ensemble model that uses multiple decision trees to improve accuracy.

Each model is evaluated using metrics like accuracy, precision, recall, F1-score, and confusion matrix.

## Predicting Sentiments

Two functions are provided to predict the sentiment of a new text input:

```python
def predict_sentiment(Text, model):
    # Process the text
    processed_Text = processword(Text)

    # Transform the text into vectors
    X_new = v.transform([processed_Text])

    # Predict sentiment
    predicted_sentiment = model.predict(X_new)
    
    # Output the sentiment
    print("Predicted sentiment:", predicted_sentiment[0])
```

Example usage:

```python
predict_sentiment("I love this movie!", model)  # Random Forest model
predict_sentiment("I hate this movie!", nb)     # Naive Bayes model
```

## Visualizations

The project includes several visualizations to help understand the data and the performance of the models:

- **Count Plot:** Displays the distribution of sentiment labels.
- **Histogram:** Shows the frequency distribution of sentiment labels.
- **Pie Chart:** Visual representation of sentiment label proportions.
- **Confusion Matrix Heatmap:** Visualizes the performance of classification models.

## Usage

1. **Load the Dataset:** Ensure that `twitter_training.csv` is in your working directory.
2. **Run the Jupyter Notebook:** Execute the cells in `sentiment_analysis.ipynb` to perform data preprocessing, model training, and evaluation.
3. **Predict Sentiments:** Use the provided functions to predict sentiments on new text inputs.
