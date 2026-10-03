# Comparative Analysis of RNN, LSTM, and GRU for Sentiment Analysis

## Project Overview

This project presents a comparative analysis of three recurrent deep learning models — **Simple RNN, LSTM, and GRU** — for sentiment analysis.

The **IMDB Movie Reviews dataset** is used to classify movie reviews as **positive or negative**. The models are trained and evaluated using Accuracy, Precision, Recall, F1-Score, and Training Time.

The experimental results show that **GRU achieved the highest overall classification performance**, with an accuracy of **87.08%** and an F1-Score of **86.88%**.

## Objectives

* Select a sentiment analysis dataset.
* Perform text preprocessing.
* Apply tokenization and padding.
* Implement Simple RNN, LSTM, and GRU models.
* Train and evaluate the models.
* Compare Accuracy, Precision, Recall, F1-Score, and Training Time.
* Analyze the results.
* Identify the best-performing model.

## Dataset

### IMDB Movie Reviews Dataset

The IMDB dataset contains **50,000 movie reviews** for binary sentiment classification.

* Training samples: 25,000
* Testing samples: 25,000
* Positive sentiment: 1
* Negative sentiment: 0
* Vocabulary size: 10,000 words
* Maximum sequence length: 200 tokens

## Preprocessing

The following preprocessing steps were performed:

1. Load the IMDB dataset.
2. Limit the vocabulary to the 10,000 most frequent words.
3. Convert reviews into numerical sequences.
4. Apply padding to make each sequence 200 tokens long.
5. Use 20% of the training data for validation.

## Models

### Simple RNN

Simple RNN processes the text sequentially and maintains information from previous time steps.

**Architecture:**

`Input → Embedding → Simple RNN → Dense → Output`

### LSTM

LSTM uses memory cells and gates to retain important information over longer sequences.

**Architecture:**

`Input → Embedding → LSTM → Dense → Output`

### GRU

GRU is a gated recurrent architecture with a simpler structure than LSTM.

**Architecture:**

`Input → Embedding → GRU → Dense → Output`

## Experimental Configuration

| Parameter           | Value               |
| ------------------- | ------------------- |
| Dataset             | IMDB Movie Reviews  |
| Vocabulary Size     | 10,000              |
| Sequence Length     | 200                 |
| Embedding Dimension | 128                 |
| Recurrent Units     | 64                  |
| Optimizer           | Adam                |
| Loss Function       | Binary Crossentropy |
| Epochs              | 5                   |
| Batch Size          | 128                 |
| Output Activation   | Sigmoid             |

## Evaluation Metrics

* **Accuracy:** Percentage of correctly classified reviews.
* **Precision:** Measures the correctness of positive predictions.
* **Recall:** Measures how many actual positive reviews were identified.
* **F1-Score:** Provides a balance between Precision and Recall.
* **Training Time:** Measures the time required to train each model.

## Results

| Model |   Accuracy |  Precision |     Recall |   F1-Score | Training Time |
| ----- | ---------: | ---------: | ---------: | ---------: | ------------: |
| RNN   |     52.83% |     52.98% |     50.28% |     51.59% |      175.57 s |
| LSTM  |     82.23% | **89.13%** |     73.41% |     80.51% |      402.42 s |
| GRU   | **87.08%** |     88.24% | **85.55%** | **86.88%** |      483.24 s |

## Result Analysis

The Simple RNN achieved the lowest classification performance with an accuracy of **52.83%**, but it required the shortest training time.

LSTM achieved significantly better performance with **82.23% accuracy** and the highest precision of **89.13%**.

GRU achieved the highest **accuracy (87.08%)**, **recall (85.55%)**, and **F1-score (86.88%)**. However, it required the longest training time of **483.24 seconds**.

## Best-Performing Model

**GRU** was identified as the best-performing model based on the overall classification metrics.

Its results were:

* Accuracy: **87.08%**
* Precision: **88.24%**
* Recall: **85.55%**
* F1-Score: **86.88%**
* Training Time: **483.24 seconds**

Although LSTM achieved slightly higher precision, GRU provided better overall classification performance.

## Project Workflow

`IMDB Dataset → Preprocessing → Tokenization → Padding → RNN/LSTM/GRU → Training → Evaluation → Comparison → Best Model`

## Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* Scikit-learn
* Matplotlib
* Google Colab / Jupyter Notebook

## Project Structure

```text
RNN-LSTM-GRU-Sentiment-Analysis/
│
├── RNN_LSTM_GRU_Sentiment_Analysis.ipynb
├── RNN_LSTM_GRU_Sentiment_Analysis.py
├── RNN_LSTM_GRU_Comparison.csv
├── RNN_LSTM_GRU_Report.pdf
└── README.md
```

## How to Run

### Install Dependencies

```bash
pip install tensorflow numpy pandas scikit-learn matplotlib
```

### Run the Notebook

Open `RNN_LSTM_GRU_Sentiment_Analysis.ipynb` using Google Colab or Jupyter Notebook and execute the cells in order.

The notebook will:

1. Load the dataset.
2. Preprocess the reviews.
3. Build the RNN, LSTM, and GRU models.
4. Train the models.
5. Evaluate their performance.
6. Generate the comparison results.

## Limitations

* Only binary sentiment classification is performed.
* The vocabulary is limited to 10,000 words.
* Reviews are limited to 200 tokens.
* Only five training epochs are used.
* Transformer-based models are not included.

## Future Enhancements

* Implement Bidirectional LSTM and GRU.
* Use pretrained word embeddings such as Word2Vec or GloVe.
* Add attention mechanisms.
* Perform hyperparameter tuning.
* Compare with transformer models such as BERT.
* Extend the system to multiclass sentiment classification.

## Conclusion

This project compares Simple RNN, LSTM, and GRU models for sentiment analysis using the IMDB Movie Reviews dataset.

The results demonstrate that **GRU achieved the best overall classification performance**, with an accuracy of **87.08%** and an F1-Score of **86.88%**. Simple RNN had the shortest training time, while LSTM achieved the highest precision.

The experiment demonstrates the differences between recurrent architectures and the trade-off between classification performance and training time.

