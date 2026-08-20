
# Code Switching NLP | Code Saviours SI-26 | Saima Manzoor

## Roman Urdu–English Code Switching Detector

A machine learning application that analyzes a Roman Urdu-English sentence and identifies whether each word belongs to **Roman Urdu (URD)**, **English (ENG)**, or **Mixed (MIX)**.

## Why This Matters

Roman Urdu and English are frequently used together in everyday online communication, including social media posts, chats, comments, and messages. However, many language processing systems are designed for a single language and may struggle when both languages appear in the same sentence.

This project focuses on identifying the language category of each individual word in code-switched text. This can be useful as a foundation for future applications involving multilingual text analysis, sentiment analysis, search, and other NLP tasks.

## Live Demo

Try it here:

[https://huggingface.co/spaces/Saima109/code-switching-demo](https://huggingface.co/spaces/Saima109/code-switching-demo)

<img width="1913" height="993" alt="image" src="https://github.com/user-attachments/assets/10d125a4-b9c0-4de1-927d-1517a98f0e0f" />

The demo allows users to enter a Roman Urdu, English, or mixed sentence and view the predicted category for each word.

## How It Works

The user enters a sentence containing Roman Urdu, English, or a combination of both.

The application separates the sentence into individual words and sends them to the trained language classification model.

Each word is analyzed and assigned one of three labels: **URD**, **ENG**, or **MIX**.

The final interface displays the detected words along with their predicted labels and a summary showing the total number of words in each category.

## Results

The model was evaluated on three language categories: Roman Urdu (URD), English (ENG), and Mixed (MIX).

| Label | F1 Score |
|-------|----------|
| Roman Urdu (URD) | 0.9949 |
| English (ENG) | 0.9917 |
| Mixed (MIX) | 0.0000 |

**Overall Accuracy: 99%**

**Weighted Average F1 Score: 0.99**

The model performed very well for Roman Urdu and English word classification. The MIX category received an F1 score of 0.0000 because only one MIX example was available in the evaluation data, making it difficult to evaluate and learn this category reliably.
## How to Run Locally

```bash
git clone https://github.com/saimamanzoor651/code-switching-codesaviours-si26-saima.git
cd code-switching-codesaviours-si26-saima
pip install transformers torch
```

```python
from transformers import pipeline

classifier = pipeline(
    "token-classification",
    model="Saima-Manzoor/code-switching-codesaviours-si26-saima"
)

result = classifier(
    "Kal university mein presentation hai aur I am feeling prepared"
)

print(result)
```

## Repository Structure

```
├── SI26_Week6_Saima.ipynb   # Dataset preparation and labeling work
├── SI26_Week7_Saima.ipynb   # Model training and evaluation
├── dataset.csv              # Dataset used for the project
└── README.md                # Project documentation
```
## Project Overview

This project was developed as part of the **Code Saviours SI-26** program. The work includes preparing a labeled dataset, training a language classification model, evaluating its performance, and deploying an interactive demonstration.

The application provides a simple interface where users can test sentences and see how individual words are classified between Roman Urdu and English.

## Built With

* Python
* Hugging Face Transformers
* PyTorch
* XLM-RoBERTa
* Hugging Face Spaces
* Google Colab / Jupyter Notebook

---

**Built by: Saima Manzoor | Code Saviours SI-26 | 2026**
