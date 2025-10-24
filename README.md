Emotion Detection AI

Overview

This project implements an Emotion Detection system that classifies text into 7 main emotions: joy, sadness, anger, fear, disgust, surprise, and neutral. It uses the GoEmotions dataset and a TF-IDF + Logistic Regression approach.

Users can input text in a Jupyter Notebook widget or a Streamlit web app and receive:

Predicted emotion

Prediction confidence per emotion

Top words influencing prediction


Features

Data preprocessing and cleaning

TF-IDF vectorization (1-3 grams)

Logistic Regression with GridSearch hyperparameter tuning

Comparison with Naive Bayes and Random Forest

Confusion matrix and classification report

Misclassified example analysis

Jupyter widget for interactive input

Prediction output saved in prediction_output.txt

Optional Streamlit web interface


Workflow

1. Load GoEmotions dataset via datasets library.


2. Simplify 27 original emotions into 7 main categories.


3. Clean text by removing punctuation, stopwords, and URLs.


4. Vectorize text using TF-IDF (max 10000 features, ngram 1-3).


5. Train Logistic Regression model (hyperparameter tuned using GridSearchCV).


6. Evaluate model using classification report, accuracy, and confusion matrix.


7. Input new text via:

Jupyter Notebook widget

Streamlit web app (optional)



8. Save predictions and confidence to prediction_output.txt.



Model Details

Vectorizer: TF-IDF (max_features=10000, ngram_range=(1,3))

Classifier: Logistic Regression (tuned hyperparameters)

Alternative Models Tested: Multinomial Naive Bayes, Random Forest

Main emotions: joy, sadness, anger, fear, disgust, surprise, neutral


Example Usage

Jupyter Notebook

text_input.value = "I am so happy today!"
predict_button.click()

Streamlit Web App

streamlit run app.py

Folder Structure

emotion-detection-ai/
│
├─ notebooks /               # Jupyter notebook file
├─ models/                   # Saved models and vectorizers
├─ outputs/                  # Saved prediction outputs
├─ app.py                    # Streamlit web app          
└─ README.md

Installation

1. Clone or upload project files.


2. Install dependencies:



pip install -r requirements.txt

3. Open notebooks/EmotionDetection.ipynb and run all cells.



Outputs

Predicted emotion

Confidence per emotion

Top contributing TF-IDF words

Saved in outputs/prediction_output.txt


License

MIT License
