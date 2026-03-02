Multimodal Code-Mixed Meme Moderation Model
📌 Overview

This project presents a deep learning–based multimodal framework for detecting harmful content in code-mixed memes under ultra-low-resource settings. The model combines textual and visual features using gated fusion and imbalance-aware learning strategies to improve moderation performance on minority and slang-heavy data.

The system is specifically designed to handle:

Code-mixed language (e.g., Hinglish)

Slang and informal expressions

OCR-extracted meme text

Severe class imbalance

🧠 Model Architecture

The framework consists of the following components:

1️⃣ Text Processing

Bilingual OCR for meme text extraction

Text normalization for slang and code-mixed tokens

Transformer-based text encoder

2️⃣ Image Processing

Pretrained CNN/vision encoder for visual feature extraction

Robust visual embedding generation

3️⃣ Multimodal Fusion

Gated fusion mechanism

Adaptive feature weighting between text and image

4️⃣ Imbalance Handling

Asymmetric loss function

Threshold optimization

Minority-aware training strategy

📂 Project Structure
├── bestmodel.ipynb        # Main training and evaluation notebook
├── dataset/               # Dataset directory (not included)
├── models/                # Saved model checkpoints
├── utils/                 # Helper functions
└── README.md              # Project documentation
⚙️ Installation
Requirements

Python 3.8+

PyTorch

torchvision

transformers

scikit-learn

numpy

pandas

matplotlib

opencv-python

tqdm

Install dependencies:

pip install -r requirements.txt
🚀 How to Run

Clone the repository.

Place the dataset inside the dataset/ directory.

Open and run:

bestmodel.ipynb

The notebook contains:

Data preprocessing

OCR integration

Model training

Evaluation

Threshold tuning

📊 Evaluation Metrics

Due to severe class imbalance, multiple evaluation metrics are used:

Precision

Recall

F1-Score (Macro & Weighted)

ROC-AUC

Confusion Matrix

Threshold tuning is applied to optimize minority class detection.

🏆 Key Features

✔ Handles code-mixed and slang-heavy content
✔ Combines visual and textual modalities
✔ Robust against class imbalance
✔ Uses gated multimodal fusion
✔ Designed for low-resource environments

📈 Potential Improvements

Enhanced OCR fine-tuning for low-resolution memes

Data augmentation for minority classes

Incorporation of domain-specific slang lexicons

Lightweight model distillation for deployment

📌 Use Cases

Social media content moderation

Hate speech detection in memes

Code-mixed language analysis

Multimodal abusive content detection
