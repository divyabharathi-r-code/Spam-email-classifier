# Simple Email Spam Classifier using Logistic Regression

A minimal Python script that demonstrates binary classification using **Scikit-Learn**. The model trains on a small dataset to predict whether an email is "Spam" or "Normal" based entirely on the frequency of the word **"FREE"**.

## How It Works
The script utilizes a **Logistic Regression** model. It learns a decision boundary from a sample dataset where emails with low occurrences of the word "FREE" are marked as normal, and high occurrences are marked as spam. 

Given a new email with `7` instances of the word "FREE", the model outputs:
* **Classification:** Spam (Class 1)
* **Confidence Level:** ~98.5% probability

## Prerequisites

To run this script, you need Python installed along with `numpy` and `scikit-learn`. You can install the dependencies via pip:

```bash
pip install numpy scikit-learn
```

## Usage

1. Save the code into a file named `spam_classifier.py`.
2. Run the script using your terminal:

```bash
python spam_classifier.py
```

## Dataset Representation

The model maps the feature (count of the word "FREE") to binary targets:
* **Class 0 (Normal Email):** 0, 1, or 2 occurrences.
* **Class 1 (Spam Email):** 4 or 5 occurrences.

The decision boundary naturally falls around **3 words**, making any email containing 4 or more "FREE" words highly likely to be flagged as spam.
