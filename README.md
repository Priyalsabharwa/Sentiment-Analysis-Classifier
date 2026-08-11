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
  <img src="https://img.shields.io/badge/Google%20Colab-Notebook-orange?logo=googlecolab&logoColor=white" alt="Google Colab">
</p>

---

## 📌 Overview

**Sentiment Analysis Classifier** is a Machine Learning project that analyzes movie reviews and classifies them as either **Positive** 😊 or **Negative** 😞.

The project demonstrates a complete **Natural Language Processing (NLP) and Machine Learning pipeline**, starting from raw text data and ending with a trained model capable of making predictions on new, unseen reviews.

The complete implementation is developed and executed using **Google Colab**.

### 🔄 Overall Workflow

```text
Raw Movie Review
       ↓
Data Exploration
       ↓
Text Preprocessing
       ↓
TF-IDF Vectorization
       ↓
Train/Test Split
       ↓
Model Training
       ↓
Model Evaluation
       ↓
Custom Sentiment Prediction
```

---

## ✨ Features

* 🎥 Classifies movie reviews as **Positive** or **Negative**
* 🧹 Cleans and preprocesses raw text
* 🔤 Converts text into numerical features using **TF-IDF**
* 🤖 Uses Machine Learning classification algorithms
* 📊 Evaluates model performance
* 📈 Calculates accuracy, precision, and recall
* 🔍 Generates a confusion matrix
* ✍️ Supports custom movie review predictions
* 📓 Fully implemented in Google Colab
* 🚀 Can be extended to advanced NLP and Deep Learning models

---

## 🛠️ Tech Stack

| Technology                  | Purpose                               |
| --------------------------- | ------------------------------------- |
| 🐍 **Python 3**             | Programming language                  |
| 🐼 **Pandas**               | Data manipulation and analysis        |
| 🤖 **Scikit-learn**         | Machine Learning                      |
| 📚 **NLTK**                 | Natural Language Processing           |
| 🔢 **TF-IDF**               | Text feature extraction               |
| 📊 **Matplotlib / Seaborn** | Data visualization                    |
| ☁️ **Google Colab**         | Development and execution environment |

---

## 📊 Dataset

The project uses the **IMDb Movie Reviews Dataset**, containing **50,000 labeled movie reviews**.

| Property            | Details             |
| ------------------- | ------------------- |
| 📚 Total Reviews    | 50,000              |
| 😊 Positive Reviews | 25,000              |
| 😞 Negative Reviews | 25,000              |
| 🏷️ Classes         | Positive / Negative |
| 🎬 Domain           | Movie Reviews       |

The balanced dataset provides equal numbers of positive and negative reviews for binary sentiment classification.

---

## 🧠 NLP & Machine Learning Pipeline

### 1️⃣ Data Exploration

The dataset is first explored to understand its structure and distribution.

The analysis includes:

* Number of reviews
* Class distribution
* Sample reviews
* Missing values
* Dataset information
* Positive vs. negative review distribution

---

### 2️⃣ Text Preprocessing

Raw movie reviews contain unnecessary characters and formatting that can affect model performance.

The following preprocessing techniques are applied:

* Lowercasing
* Punctuation removal
* Stopword removal
* Text normalization

#### Example

```text
"This Movie Was AMAZING!"
            ↓
"this movie was amazing"
```

---

### 3️⃣ TF-IDF Vectorization

Machine Learning models cannot directly process raw text.

Therefore, the cleaned text is converted into numerical features using **TF-IDF (Term Frequency–Inverse Document Frequency)**.

```text
Movie Review
     ↓
Text Cleaning
     ↓
TF-IDF Vectorization
     ↓
Numerical Feature Matrix
```

TF-IDF assigns higher importance to words that are meaningful within a review while reducing the importance of extremely common words.

---

## 🤖 Machine Learning Models

The project uses and compares two popular Machine Learning algorithms for sentiment classification.

### 🔹 Naive Bayes

Naive Bayes is a probabilistic classification algorithm that performs particularly well on many text classification problems.

### 🔹 Logistic Regression

Logistic Regression is a widely used binary classification algorithm and provides a strong baseline for sentiment analysis.

---

## 📈 Model Evaluation

The trained models are evaluated using multiple performance metrics:

* ✅ Accuracy
* ✅ Precision
* ✅ Recall
* ✅ Confusion Matrix

### 📊 Results

| Model               | Accuracy | Precision | Recall |
| ------------------- | -------: | --------: | -----: |
| Naive Bayes         |      TBD |       TBD |    TBD |
| Logistic Regression |      TBD |       TBD |    TBD |

> **Note:** Replace the `TBD` values with the actual results obtained after running the models in Google Colab.

---

## 🔍 Confusion Matrix

A confusion matrix is used to understand how well the classifier distinguishes between positive and negative reviews.

```text
                 Predicted
              Negative  Positive
Actual
Negative          TN        FP

Positive          FN        TP
```

This helps identify:

* Correctly classified positive reviews
* Correctly classified negative reviews
* False positive predictions
* False negative predictions

---

