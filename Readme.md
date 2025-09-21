# NMT-RNN-CS224N-Assignment3

Sequence-to-sequence Neural Machine Translation (RNNs + Global Attention) implemented in PyTorch.  
This repository contains a single Jupyter notebook that implements and explains the full pipeline from tokenization and vocabulary construction to training, evaluation (BLEU) and beam-search decoding.

**This project is a personal implementation modified from Stanford's CS224N: _Natural Language Processing with Deep Learning_ — Assignment 3 (Neural Machine Translation with RNNs).**

---

## 📌 What's included
- `Neural_Machine_Translation_with_RNNs.ipynb` — A complete Jupyter Notebook implementing:
  - Subword/token handling (SentencePiece)
  - Vocabulary building (Vocab / VocabEntry)
  - `ModelEmbeddings` (source & target)
  - BiLSTM encoder and LSTMCell decoder
  - Global (Luong-style) attention
  - Combined-output projection, softmax vocabulary projection
  - Training loop, evaluation (BLEU), and beam search inference

> Note: Only the notebook file is included in the repository (as requested). Data files used in the original assignment (a4.zip) are not included here; follow the notebook instructions to obtain or generate the assignment data.

---

## ✨ Highlights
- Implements a full **Seq2Seq + Attention** NMT model (RNN-based).
- Clear, commented code mapping formulas → PyTorch implementation.
- Evaluation using BLEU; beam search decoding included.
- Useful as a learning resource or demonstration of the classic RNN + attention NMT pipeline.

---

## 🧭 How to run

Clone this repo:
```bash
  git clone https://github.com/wajason/Neural-Machine-Translation-RNN.git
  cd Neural-Machine-Translation-RNN
```

Open Neural_Machine_Translation_with_RNNs.ipynb and run the cells step-by-step!!


## 🧾 Notebook structure (quick outline)

1. Data & Tokenization — SentencePiece training / tokenization and autograder_read_corpus.

2. Vocabulary — VocabEntry, Vocab building, saving/loading.

3. Embedding — ModelEmbeddings (source & target).

4. Encoder — Bidirectional LSTM producing enc_hiddens.

5. Decoder — LSTMCell with attention (step()), combined-output projection.

6. Training — forward pass, loss computation (cross-entropy on gold words), optimization.

7. Evaluation — compute BLEU, and beam search for decoding.

8. Sanity checks & autograder compatibility stubs.


## 📈 Results

With default hyperparameters (not extensively tuned) the notebook successfully completes the assignment’s checks / autograder conditions (per personal test).

The notebook prints training/evaluation metrics and example translations. Results will vary by seed, hardware, and tokenization settings.


## ⚠️ Academic Integrity, License & Disclaimer

This repository is for personal study, learning, and reference purposes only.

If you reuse code from this notebook in a public project, please include appropriate attribution to CS224N and to any referenced papers.

## 📚 References (key)

1. Stanford CS224N: Natural Language Processing with Deep Learning — Assignment 3 (Neural Machine Translation).





