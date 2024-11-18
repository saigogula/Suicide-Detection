# Suicide Detection Using Machine Learning

## Overview

This project aims to address the critical issue of suicide prevention by leveraging machine learning to detect suicidal tendencies through text analysis. By analyzing social media posts, the project identifies language patterns and behavioral markers that signal mental health struggles. The goal is to provide a proactive tool for early intervention and support.

## Features

- **Text Classification Model**: Utilizes a fine-tuned BERT model for accurate detection of suicidal and depressive content.
- **Dataset**: Includes data from Reddit's `SuicideWatch`, `depression`, and `teenagers` subreddits, ensuring a balanced and comprehensive training set.
- **Robust Training Pipeline**: Implements advanced techniques for data preprocessing, model training, and evaluation.
- **Real-Time Monitoring**: Tracks training loss and evaluation accuracy with visualization capabilities.
- **Efficient Inference**: Provides GPU-accelerated predictions with batch processing support.

---

## Dataset

The dataset consists of posts collected via the Pushshift API, labeled as follows:

- **SuicideWatch**: Posts indicating suicidal tendencies.
- **Depression**: Posts expressing depressive symptoms.
- **Teenagers**: Non-suicidal posts for contrast.

### Data Processing Steps:
- Tokenization using BERT tokenizer.
- Sequence truncation and dynamic padding.
- Train-test split with an 80/20 ratio.

---

## Model Architecture

The text classification model uses the **BERT (Bidirectional Encoder Representations from Transformers)** architecture:

- **Base Model**: `bert-base-uncased`
- **Output Layer**: Binary classification (suicidal or non-suicidal)
- **Training Configuration**:
  - Epochs: 3
  - Batch size: 8
  - Warmup steps: 500
  - Weight decay: 0.01

### Performance Metrics:
- Training and evaluation loss
- Step-wise accuracy tracking
- Visualization of loss and accuracy progression

---

## Implementation Details

### Dependencies

- Python 3.8+
- PyTorch
- Transformers library
- Pandas
- scikit-learn

### How to Run

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/suicide-detection
   cd suicide-detection
2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
3. **Prepare Dataset**:
   ```bash
   python preprocess.py
4. **Train the Model**:
   ```bash
   python train.py
5. **Evaluate the Model**:
   ```bash
   python evaluate.py
6. **Run Inference**:
   ```bash
   python inference.py --input "Your test input here"

## Results

The model achieved the following results:

| **Dataset Size** | **Accuracy** |
|-------------------|--------------|
| 500 Samples       | 81%          |
| 7,500 Samples     | 92%          |
| 15,000 Samples    | 98%          |

### Key Insights

- Early detection through text analysis can be a transformative tool for mental health professionals.
- Patterns such as work overload and excessive involvement in activities were identified as key indicators of distress.


You can get the datasets frrom the notebook folder
