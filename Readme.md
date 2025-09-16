# NMT-RNN-CS224N-Assignment3

Sequence-to-sequence Neural Machine Translation (RNNs + Global Attention) implemented in PyTorch.  
This repository contains a single Jupyter notebook that implements and explains the full pipeline from tokenization and vocabulary construction to training, evaluation (BLEU) and beam-search decoding.

**This project is a personal implementation modified from Stanford's CS224N: _Natural Language Processing with Deep Learning_ — Assignment 3 (Neural Machine Translation with RNNs).**

---

# 📌 What's included
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

# ✨ Highlights
- Implements a full **Seq2Seq + Attention** NMT model (RNN-based).
- Clear, commented code mapping formulas → PyTorch implementation.
- Evaluation using BLEU; beam search decoding included.
- Useful as a learning resource or demonstration of the classic RNN + attention NMT pipeline.

---

# 🧭 How to run

Clone this repo:
'''
  git clone https://github.com/<your-username>/NMT-RNN-CS224N-Assignment3.git
  cd NMT-RNN-CS224N-Assignment3
'''

Prepare the assignment data:

The original CS224N assignment package (a4.zip) contains sample source/target files and SentencePiece examples. Follow the notebook cell instructions to train SentencePiece models or to use provided files if you have a4.zip.

Do not upload or share any data you do not have rights to—see the Disclaimer below.

Launch the notebook:

jupyter lab   # or jupyter notebook


Open Neural_Machine_Translation_with_RNNs.ipynb and run the cells step-by-step.

# 🧾 Notebook structure (quick outline)

Data & Tokenization — SentencePiece training / tokenization and autograder_read_corpus.

Vocabulary — VocabEntry, Vocab building, saving/loading.

Embedding — ModelEmbeddings (source & target).

Encoder — Bidirectional LSTM producing enc_hiddens.

Decoder — LSTMCell with attention (step()), combined-output projection.

Training — forward pass, loss computation (cross-entropy on gold words), optimization.

Evaluation — compute BLEU, and beam search for decoding.

Sanity checks & autograder compatibility stubs.

# 📈 Results

With default hyperparameters (not extensively tuned) the notebook successfully completes the assignment’s checks / autograder conditions (per personal test).

The notebook prints training/evaluation metrics and example translations. Results will vary by seed, hardware, and tokenization settings.

# ⚠️ Academic Integrity, License & Disclaimer

This repository is for personal study, learning, and reference purposes only.

Not affiliated with nor endorsed by Stanford University or the CS224N course staff.

Do not use this repository as a substitute for your own assignment submissions. If you are enrolled in CS224N (or any course), do not submit this notebook or derived work as your own.

Data & licensing: This repo does not include assignment datasets. If you download original course data or any other dataset, ensure you have the right to use and redistribute it and comply with its license. Do not commit proprietary or third-party data into this public repo.

If you reuse code from this notebook in a public project, please include appropriate attribution to CS224N and to any referenced papers.

# 📚 References (key)

Stanford CS224N: Natural Language Processing with Deep Learning — Assignment 3 (Neural Machine Translation).

Luong, Pham & Manning (2015), Effective Approaches to Attention-based Neural Machine Translation (Luong attention).

General seq2seq literature (Bahdanau et al., Luong et al.).
