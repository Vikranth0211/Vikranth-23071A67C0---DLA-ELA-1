# Track 1 — Phishing & Malicious Email Classifier (Deep Learning ELA-1)

Dept. of CSE- DS, Cys and AI&DS · Security-Focus Track.

**Name:** P. Adi Sai Vikranth · **Roll No:** 23071A67C0

## Colab Notebook
Colab Link: https://colab.research.google.com/drive/14uYCtU_U3eI4GYnsUrPZkwyRG7wPggDP?authuser=1#scrollTo=FDKquXfWMkiS
End-to-end pipeline for phishing email detection using Deep Learning, including preprocessing, training, evaluation, and live inference.

## Files

| File                                    | Purpose                                   |
| --------------------------------------- | ----------------------------------------- |
| `phishing_email_classifier_colab.ipynb` | Complete TensorFlow/Keras implementation. |
| `phishing_email_classifier_report.pdf`  | 3-page project report.                    |
| `synthetic_email_dataset.csv`           | 1,800 labelled synthetic emails.          |

## Dataset

The dataset contains **1,800 emails**:

* 900 Legitimate
* 900 Phishing/Malicious

The dataset is generated programmatically and requires no external download.

## Preprocessing

```text
Raw Email → Cleaning → Tokenisation → Encoding → Padding → Model
```

Email text is cleaned, tokenised, converted into integer sequences, and padded/truncated to a fixed length.

## Model

**Bidirectional LSTM (TensorFlow/Keras)**

```text
Embedding (64)
      ↓
BiLSTM (64)
      ↓
GlobalMaxPool1D
      ↓
Dropout (0.5)
      ↓
Dense (32, ReLU)
      ↓
Dropout (0.3)
      ↓
Sigmoid Output
```

**Optimizer:** Adam
**Loss:** Binary Cross-Entropy
**Early Stopping:** Patience = 3

## Evaluation

Metrics used:
* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix
* Loss & Accuracy Curves

**Test F1-Score:** ~0.99 on the seeded synthetic dataset.

> Performance on synthetic data does not represent real-world phishing detection accuracy.

## Technologies

**Python · TensorFlow/Keras · Google Colab · NumPy · Pandas · Scikit-learn · Matplotlib · Seaborn**

## Author

**P. Adi Sai Vikranth**
**Roll No:** 23071A67C0
