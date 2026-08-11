Sentiment Analysis Classifier

A machine learning model that classifies movie reviews as positive or negative using Natural Language Processing (NLP) and scikit-learn.

This project walks through the complete end-to-end machine learning pipeline — from raw text data to a working, evaluated prediction model — built as a hands-on introduction to core AI/ML concepts.

What It Does
Takes a movie review as text input (e.g. "This film was a masterpiece, I loved every second")
Cleans and converts the text into numerical features using TF-IDF
Predicts whether the sentiment is positive or negative
Tech Stack
Python 3
pandas
scikit-learn
NLTK
Dataset

IMDB Movie Reviews Dataset — 50,000 labeled movie reviews (positive/negative).

Pipeline
Data Exploration — load dataset, check class balance, inspect samples
Text Preprocessing — lowercasing, punctuation removal, stopword removal, TF-IDF vectorization
Train/Test Split — 80/20 split to evaluate generalization
Model Training — Logistic Regression / Naive Bayes
Evaluation — accuracy, precision, recall, confusion matrix
Custom Testing — test the model on your own written reviews
Project Structure
sentiment-analysis-classifier/
├── data/
│   └── imdb_reviews.csv
├── notebooks/
│   └── sentiment_analysis.ipynb
├── src/
│   ├── preprocess.py
│   ├── train.py
│   └── predict.py
├── requirements.txt
└── README.md
Installation
bash
git clone https://github.com/<your-username>/sentiment-analysis-classifier.git
cd sentiment-analysis-classifier
pip install -r requirements.txt
Usage

Run the notebook:

bash
jupyter notebook notebooks/sentiment_analysis.ipynb

Or run the training script directly:

bash
python src/train.py

Test on a custom sentence:

python
from src.predict import predict_sentiment

predict_sentiment("This movie was absolutely fantastic!")
# Output: Positive
Results
Model	Accuracy
Naive Bayes	TBD
Logistic Regression	TBD

(Fill in after training)

Future Improvements
Try more advanced models (SVM, deep learning with LSTM/BERT)
Deploy as a simple web app using Streamlit or Gradio
Expand to multi-class sentiment (e.g. very negative → very positive)
