# 🎬 Sentiment Analysis Classifier

<p align="center">
  <b>An End-to-End NLP & Machine Learning Project for Movie Review Sentiment Classification</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/NLP-Text%20Classification-green" alt="NLP">
  <img src="https://img.shields.io/badge/Scikit--learn-Machine%20Learning-orange?logo=scikit-learn&logoColor=white" alt="Scikit-learn">
  <img src="https://img.shields.io/badge/NLTK-NLP-yellow" alt="NLTK">
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-purple?logo=pandas&logoColor=white" alt="Pandas">
</p>

---

## 📌 About the Project

**Sentiment Analysis Classifier** is a Machine Learning project that analyzes movie reviews and classifies them as either **Positive** 😊 or **Negative** 😞.

The project demonstrates a complete **Natural Language Processing (NLP) and Machine Learning pipeline**, starting from raw text data and ending with a trained model capable of making predictions on new, unseen reviews.

### 🔄 Overall Workflow

```text
Raw Movie Review
       ↓
Text Preprocessing
       ↓
TF-IDF Vectorization
       ↓
Train/Test Split
       ↓
Machine Learning Model
       ↓
Model Evaluation
       ↓
Sentiment Prediction
```

---

## ✨ What This Project Does

* 🎥 Takes a movie review as text input
* 🧹 Cleans and preprocesses the text
* 🔤 Converts text into numerical features using **TF-IDF**
* 🤖 Trains Machine Learning classification models
* 📊 Evaluates model performance
* 🔍 Generates a confusion matrix
* ✍️ Allows custom reviews to be tested
* 📈 Compares different classification algorithms

---

## 🛠️ Tech Stack

| Technology              | Purpose                        |
| ----------------------- | ------------------------------ |
| 🐍 **Python**           | Core programming language      |
| 🐼 **Pandas**           | Data manipulation and analysis |
| 🤖 **Scikit-learn**     | Machine Learning               |
| 📚 **NLTK**             | Natural Language Processing    |
| 📓 **Jupyter Notebook** | Experimentation and analysis   |
| 🔢 **TF-IDF**           | Text feature extraction        |

---

## 📊 Dataset

The project uses the **IMDb Movie Reviews Dataset**, containing **50,000 labeled movie reviews**.

| Category         | Details             |
| ---------------- | ------------------- |
| Total Reviews    | 50,000              |
| Positive Reviews | 25,000              |
| Negative Reviews | 25,000              |
| Classes          | Positive / Negative |
| Domain           | Movie Reviews       |

The dataset provides balanced positive and negative examples, making it suitable for binary sentiment classification.

---

## 🧠 NLP Pipeline

### 1️⃣ Data Exploration

The dataset is first explored to understand:

* Number of reviews
* Positive/negative class distribution
* Sample reviews
* Missing values
* Dataset structure

### 2️⃣ Text Preprocessing

Raw reviews are cleaned before being passed to the Machine Learning model.

The preprocessing pipeline includes:

* Lowercasing
* Punctuation removal
* Stopword removal
* Text normalization

Example:

```text
"This Movie Was AMAZING!"
              ↓
"this movie was amazing"
```

### 3️⃣ TF-IDF Vectorization

Since Machine Learning models cannot directly understand raw text, the cleaned reviews are converted into numerical vectors using **TF-IDF (Term Frequency–Inverse Document Frequency)**.

TF-IDF assigns importance to words based on how frequently they appear in a document compared with the entire collection of documents.

```text
Text
 ↓
TF-IDF
 ↓
Numerical Feature Matrix
 ↓
Machine Learning Model
```

---

## 🤖 Machine Learning Models

The project explores two popular classification algorithms:

### 🔹 Naive Bayes

A probabilistic algorithm that is commonly used for text classification tasks.

### 🔹 Logistic Regression

A powerful and widely used algorithm for binary classification and a strong baseline for NLP problems.

---

## 📈 Model Evaluation

The models are evaluated using multiple metrics:

* **Accuracy**
* **Precision**
* **Recall**
* **Confusion Matrix**

### Results

| Model               | Accuracy | Precision | Recall |
| ------------------- | -------: | --------: | -----: |
| Naive Bayes         |      TBD |       TBD |    TBD |
| Logistic Regression |      TBD |       TBD |    TBD |

