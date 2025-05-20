# Multi-Label Hate Speech Detection

## Project Overview

This project focuses on detecting hate speech in text, particularly multi-label hate speech classification on social media comments. Hate speech is communication that attacks individuals or groups based on characteristics such as race, ethnicity, gender, religion, or sexual orientation.

Due to the large volume of social media content, automated methods using machine learning (ML) and deep learning (DL) techniques are necessary for effective hate speech detection. This project explores various feature selection techniques and model architectures including classical ML algorithms and state-of-the-art models such as BERT and Bi-LSTM.

---

## Motivation

- The rise of social media has made hate speech a critical issue affecting millions.
- Manual moderation is impractical due to scale, necessitating automated detection.
- Accurate and efficient ML methods can help curb online hate speech.

---

## Datasets Used

- **ETHOS Dataset**: Multi-label hate speech annotations from YouTube and Reddit comments (433 comments, 8 labels).
- **Jigsaw Toxic Comment Classification Dataset**: Large-scale Wikipedia comments dataset labeled for toxicity across 6 categories (~160,000 comments).

---

## Methodology

### Data Preprocessing
- Lowercasing text
- Expanding contractions (e.g., "don't" → "do not")
- Removing punctuation, digits, and stopwords
- Lemmatization to reduce words to their dictionary forms

### Feature Representation
- Word embeddings using BERT, GloVe, and Word2Vec
- Keras tokenizer for word vectorization

### Models Implemented
- **Bi-LSTM**: Bidirectional LSTM networks to capture context from past and future tokens
- **LSTM**: Standard Long Short-Term Memory networks for sequential data
- **Dense Layers**: Fully connected neural network layers for classification
- **ULMFit**: Transfer learning approach for NLP fine-tuning

---

## Results and Observations

- Preprocessing improved model accuracy and reduced loss across datasets.
- Small dataset size (ETHOS) posed challenges; results were better with larger Jigsaw dataset.
- Classical ML with fine-tuned features performed comparably with deep learning models.
- Pretrained embeddings like BERT enhanced model understanding of context.
- Models struggled with overfitting on smaller datasets without data augmentation.

---

## Challenges

- Limited size of ETHOS dataset restricted performance.
- Some models showed high loss and low accuracy without proper preprocessing.
- Cultural and linguistic variations in hate speech made classification complex.

---

## Future Work

- Implement text augmentation techniques to increase dataset size:
  - Back Translation
  - Easy Data Augmentation (synonym replacement)
  - Use of NLP augmentation libraries for character, word, and sentence-level augmentation.
- Explore more sophisticated architectures and ensemble methods.
- Incorporate more multilingual datasets for broader coverage.

---

