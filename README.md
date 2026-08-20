# Code Switching NLP | Code Saviours SI-26 | Saima Manzoor
# Roman Urdu–English Code Switching Detector

A Machine Learning model that identifies each word in a sentence as Roman Urdu, English, or Mixed.

## Why This Matters

People in Pakistan frequently mix Roman Urdu and English while chatting, posting on social media, and communicating online.

For example:

> Aaj ka din bohot busy tha, had 3 meetings back to back.

Traditional language processing systems can struggle with this type of mixed-language text because different languages appear in the same sentence.

This project identifies the language of each word as:

- **URD** — Roman Urdu
- **ENG** — English
- **MIX** — Mixed

This can help support future work in Urdu NLP, language identification, text analysis, and code-switching research.

## Live Demo

Try the live application here:

[Open the Hugging Face Space](https://huggingface.co/spaces/Saima109/code-switching-demo)

## How It Works

The user enters a sentence containing Roman Urdu, English, or both.

The application splits the sentence into words and sends them to my trained XLM-RoBERTa model.

The model analyzes each word and predicts whether it belongs to Roman Urdu, English, or the Mixed category.

The final result displays every detected word with its predicted language label, along with a summary showing the total number of words in each category.

## Results

The model was evaluated using F1 scores for each language category.

| Label | F1 Score |
|---|---:|
| Roman Urdu (URD) | 0.9949 |
| English (ENG) | 0.9917 |
| Mixed (MIX) | 0.0000 |

**Overall Accuracy: 99%**

The model performed strongly on Roman Urdu and English word classification.

The MIX category received a lower score because of limited representation in the evaluation data.

## How to Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/saimamanzoor651/code-switching-codesaviours-si26-saima.gi
