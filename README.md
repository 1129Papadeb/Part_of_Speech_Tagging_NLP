# Hidden Markov Model (HMM) with Viterbi Algorithm for POS Tagging

This implements a basic Hidden Markov Model (HMM) to perform Part-of-Speech (POS) tagging on sentences. The Viterbi algorithm is used to determine the most likely sequence of tags for a given input sentence.

---

## 📚 Description

The goal is to predict the most probable POS tags for a sequence of words based on a trained HMM using labeled training data.

- **Training Data**: Small set of manually tagged sentences with POS tags like `DET`, `NOUN`, `VERB`, and `ADV`.
- **Model**: Uses transition probabilities, emission probabilities, and start probabilities computed from the training data.
- **Prediction**: The Viterbi algorithm is applied to input test sentences to find the most likely sequence of tags.

---

## 📌 Training Data Example

The_DET cat_NOUN sleeps_VERB
A_DET dog_NOUN barks_VERB
The_DET dog_NOUN sleeps_VERB
My_DET dog_NOUN runs_VERB fast_ADV
A_DET cat_NOUN meows_VERB loudly_ADV
Your_DET cat_NOUN runs_VERB
The_DET bird_NOUN sings_VERB sweetly_ADV
A_DET bird_NOUN chirps_VERB


---

## 🧪 Test Sentences

These are the test sentences the model will tag:

1. `The cat meows`  
2. `My dog barks loudly`

---

## ✅ Sample Output

Sentence 1: The cat meows
Predicted Tags: ['DET', 'NOUN', 'VERB']

Sentence 2: My dog barks loudly
Predicted Tags: ['DET', 'NOUN', 'VERB', 'ADV']


> Note: The model uses a default low probability (1e-6) for unknown words not seen during training.

---

## 🧠 How It Works

1. **Training**:
    - Calculates start probabilities for each tag.
    - Calculates transition probabilities between tags.
    - Calculates emission probabilities of words given a tag.

2. **Viterbi Algorithm**:
    - Uses dynamic programming to find the best tag sequence with the highest probability.
