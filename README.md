Arabic Company Reviews – Rating Classification

This project builds a machine learning model to predict the rating (1–5 stars) of a company based on the Arabic review text provided by users.

The dataset is downloaded from Kaggle using kagglehub:

import kagglehub

# Download latest version
path = kagglehub.dataset_download("fahdseddik/arabic-company-reviews")
print(path)

📂 Dataset

Source: Kaggle
Name: Arabic Company Reviews
Content:

review: Arabic text review

rating: Integer rating ( -1 , 0 , 1 )

Additional fields depending on dataset version

This project aims to transform these raw reviews into structured learning signals for classification.

🧹 Preprocessing

The notebook includes a full Arabic NLP text-cleaning pipeline:

Remove URLs, emojis, numbers, and punctuation

Normalize Arabic letters

Remove diacritics (التشكيل)

Handle elongation (e.g., “جميلللل → جميل”)

Tokenize text

Remove Arabic stopwords

Stemming or lemmatization (optional)

Convert text to numerical vectors:

TF-IDF

or Transformer embeddings (AraBERT, CAMeLBERT, MARBERT)

🤖 Models Implemented

Deep Learning:

LSTM model

📊 Evaluation Metrics

Performance is measured using:

Accuracy

Precision

Recall

F1-score

Confusion Matrix


3. Run the notebook

Open Jupyter or Google Colab and run the provided .ipynb file.

🎯 Project Goals

Build a complete classification pipeline for Arabic text

Understand how review content affects rating

Compare ML and transformer-based methods

Provide a clean and reusable workflow for Arabic NLP tasks
