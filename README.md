Fake News Detection Using Machine Learning
Overview

This project implements a Fake News Detection system using classical Machine Learning techniques.
The objective is to classify news articles as Fake or Real based on their textual content.

The solution is developed and executed in Google Colab, leveraging TF-IDF vectorization and multiple supervised learning algorithms for comparison and evaluation.

Key Features

Text preprocessing and normalization

TF-IDF feature extraction

Multiple classification models:

Logistic Regression

Decision Tree

Gradient Boosting

Random Forest

Performance evaluation using accuracy and classification reports

Manual testing with custom news input

Optional deployment support using Anvil

Dataset

Source: Kaggle – Fake News Detection Dataset
https://www.kaggle.com/datasets/jainpooja/fake-news-detection

Files Used:

Fake.csv

True.csv

Each dataset contains news articles labeled as fake or real.

Technology Stack

Python 3

Google Colab

Pandas, NumPy

Scikit-learn

Matplotlib, Seaborn

Kaggle API

Anvil Uplink (optional)

Project Workflow

Dataset acquisition from Kaggle

Data cleaning and preprocessing

Feature extraction using TF-IDF

Model training and evaluation

Manual testing of unseen news articles

Optional model upload to Anvil Data Tables

Installation & Setup (Google Colab)
Step 1: Open Notebook

Upload the notebook file to Google Colab or open it via a shared link.

Step 2: Configure Kaggle API

Create an API token from Kaggle (kaggle.json)

Upload the file to Colab

Run:

mkdir -p ~/.kaggle
cp kaggle.json ~/.kaggle/
chmod 600 ~/.kaggle/kaggle.json

Step 3: Download Dataset
!kaggle datasets download -d jainpooja/fake-news-detection --unzip

Step 4: Execute Notebook

Run all cells sequentially to:

Train models

Evaluate performance

Enable manual testing

Models Implemented
Model	Description
Logistic Regression	Baseline linear classifier
Decision Tree	Rule-based classification
Gradient Boosting	Ensemble boosting model
Random Forest	Bagging-based ensemble
Model Evaluation

Each model is evaluated using:

Accuracy score

Precision

Recall

F1-score

Evaluation is performed on a held-out test dataset.

Manual Testing

Users can input custom news text to receive predictions from all trained models, allowing real-time qualitative testing.

Optional: Anvil Integration

The trained model and TF-IDF vectorizer can be uploaded to Anvil Data Tables for use in a web application.

Requirements:

anvil-uplink

Valid Anvil uplink key

Output Files

manual_testing.csv

fake_news_model.pkl

tfidf_vectorizer.pkl

Limitations

Classical ML models only (no deep learning)

Dataset bias may affect real-world generalization

Requires internet access for Kaggle download

Future Enhancements

Transformer-based models (BERT, RoBERTa)

REST API using FastAPI

Web interface using Streamlit

Hyperparameter tuning and cross-validation
