# NLP Emotion Recognition & Irony Detection

> Neural Network models for tweet emotion classification and irony detection

![Python](https://img.shields.io/badge/Python-3.10-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.x-red)
![HuggingFace](https://img.shields.io/badge/Transformers-4.x-orange)
![License](https://img.shields.io/badge/License-MIT-green)

---

## Overview

This project implements two NLP neural network models for Twitter text analysis:

| Task | Type | Classes |
|------|------|---------|
| **Emotion Recognition** | Multi-class Classification | anger, joy, optimism, sadness |
| **Irony Detection** | Binary Classification | ironic, non-ironic |

---

## Project Architecture

```
Input Tweets
      │
      ▼
  Text Preprocessing
  ├── Emoji Handling
  ├── URL/Username Removal
  ├── Stopwords Removal
  └── Tokenization
      │
      ▼
  Feature Extraction (BERT-based)
      │
      ▼
  Neural Network Training
  ├── Emotion Detection Model
  │   └── Dense(4) + Softmax
  └── Irony Detection Model
      └── Dense(1) + Sigmoid
```

---

## Tech Stack

| Category | Library |
|----------|---------|
| **Deep Learning** | PyTorch |
| **NLP** | Transformers, NLTK |
| **Data Processing** | Pandas, NumPy |
| **ML Utilities** | Scikit-learn |
| **Visualization** | Matplotlib, Seaborn |
| **Text** | Emoji |

---

## Dataset Structure

```
datasets/
├── emotion/
│   ├── train_text.txt
│   ├── train_labels.txt
│   ├── val_text.txt
│   ├── val_labels.txt
│   ├── test_text.txt
│   └── mapping.txt
└── ironyDataset/
    ├── train_text.txt
    ├── train_labels.txt
    ├── val_text.txt
    ├── val_labels.txt
    ├── test_text.txt
    └── mapping.txt
```

### Emotion Classes

| Label | Emotion |
|-------|---------|
| 0 | anger |
| 1 | joy |
| 2 | optimism |
| 3 | sadness |

### Irony Labels

| Label | Class |
|-------|-------|
| 0 | non-ironic |
| 1 | ironic |

---

## Setup

### 1. Clone the repository

```bash
git clone https://github.com/StefoXCaffeine/NLP-EmotionRecognition-IronyDetection.git
cd NLP-EmotionRecognition-IronyDetection
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the notebooks

```bash
jupyter notebook Emotion_Detection.ipynb
jupyter notebook Irony_Detection.ipynb
```

---

## Notebooks

| File | Description |
|------|-------------|
| `Emotion_Detection.ipynb` | Multi-class emotion classification model |
| `Irony_Detection.ipynb` | Binary irony detection model |

---

## Evaluation Metrics

| Task | Metric |
|------|--------|
| Emotion Recognition | Macro F1-Score |
| Irony Detection | F1-Score |

---

## License

MIT License - see `LICENSE` file for details.

---

## Author

**StefoXCaffeine**

- GitHub: [@StefoXCaffeine](https://github.com/StefoXCaffeine)
- LinkedIn: [linkedin.com/in/stefano-corrao](https://www.linkedin.com/in/stefano-corrao)

---

*If you find this project useful, leave a star!*
