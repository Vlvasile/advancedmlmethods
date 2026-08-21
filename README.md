# Advanced ML Methods

Collection of exercises and small projects I worked through while studying advanced machine learning topics — mostly classical ML techniques, Bayesian neural networks, and a bit of NLP. Not a single polished product, more of a lab notebook of things I tried and learned from.

## What's in here

### `classical-ml/`
Classification and regression basics, plus stacking ensembles (combining several models into one). Datasets: phone classification, mushroom classification, housing prices.

### `bayesian-neural-networks/`
This is the part I found most interesting. Instead of a normal neural network that outputs a single number, a Bayesian NN (using `torchbnn`) outputs a distribution — so you get some sense of how confident the model actually is. I tried it on regression (housing), and two classification setups (categorical and ordinal, on the Iris dataset).

### `nlp-text-classification/`
Classic text classification — Naive Bayes on a news dataset and a product review dataset. Nothing fancy, just wanted to get comfortable with the standard NLP preprocessing pipeline (tokenizing, vectorizing, etc.) before moving to anything more complex.

### `nlp-text-generation/`
Trained a Bidirectional LSTM to generate text, one word at a time, based on a corpus of poetry (~3,800 unique words). Ran this in Google Colab. Honestly, training got cut off before it finished all 150 epochs (Colab disconnected around epoch 105), but it had already reached about 71% training accuracy at that point, so I kept the notebook as-is rather than pretending it was a finished run.

### `aurabot-chatbot/`
A simple intent-based chatbot — you type something, it matches your message against a set of predefined intents (greeting, goodbye, etc.) using a small Keras model, and replies accordingly. Includes a Gradio interface so you can actually chat with it instead of just reading code.

## Honest notes

- These started as coursework exercises, not from-scratch personal projects — I picked the datasets and approaches myself within each assignment, but the topics/structure came from a course.
- The `news.csv` and `PoetryFoundationData.csv` datasets aren't included in this repo (they're large public datasets — news classification and poetry, both easy to find on Kaggle) — the notebooks assume you download them separately if you want to rerun everything.
- Not every notebook has a fully "finished" result — some are more exploratory than others. I'd rather leave that visible than dress it up.

## Tech Stack

Python, scikit-learn, PyTorch, torchbnn, TensorFlow/Keras, pandas, Gradio

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook
```
Each folder is self-contained — open whichever notebook you're curious about.
