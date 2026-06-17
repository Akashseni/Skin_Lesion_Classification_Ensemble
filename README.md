# 🩺 Skin Lesion Classification using Deep Learning

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-orange)
![Medical AI](https://img.shields.io/badge/Domain-Medical%20AI-green)
![Computer Vision](https://img.shields.io/badge/Computer%20Vision-Classification-red)

</div>

---

## 📌 Overview

This project focuses on **automated skin lesion classification** using deep learning techniques applied to dermoscopic images from the **HAM10000 dataset**.

The system leverages transfer learning, advanced data augmentation, and ensemble learning to accurately classify skin lesions into multiple diagnostic categories. The objective is to assist in the early detection of skin cancer and support medical decision-making through AI-powered image analysis.

---

## 🎯 Project Goals

- Develop an accurate multi-class skin lesion classifier.
- Improve robustness using transfer learning and augmentation.
- Address class imbalance in medical datasets.
- Evaluate performance using industry-standard metrics.
- Explore practical applications of deep learning in healthcare.

---

## 🧠 Model Architecture

### Deep Learning Pipeline

```text
Input Dermoscopic Image
          │
          ▼
   Image Preprocessing
          │
          ▼
    Data Augmentation
          │
          ▼
 Transfer Learning Model
          │
          ▼
  Feature Extraction
          │
          ▼
 Classification Head
          │
          ▼
 Predicted Lesion Class
```

### Key Techniques

✅ Transfer Learning

✅ Data Augmentation

✅ Class Weighting

✅ Learning Rate Scheduling

✅ Early Stopping

✅ Ensemble Prediction

✅ Multi-Class Classification

---

## 🔍 Lesion Categories

The model classifies images into the following categories:

| Class | Description |
|---------|------------|
| MEL | Melanoma |
| NV | Melanocytic Nevus |
| BCC | Basal Cell Carcinoma |
| BKL | Benign Keratosis-like Lesions |
| AKIEC | Actinic Keratoses |
| DF | Dermatofibroma |
| VASC | Vascular Lesions |

---

## 📂 Dataset

### HAM10000 Dataset

**HAM10000 (Human Against Machine with 10000 Training Images)** is one of the most widely used datasets for skin lesion analysis.

Dataset Highlights:

- 10,015 dermoscopic images
- 7 diagnostic classes
- Real clinical cases
- Public benchmark dataset

---

## ⚙️ Training Strategy

### Data Preprocessing

- Image resizing
- Pixel normalization
- Label encoding

### Data Augmentation

- Random rotation
- Horizontal flip
- Vertical flip
- Zoom transformations
- Brightness adjustments

### Optimization

- Transfer learning-based fine tuning
- Adaptive learning rate scheduling
- Early stopping
- Validation monitoring

---

## 📈 Results

### Model Performance

| Metric | Value |
|----------|----------|
| Validation Accuracy | **80.51%** |
| Classification Type | Multi-Class |
| Dataset | HAM10000 |
| Framework | TensorFlow / Keras |

### Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Confusion Matrix

> The model achieved strong performance despite significant class imbalance and visual similarity between lesion categories.

---

## ✨ Key Features

- Multi-Class Skin Lesion Classification
- Medical Image Analysis
- Transfer Learning
- Advanced Data Augmentation
- Ensemble Learning
- Class Imbalance Handling
- ROC-AUC Evaluation
- Confusion Matrix Analysis
- GPU Accelerated Training

---

## 🛠️ Technologies Used

| Category | Tools |
|-----------|--------|
| Programming | Python |
| Deep Learning | TensorFlow, Keras |
| Data Processing | NumPy, Pandas |
| Machine Learning | Scikit-Learn |
| Visualization | Matplotlib, Seaborn |
| Image Processing | OpenCV |
| Development | Jupyter Notebook, Kaggle |

---

## 📁 Repository Structure

```text
Skin-Lesion-Classification/
│
├── skin-lesion-classification.ipynb
├── README.md
├── requirements.txt
│
├── dataset/
├── models/
├── outputs/
│   ├── confusion_matrix.png
│   ├── roc_curve.png
│   ├── training_curves.png
│   └── predictions/
│
└── images/
```

---

## 🚀 Future Improvements

- Vision Transformers (ViT)
- Explainable AI with Grad-CAM
- Clinical Metadata Integration
- Real-Time Web Application
- Mobile Deployment
- Lightweight Edge-AI Models

---

## 🎓 Learning Outcomes

This project provided hands-on experience in:

- Medical Image Classification
- Deep Learning
- Transfer Learning
- Computer Vision
- Model Evaluation
- Healthcare AI Applications

---

## 👨‍💻 Author

**Akash Senigarapu**

B.E. Artificial Intelligence & Machine Learning

Chaitanya Bharathi Institute of Technology (CBIT)

---

## ⭐ Support

If you found this project useful, consider giving it a **Star ⭐** on GitHub.
