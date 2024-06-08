# Complete Text Analysis App

## Introduction

The Complete Text Analysis App is a Streamlit-based web application that provides various text analysis functionalities. The app includes features for spam detection, sentiment analysis, stress detection, hate and offensive content detection, and sarcasm detection. It leverages Natural Language Processing (NLP) techniques and machine learning models to analyze and classify text inputs.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Configuration](#configuration)
- [Documentation](#documentation)
- [Examples](#examples)
- [Troubleshooting](#troubleshooting)
- [Contributors](#contributors)
- [License](#license)

## Features

1. **Spam or Ham Detection**
   - Classifies text as spam or ham.
2. **Sentiment Analysis**
   - Detects the sentiment of the text (positive or negative).
3. **Stress Detection**
   - Determines the level of stress in the text.
4. **Hate and Offensive Content Detection**
   - Identifies the level of hate and offensive content in the text.
5. **Sarcasm Detection**
   - Detects whether the text is sarcastic or not.

## Installation

To install and run the Complete Text Analysis App, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/complete-text-analysis-Using-Natural-Language-Processing.git
   cd complete-text-analysis-app
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Download NLTK data:
   ```python
   import nltk
   nltk.download('punkt')
   nltk.download('stopwords')
   ```

4. Run the Streamlit app:
   ```bash
   streamlit run app.py
   ```

## Usage

1. Navigate to the app in your web browser.
2. Use the sidebar to select the desired analysis option:
   - Home
   - Spam or Ham Detection
   - Sentiment Analysis
   - Stress Detection
   - Hate and Offensive Content Detection
   - Sarcasm Detection
3. Enter the text you want to analyze in the provided text area.
4. Click the "Predict" button to get the analysis results.

## Dependencies

- Python 3.x
- Streamlit
- NumPy
- Pandas
- NLTK
- Scikit-learn

## Configuration

Ensure you have the following CSV files in the same directory as `app.py`:

- Spam Detection.csv
- Sentiment Analysis.csv
- Stress Detection.csv
- Hate Content Detection.csv
- Sarcasm Detection.csv

The CSV files should have the following columns:
- Spam Detection.csv: `Label`, `Text`
- Sentiment Analysis.csv: `Text`, `Label`
- Stress Detection.csv: `Text`, `Sentiment`, `Stress Level`
- Hate Content Detection.csv: `Hate Level`, `Offensive Level`, `Class Level`, `Text`
- Sarcasm Detection.csv: `Text`, `Label`

## Documentation

### Text Cleaning and Transformation

The `transform_text` function cleans and preprocesses the text input by:
- Converting to lowercase
- Tokenizing words
- Removing stopwords and punctuation
- Stemming the words

### Model Training

Each analysis option has its own model training setup using the provided CSV files. The models are trained using Scikit-learn classifiers and vectorizers.

### Spam Detection
- Uses Logistic Regression and TF-IDF Vectorizer.

### Sentiment Analysis
- Uses Logistic Regression and TF-IDF Vectorizer.

### Stress Detection
- Uses Decision Tree Regressor and TF-IDF Vectorizer.

### Hate and Offensive Content Detection
- Uses Random Forest Classifier and TF-IDF Vectorizer.

### Sarcasm Detection
- Uses Logistic Regression and TF-IDF Vectorizer.

## Examples

Here are some examples of how to use the app:

- Enter a text message to check if it's spam or ham.
- Analyze the sentiment of a social media post.
- Detect stress levels in a piece of text.
- Identify offensive content in user comments.
- Check if a statement is sarcastic.

## Troubleshooting

- Ensure all CSV files are correctly formatted and placed in the same directory as `app.py`.
- Verify that all dependencies are installed.
- Check for any errors in the console for more details on issues.

## Contributors

- https://github.com/shubham5027

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

Feel free to customize this README further based on your project's specific details or additional information you might have.
