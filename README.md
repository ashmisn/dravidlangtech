
# Multimodal Code-Mixed Meme Moderation Model
Authors: Ashmi S N,Nimisha M Iyer, Balasubramanian Palani, Jobin Jose.
## Overview
This project presents a deep learning-based multimodal framework for detecting harmful content in code-mixed memes under ultra-low-resource settings. The model combines textual and visual features using gated fusion and imbalance-aware learning strategies to improve moderation performance on minority and slang-heavy data.

The system is specifically designed to handle:
* Code-mixed language (e.g., Hinglish, Malayalam)
* Slang and informal expressions
* OCR-extracted meme text
* Severe class imbalance

---

## Model Architecture
The framework consists of four core components:

### 1. Text Processing
* Bilingual OCR for meme text extraction
* Text normalization for slang and code-mixed tokens
* Transformer-based text encoder (e.g., IndicBERT)

### 2. Image Processing
* Pretrained vision encoder (e.g., Vision Transformer / ViT) for visual feature extraction
* Robust visual embedding generation

### 3. Multimodal Fusion
* Gated fusion mechanism
* Adaptive feature weighting between text and image to filter OCR noise

### 4. Imbalance Handling
* Asymmetric loss function
* Threshold optimization
* Minority-aware training strategy

---

## Project Structure
```text
├── bestmodel.ipynb        # Main training and evaluation notebook
├── dataset/               # Dataset directory (not included in repo)
├── models/                # Saved model checkpoints
├── utils/                 # Helper functions
└── README.md              # Project documentation

```

---

## Installation

**Requirements:**

* Python 3.8+
* PyTorch
* torchvision
* transformers
* scikit-learn
* numpy
* pandas
* matplotlib
* opencv-python
* tqdm

**Install dependencies:**

```bash
pip install -r requirements.txt

```

---

## How to Run

1. **Clone the repository:**
```bash
git clone [https://github.com/ashmisn/dravidlangtech.git](https://github.com/ashmisn/dravidlangtech.git)
cd dravidlangtech

```


2. **Add Data:** Place your training and testing data inside the `dataset/` directory.
3. **Execute the Pipeline:** Open and run `bestmodel.ipynb`.

The notebook sequentially executes:

* Data preprocessing
* OCR integration
* Model training
* Evaluation
* Post-training threshold tuning

---

## Evaluation Metrics

Due to the severe class imbalance typical in meme moderation datasets, the model is evaluated using multiple metrics:

* Precision
* Recall
* F1-Score (Macro & Weighted)
* ROC-AUC
* Confusion Matrix

*Note: Post-training threshold tuning is actively applied to the decision boundary to optimize minority class detection.*

---

## Key Features

* Handles code-mixed and slang-heavy regional content
* Dynamically combines visual and textual modalities
* Highly robust against extreme class imbalance
* Utilizes a mathematically robust gated multimodal fusion mechanism
* Specifically designed and optimized for ultra-low-resource environments

---

## Potential Improvements

* Enhanced OCR fine-tuning for low-resolution, heavily stylized memes
* Synthetic data augmentation targeted specifically at minority classes
* Incorporation of domain-specific slang lexicons
* Lightweight model distillation for rapid deployment

---

## Use Cases

* Social media content moderation
* Hate speech and cyberbullying detection in memes
* Code-mixed language analysis
* Multimodal abusive content detection

```




