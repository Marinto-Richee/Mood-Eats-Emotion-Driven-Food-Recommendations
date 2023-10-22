# Emotion-Based Food Recommendation System

This repository contains a Python script that utilizes both textual sentiment analysis and facial emotion prediction to recommend food items based on the user's emotional state. It combines VADER sentiment analysis for textual input and a deep learning model for predicting emotions from facial images.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Usage](#usage)
- [Code Explanation](#code-explanation)
    - [Sentiment Analysis](#sentiment-analysis)
    - [Facial Emotion Prediction](#facial-emotion-prediction)
    - [Data Processing](#data-processing)
    - [Visualization](#visualization)
    - [Comparison of Textual and Facial Predictions](#comparison-of-textual-and-facial-predictions)
    - [Print Recommendations](#print-recommendations)

## Prerequisites
Before using this code, ensure you have the following installed:
- Python 3.x
- TensorFlow and Keras for deep learning
- VADER Sentiment Analysis Library
- NumPy, Matplotlib, and Pandas

## Usage
1. Clone this repository to your local machine.

2. Make sure you have the required dependencies installed (mentioned in the Prerequisites section).

3. Place your pre-trained emotion prediction model (named "emotion_model.h5") and a custom image (e.g., "happy.jpg") in the same directory as the script.

4. Run the Python script:

```python
python emotion_based_food_recommendation.py
```

5. Follow the prompt to input a sentence. The script will analyze the sentiment of the input and predict emotion from the provided image. It will recommend a food item based on the predicted emotion.

## Code Explanation

### Sentiment Analysis
- The script takes a sentence as input from the user.
- Utilizes the VADER sentiment analysis library to analyze the sentiment of the input.
- The sentiment score is classified as positive, negative, or neutral based on the compound score.

### Facial Emotion Prediction
- Loads a pre-trained deep learning model for emotion prediction from an image.
- Loads and preprocesses a custom image.
- Uses the model to predict the emotion from the image, such as "happy" or "sad."

### Data Processing
- Reads data from a CSV file named "Food and Emotion.csv" into a Pandas DataFrame.
- Performs data preprocessing, such as converting emotion and food strings to lowercase and mapping certain emotions to specific categories.

### Visualization
- Utilizes Matplotlib to display the image, sentiment analysis, and emotion prediction.

### Comparison of Textual and Facial Predictions
- Compares the prediction percentages for textual sentiment analysis and facial emotion prediction.
- Selects the prediction method with the higher percentage as the final prediction for emotion.

### Print Recommendations
- Prints the final emotion and recommends a food item based on the selected prediction method.

For better organization and readability, consider encapsulating certain functionality into functions or classes, adding detailed comments, and handling exceptions and errors that may occur during file loading or data processing.

Enjoy using this emotion-based food recommendation system!
