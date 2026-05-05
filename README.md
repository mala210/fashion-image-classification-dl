# Fashion Image Classification using Deep Learning

## Overview

This project addresses fashion image classification using deep learning. Two approaches are implemented and compared:

1. A Convolutional Neural Network (CNN) built from scratch.
2. A transfer learning model based on MobileNetV2.

The objective is to evaluate which approach performs better on a relatively simple image dataset.

---

## Dataset

* Fashion-MNIST
* 70,000 grayscale images
* 10 classes (e.g., T-shirt/top, Trouser, Dress, etc.)
* Image size: 28×28

---

## Methodology

### Data Preprocessing

* Pixel normalization to the range [0, 1]
* Conversion from grayscale to RGB for the transfer learning model

### Model 1: Proposed CNN

* Convolutional layers with ReLU activation
* Batch Normalization
* MaxPooling layers
* Dropout for regularization
* Data augmentation (flip, rotation, zoom)

### Model 2: Transfer Learning (MobileNetV2)

* Pretrained MobileNetV2 (ImageNet)
* Frozen base layers
* Custom classification head (Global Average Pooling + Dense layers)

---

## Training

* Optimizer: Adam
* Loss: Sparse Categorical Crossentropy
* Early Stopping based on validation accuracy

---

## Results

| Model            | Test Accuracy |
| ---------------- | ------------- |
| Proposed CNN     | 91.3%         |
| MobileNetV2 (TL) | 89.2%         |

The CNN model achieved higher accuracy than the transfer learning model. Most errors occur between visually similar classes (e.g., shirt vs t-shirt).

---

## Evaluation

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix
* Training curves (validation accuracy and loss)

---

## Key Insight

Model performance depends on dataset characteristics. For small, low-resolution grayscale datasets, a well-designed CNN can outperform transfer learning models pretrained on large, high-resolution color datasets.

---

## Technologies

* Python
* TensorFlow / Keras
* NumPy
* Matplotlib


