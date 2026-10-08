# Exploring Word Representations: From Traditional Embeddings to Transformers

## 📌 About the Project

This project is part of the **24ADI306 – Deep Learning** self-learning activity.

The project explores different ways of converting words and sentences into **numerical representations** that computers can understand.

The techniques are studied from simple methods to advanced Transformer-based methods.

### Techniques Used

- One-Hot Encoding
- Bag of Words (BoW)
- TF-IDF
- Word2Vec
- FastText
- Keras Embedding
- BERT
- PCA Visualization

---

## 🎯 Objectives

The main objectives of this project are:

- Understand how text is converted into numbers.
- Study traditional text representation methods.
- Implement Word2Vec and FastText.
- Understand how BERT represents words based on context.
- Find similar words using embeddings.
- Visualize word embeddings.
- Compare traditional, Word2Vec and BERT representations.

---

## 🧠 What We Learned

### Traditional Methods

**One-Hot Encoding**  
Represents each word using a binary vector. It is simple but does not understand word meaning.

**Bag of Words**  
Counts how often words occur in a document.

**TF-IDF**  
Finds how important a word is in a document.

---

### Word2Vec

Word2Vec converts words into numerical vectors based on the words that appear around them.

It can find words that have similar meanings.

For example:

```text
machine → learning
learning → model
python → programming
```

---

### FastText

FastText is similar to Word2Vec but also uses parts of words.

This helps it handle:

- Rare words
- New words
- Misspelled words
- OOV (Out-of-Vocabulary) words

---

### Keras Embedding

The Keras Embedding layer converts words into small numerical vectors that can be learned by a neural network.

---

### BERT

BERT is a Transformer-based model.

The main advantage of BERT is that it understands the **context of a word**.

For example:

```text
I deposited money in the bank.

We sat near the river bank.
```

The word **bank** has different meanings in these two sentences.

BERT can understand this difference.

---

## 🔬 Experiments

The following experiments were performed:

### 1. TF-IDF

Generated TF-IDF representations for the dataset.

### 2. Word2Vec

Trained a Skip-gram Word2Vec model and found the **five most similar words** for selected words.

### 3. FastText

Tested FastText with rare and unseen words to study its OOV handling.

### 4. Keras Embedding

Generated word embeddings using the TensorFlow/Keras Embedding layer.

### 5. BERT

Used BERT to compare the word **"bank"** in different sentences.

### 6. Visualization

Used **PCA** to visualize Word2Vec and FastText embeddings.

---

## 📊 Simple Comparison

| Method | Main Idea | Understands Meaning? | Understands Context? |
|---|---|---|---|
| One-Hot | Binary representation | ❌ | ❌ |
| BoW | Word counts | ❌ | ❌ |
| TF-IDF | Word importance | Limited | ❌ |
| Word2Vec | Word meaning | ✅ | ❌ |
| FastText | Word + subwords | ✅ | ❌ |
| BERT | Word meaning + context | ✅ | ✅ |

---

## 📈 Embedding Visualization

PCA was used to convert the high-dimensional embeddings into 2D plots.

The plots help us see which words are close to each other in the embedding space.

### Visualizations Included

- Word2Vec PCA
- FastText PCA

---

## 🛠️ Tools Used

- Python
- Google Colab
- Jupyter Notebook
- Scikit-learn
- Gensim
- TensorFlow/Keras
- Hugging Face Transformers
- Matplotlib

---



## 📌 Main Result

The project shows how word representation techniques have developed:

```text
One-Hot
   ↓
BoW
   ↓
TF-IDF
   ↓
Word2Vec
   ↓
FastText
   ↓
BERT
```

Simple methods mainly represent **word frequency**, while Word2Vec and FastText learn **word relationships**. BERT goes further by understanding the **context in which a word is used**.

---

## 🎓 Learning Outcome

After completing this project, we understood:

- The difference between traditional and neural word representations.
- How Word2Vec creates word embeddings.
- How FastText handles unseen words.
- How BERT understands context.
- How cosine similarity can find similar words.
- How PCA can be used to visualize embeddings.

---
