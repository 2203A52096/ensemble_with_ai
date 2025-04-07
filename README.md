# 🧥 Fashion Outfit Classification using CNN, MobileNetV2, and EfficientNetB0

This project classifies fashion outfit images into 5 categories using deep learning models. A custom CNN, MobileNetV2, and EfficientNetB0 are trained and compared.
---

## 📁 Dataset

- Custom dataset organized by folders:
  - `hoodies/`, `skirts/`, `shorts/`, `jeans/`, `dress/`
- Around 300 images per class
- Resized to (200x200)
- Normalized using appropriate preprocessing functions
- 80/20 split using `ImageDataGenerator` (`validation_split=0.2`)

---

## 🧠 Models Used

### 1. CNN
- Custom architecture with Conv2D, MaxPooling, Dropout, and Dense layers
- Lightweight and good for baseline

### 2. MobileNetV2
- Pretrained on ImageNet
- Used as a frozen feature extractor
- Added custom classification head

### 3. EfficientNetB0
- Pretrained on ImageNet
- Lightweight, efficient model
- Added custom classification head

---

## 🏃 Training Configuration

| Parameter     | Value        |
|---------------|--------------|
| Image Size    | (200, 200)   |
| Batch Size    | 16 *(fixed)* |
| Epochs        | Up to 10     |
| Optimizer     | Adam         |
| Loss          | Categorical Crossentropy |

---

## 📊 Evaluation Metrics

- **Accuracy**
- **Classification Report** (precision, recall, f1-score)
- **Confusion Matrix**

---

## 📈 Statistical Tests

We analyzed model accuracy across different **epochs** using:

- ✅ **F-Test** – for comparing variances  
- ✅ **t-Test** – for comparing means between two epochs  
- ✅ **ANOVA** – for comparing means across multiple epochs  

These tests help determine if accuracy improvements over time are statistically significant.

---
