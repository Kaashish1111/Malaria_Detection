# Malaria_Detection
Binary image classification model to detect malaria-infected blood cells using CNN
# Malaria Cell Detection using CNN

A deep learning model that detects malaria-infected blood cells from microscopic images using a Convolutional Neural Network (CNN). Achieves **96% accuracy** on binary classification of infected vs uninfected cells.

---

## Problem Statement

Malaria diagnosis traditionally relies on manual microscopic examination of blood smears, which is time-consuming and requires trained personnel — a major bottleneck in low-resource settings. This project automates the detection process using deep learning, enabling faster and more scalable diagnosis.

---

## Dataset

- **Source:** [Cell Images for Detecting Malaria – Kaggle / NIH](https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria)
- **Total images:** 27,558 cell images
- **Classes:**
  - `Parasitized` — infected cells
  - `Uninfected` — healthy cells
- **Split:** 80% training / 20% testing

---

## Model Architecture

Built from scratch using TensorFlow/Keras:

```
Input (128x128x3)
→ Conv2D + ReLU + MaxPooling
→ Conv2D + ReLU + MaxPooling
→ Conv2D + ReLU + MaxPooling
→ Flatten
→ Dense (256) + Dropout (0.5)
→ Dense (1) + Sigmoid (binary output)
```

- **Optimizer:** Adam
- **Loss function:** Binary Crossentropy
- **Data augmentation:** horizontal flip, zoom, rotation (to reduce overfitting)

---

## Results

| Metric | Score |
|--------|-------|
| Accuracy | **96%** |
| Precision | -- |
| Recall | -- |
| F1-Score | -- |

> Fill in your actual precision/recall/F1 values from your classification report. Add your confusion matrix image below.

<!-- ![Confusion Matrix](results/confusion_matrix.png) -->

---

## Project Structure

```
malaria-detection/
│
├── dataset/                  # Cell images (parasitized / uninfected)
├── notebooks/
│   └── malaria_detection.ipynb
├── model/
│   └── malaria_cnn_model.h5  # Saved trained model
├── results/
│   └── confusion_matrix.png
├── train.py                  # Training script
├── predict.py                # Run prediction on new image
├── requirements.txt
└── README.md
```

---

## How to Run

### 1. Clone the repository
```bash
git clone https://github.com/Kaashish1111/malaria-detection.git
cd malaria-detection
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Train the model
```bash
python train.py
```

### 4. Predict on a new image
```bash
python predict.py --image path/to/cell_image.png
```

---

## Tech Stack

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Keras](https://img.shields.io/badge/Keras-red)
![NumPy](https://img.shields.io/badge/NumPy-1.x-lightblue)
![Matplotlib](https://img.shields.io/badge/Matplotlib-green)
![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-blue)

---

## Key Learnings

- Implemented CNN architecture from scratch for medical image classification
- Applied data augmentation techniques to improve model generalization
- Evaluated model using precision, recall, F1-score, and confusion matrix
- Achieved 96% accuracy through hyperparameter tuning

---

## Author

**Kashish Goyal**
- GitHub: [@Kaashish1111](https://github.com/Kaashish1111)
- LinkedIn: [kashishgoyal111](https://www.linkedin.com/in/kashishgoyal111/)

---

> If you found this useful, consider starring the repo!