## 🧪 Custom Prediction

After training the model, custom movie reviews can be passed to the classifier to test its predictions.

### Example 1 — Positive Review

```python
review = "This movie was absolutely fantastic and entertaining!"
```

### Prediction

```text
Positive 😊
```

---

### Example 2 — Negative Review

```python
review = "The movie was boring, slow and disappointing."
```

### Prediction

```text
Negative 😞
```

---

## 💻 Example Prediction Code

```python
# Example custom review

review = "This film was a masterpiece, I loved every second!"

prediction = model.predict(vectorizer.transform([review]))

if prediction[0] == 1:
    print("Positive 😊")
else:
    print("Negative 😞")
```

---

## 📓 Google Colab

The project is developed and executed using **Google Colab**, making it easy to run the complete NLP and Machine Learning pipeline without requiring a local development environment.

### Colab Workflow

```text
Open Google Colab
      ↓
Upload / Load Dataset
      ↓
Run Data Exploration
      ↓
Preprocess Reviews
      ↓
Apply TF-IDF
      ↓
Train Models
      ↓
Evaluate Performance
      ↓
Test Custom Reviews
```

---

## 📁 Project Structure

Since the project is developed in Google Colab, the main implementation is organized inside a Jupyter/Colab notebook.

```text
sentiment-analysis-classifier/
│
├── 📓 sentiment_analysis.ipynb
│
├── 📊 imdb_reviews.csv
│
└── 📄 README.md
```

### File Description

| File                       | Description                          |
| -------------------------- | ------------------------------------ |
| `sentiment_analysis.ipynb` | Complete Google Colab implementation |
| `imdb_reviews.csv`         | IMDb movie review dataset            |
| `README.md`                | Project documentation                |

---

## ⚙️ Requirements

The project uses the following Python libraries:

```text
Python 3.x
Pandas
NumPy
Scikit-learn
NLTK
Matplotlib
Seaborn
```

If running in Google Colab, most required libraries are already available.

Additional packages can be installed using:

```python
!pip install nltk scikit-learn pandas matplotlib seaborn
```

---

## ▶️ How to Run

### Step 1 — Open Google Colab

Open the project notebook in Google Colab.

### Step 2 — Load the Dataset

Upload or load the IMDb dataset into the Colab environment.

### Step 3 — Run the Notebook

Execute the notebook cells sequentially:

```text
Data Loading
     ↓
Data Exploration
     ↓
Text Preprocessing
     ↓
TF-IDF
     ↓
Train/Test Split
     ↓
Model Training
     ↓
Evaluation
     ↓
Custom Prediction
```

### Step 4 — Test Your Own Review

Modify the review text and run the prediction cell.

Example:

```python
custom_review = "I really enjoyed this movie. It was amazing!"
```

Expected result:

```text
Positive 😊
```

---

## 🎯 Learning Outcomes

This project provides practical understanding of:

* 📌 Natural Language Processing
* 📌 Text preprocessing
* 📌 Stopword removal
* 📌 TF-IDF feature extraction
* 📌 Binary classification
* 📌 Train/Test splitting
* 📌 Naive Bayes
* 📌 Logistic Regression
* 📌 Accuracy, Precision & Recall
* 📌 Confusion Matrix
* 📌 Custom text prediction
* 📌 End-to-end Machine Learning workflow

---

## 🚀 Future Improvements

The project can be extended with more advanced NLP and Machine Learning techniques.

### 🔥 Advanced Models

* Support Vector Machine (SVM)
* Random Forest
* Gradient Boosting

### 🧠 Deep Learning

* RNN
* LSTM
* GRU
* BERT
* Transformer-based models

### 🌐 Deployment

The trained model can be deployed as an interactive application using:

* Streamlit
* Gradio
* Flask
* FastAPI

### 📊 Additional Features

* F1-score
* ROC-AUC curve
* Cross-validation
* Hyperparameter tuning
* Prediction confidence score
* Multi-class sentiment classification

---

## ⭐ Multi-Class Extension

Currently, the model performs binary classification:

```text
Positive 😊
     OR
Negative 😞
```

A future version could support:

```text
Very Negative 😡
       ↓
Negative 😞
       ↓
Neutral 😐
       ↓
Positive 🙂
       ↓
Very Positive 🤩
```

---

## 💡 Real-World Applications

Sentiment analysis can be applied to many real-world scenarios, including:

* 🎬 Movie and product reviews
* 📱 Social media monitoring
* 🛍️ Customer feedback analysis
* ⭐ E-commerce reviews
* 📧 Customer support analysis
* 📊 Brand reputation monitoring
* 📰 Opinion and feedback analysis

---

## 🌟 Project Highlights

```text
✅ 50,000 Movie Reviews
✅ NLP Preprocessing
✅ TF-IDF Feature Extraction
✅ Machine Learning Classification
✅ Naive Bayes
✅ Logistic Regression
✅ Model Evaluation
✅ Confusion Matrix
✅ Custom Predictions
✅ Google Colab Implementation
```

---

## 📜 License

This project is created for **educational and learning purposes**.
