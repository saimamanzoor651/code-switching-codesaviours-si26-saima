# Code Switching NLP | Code Saviours SI-26 | Saima Manzoor
Haan yaar 😭 **bilkul proper README.md format / raw Markdown** mein de rahi hoon. Isko **as it is copy karke GitHub ki `README.md` file mein paste** kar do:

# Roman Urdu–English Code Switching Detector

A machine learning application that detects whether each word in a sentence belongs to **Roman Urdu, English, or Mixed language**.

## Why This Matters

In Pakistan and other multilingual communities, people often communicate using a mixture of Roman Urdu and English. Traditional language detection systems usually identify only the language of an entire sentence, which makes it difficult to detect language switching at the word level.

This project solves this problem by analyzing each word separately and predicting whether it belongs to **Roman Urdu (URD)**, **English (ENG)**, or **Mixed (MIX)**.

This can be useful for multilingual text analysis, social media analysis, chatbots, and other Natural Language Processing applications.

## Live Demo

Try the live application here:

[https://huggingface.co/spaces/Saima109/code-switching-demo](https://huggingface.co/spaces/Saima109/code-switching-demo)

## How It Works

The user enters a sentence containing Roman Urdu, English, or both.

The application splits the sentence into individual words.

Each word is sent to the trained **XLM-RoBERTa model**, which predicts its language category.

The final result displays every detected word with its predicted label and shows the total number of words in each category.

## Example

### Input

```text
Aaj ka din bohot busy tha
```

### Output

| Word  | Predicted Language |
| ----- | ------------------ |
| Aaj   | Roman Urdu (URD)   |
| ka    | Roman Urdu (URD)   |
| din   | Roman Urdu (URD)   |
| bohot | Roman Urdu (URD)   |
| busy  | English (ENG)      |
| tha   | Roman Urdu (URD)   |

## Results

The model was evaluated using F1 scores for each language category.

| Label            | F1 Score |
| ---------------- | -------- |
| Roman Urdu (URD) | 0.949    |
| English (ENG)    | 0.917    |
| Mixed (MIX)      | 0.000    |

**Overall Accuracy: 99%**

The model performed strongly for Roman Urdu and English word classification.

The Mixed category received a lower score because of limited representation in the evaluation data.

## Features

* Detects Roman Urdu words
* Detects English words
* Supports mixed Roman Urdu–English sentences
* Performs word-level language classification
* Displays a label for each detected word
* Shows the total number of words in each category
* Provides an interactive web interface

## Technologies Used

* Python
* Hugging Face Transformers
* XLM-RoBERTa
* Gradio
* Hugging Face Spaces
* Hugging Face Datasets

## How to Run Locally

### 1. Clone the Repository

```bash
git clone https://github.com/saimamanzoor651/code-switching-codesaviours-si26-saima.git
```

### 2. Move into the Project Folder

```bash
cd code-switching-codesaviours-si26-saima
```

### 3. Install Required Packages

```bash
pip install gradio transformers torch datasets
```

### 4. Run the Application

```bash
python app.py
```

After running the command, open the local URL shown in the terminal.

## Project Structure

```text
code-switching-codesaviours-si26-saima/
│
├── app.py
├── dataset.csv
├── README.md
└── requirements.txt
```

## Built By

**Saima Manzoor** | **Code Saviours SI-26** | **2026**