> 📝 **Note:** Update the values above with the actual results after running the training pipeline.

---

## 🧪 Custom Prediction

The trained model can also be used to classify your own movie reviews.

### Example

```python
from src.predict import predict_sentiment

predict_sentiment("This movie was absolutely fantastic!")
```

### Output

```text
Positive
```

Another example:

```python
predict_sentiment("The movie was boring and disappointing.")
```

### Output

```text
Negative
```

---

## 📂 Project Structure

```text
sentiment-analysis-classifier/
│
├── 📁 data/
│   └── imdb_reviews.csv
│
├── 📁 notebooks/
│   └── sentiment_analysis.ipynb
│
├── 📁 src/
│   ├── preprocess.py
│   ├── train.py
│   └── predict.py
│
├── 📄 requirements.txt
└── 📄 README.md
```

### 📄 File Description

| File                                 | Description                    |
| ------------------------------------ | ------------------------------ |
| `data/imdb_reviews.csv`              | IMDb movie review dataset      |
| `notebooks/sentiment_analysis.ipynb` | Complete step-by-step analysis |
| `src/preprocess.py`                  | Text preprocessing functions   |
| `src/train.py`                       | Model training and evaluation  |
| `src/predict.py`                     | Custom sentiment prediction    |
| `requirements.txt`                   | Required Python libraries      |
| `README.md`                          | Project documentation          |

---

## ⚙️ Installation

Install the required dependencies using:

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Project

### 📓 Using Jupyter Notebook

```bash
jupyter notebook notebooks/sentiment_analysis.ipynb
```

### 🐍 Using the Training Script

```bash
python src/train.py
```

### 🔮 Making a Prediction

```python
from src.predict import predict_sentiment

review = "This film was a masterpiece, I loved every second!"

print(predict_sentiment(review))
```

Expected output:

```text
Positive
```

---

## 🎯 Learning Outcomes

This project provides practical experience with:

* Natural Language Processing
* Text preprocessing
* Stopword removal
* TF-IDF feature extraction
* Binary classification
* Train/Test splitting
* Naive Bayes
* Logistic Regression
* Model evaluation
* Confusion matrices
* Making predictions on unseen text
* Structuring an end-to-end Machine Learning project

---

## 🚀 Future Improvements

The project can be extended with more advanced techniques:

* 🔥 Support Vector Machine (SVM)
* 🧠 LSTM / RNN-based sentiment analysis
* 🤗 BERT and Transformer models
* 🌐 Streamlit web application
* 🎨 Gradio-based interface
* 📊 F1-score and ROC-AUC evaluation
* ⭐ Multi-class sentiment classification
* 📈 Confidence score for predictions
* 💾 Model serialization using Joblib
* ⚡ Hyperparameter tuning

### Possible Multi-Class Extension

Instead of only:

```text
Positive / Negative
```

the model could classify:

```text
Very Negative
     ↓
Negative
     ↓
Neutral
     ↓
Positive
     ↓
Very Positive
```

---

## 💡 Example Prediction

### Input

> **"This film was a masterpiece, I loved every second!"**

### Model Output

```text
🎬 Sentiment: Positive 😊
```

---

## 🌟 Why This Project?

Sentiment analysis is a practical application of **Natural Language Processing** that allows computers to understand and classify opinions expressed in human language.

This project demonstrates how raw text can be transformed into meaningful numerical representations using **TF-IDF** and then classified using traditional Machine Learning algorithms.

It provides a strong foundation for progressing toward more advanced NLP techniques such as **Deep Learning and Transformer-based models**.

---

## 👩‍💻 Author

### Priyal Sabharwal

**B.E. Computer Science & Engineering — Artificial Intelligence & Machine Learning**

Interested in:

* 🤖 Artificial Intelligence
* 🧠 Machine Learning
* 📝 Natural Language Processing
* 🔐 Cybersecurity

---

## ⭐ Support

If you found this project useful or interesting, consider giving the repository a **⭐ Star**.

Feel free to explore the code, experiment with different models, and improve the project!

---

### 📜 License

This project is created for **educational and learning purposes**.
