🩺 Skin Lesion Classification using Deep Learning
<div align="center">
![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-orange)
![Computer Vision](https://img.shields.io/badge/Domain-Medical%20AI-green)
![Status](https://img.shields.io/badge/Status-Completed-success)
</div>
---
📌 Overview
Skin cancer is one of the most common and clinically important forms of cancer, and early detection can significantly improve treatment outcomes.
This project presents a deep learning-based skin lesion classification system built on the HAM10000 dermoscopic image dataset. The model learns visual patterns from skin lesion images and classifies them into multiple diagnostic categories using transfer learning and an ensemble-based training strategy.
The workflow includes:
image preprocessing
data augmentation
class imbalance handling
ensemble model training
fine-tuning
performance evaluation
confusion matrix analysis
---
🎯 Project Goal
The goal of this project is to build a robust medical image classification pipeline that can assist in automated skin lesion analysis and support early diagnosis.
---
🧠 Model Architecture
This notebook implements an ensemble of three EfficientNetB0-based classifiers.  
Each model is trained on dermoscopic images and their predictions are combined to produce the final output.
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
EfficientNetB0 Backbone
        │
        ▼
Feature Extraction
        │
        ▼
Ensemble of 3 Models
        │
        ▼
Final Softmax Prediction
```
Training Techniques Used
Transfer learning with EfficientNetB0
Mixed precision training
MixUp augmentation
Focal loss
Class weights for imbalance handling
Early stopping
Model checkpointing
Fine-tuning with a lower learning rate
---
🏷️ Skin Lesion Categories
The model classifies images into the following 7 HAM10000 classes:
Label	Class
mel	Melanoma
nv	Melanocytic nevus
bcc	Basal cell carcinoma
bkl	Benign keratosis
akiec	Actinic keratosis
df	Dermatofibroma
vasc	Vascular lesion
---
📂 Dataset
Dataset used: HAM10000  
Source: Dermoscopic skin lesion images with metadata labels
Dataset Split
The notebook organizes the dataset into an 80/20 train-validation split.
Split	Images
Train	8050
Validation	1965
Class Imbalance
The dataset is heavily imbalanced, so the notebook uses:
class weights
focal loss
MixUp augmentation
This helps the model learn minority classes more effectively.
---
✨ Key Features
Multi-class skin lesion classification
Transfer learning with EfficientNetB0
Ensemble learning with 3 models
Advanced data augmentation
Mixed precision training
Class imbalance handling
Fine-tuning stage
Confusion matrix visualization
Classification report analysis
---
🔄 Training Pipeline
1) Data Preparation
Read the HAM10000 metadata CSV
Map image IDs to lesion labels
Organize images into train and validation folders
2) Preprocessing
Resize images to 224 × 224
Normalize input data
Apply augmentation during training
3) Training
Train the ensemble model
Use class weights and focal loss
Monitor validation performance
Save the best model checkpoints
4) Fine-Tuning
Unfreeze the backbone models
Continue training with a very small learning rate
Restore the best weights using early stopping
5) Evaluation
Compute validation accuracy
Generate classification report
Plot confusion matrix
Visualize sample predictions
---
📊 Model Summary
Item	Value
Input Size	224 × 224
Number of Classes	7
Ensemble Size	3 models
Total Parameters	12,175,614
Trainable Parameters	12,049,545
Non-trainable Parameters	126,069
---
📈 Training Results
Final Validation Performance
Metric	Value
Validation Accuracy after Fine-Tuning	80.66%
Final Validation Accuracy	80.31%
Validation Loss (final)	0.0761
Training Progress
The model started around 50.75% training accuracy in the first epoch.
Validation accuracy improved steadily across epochs.
After fine-tuning, the model reached 80%+ validation accuracy.
The final saved model achieved 80.31% validation accuracy on the validation set.
---
🖼️ Evaluation Outputs
The notebook also generates:
Classification Report Heatmap
Confusion Matrix
Sample Prediction Grid
Training vs Validation Accuracy Plot
Training vs Validation Loss Plot
These visualizations help understand the model's strengths and weaknesses across lesion classes.
---
🛠 Technologies Used
Category	Tools
Programming	Python
Deep Learning	TensorFlow, Keras
Data Handling	NumPy, Pandas
Visualization	Matplotlib, Seaborn
Machine Learning	Scikit-Learn
Environment	Kaggle Notebook
---
📁 Repository Structure
```text
Skin-Lesion-Classification/
├── skin-lesion-classification.ipynb
├── README.md
├── requirements.txt
├── dataset/
├── models/
├── outputs/
│   ├── confusion_matrix.png
│   ├── classification_report.png
│   ├── training_curves.png
│   └── sample_predictions.png
└── images/
```
---
🚀 Future Improvements
Add Grad-CAM explainability
Try Vision Transformer based backbones
Experiment with deeper ensemble architectures
Add calibration metrics
Build a Streamlit web app for inference
Deploy the model as a lightweight medical AI demo
---
👨‍💻 Author
Akash Senigarapu  
Artificial Intelligence & Machine Learning  
Chaitanya Bharathi Institute of Technology (CBIT)
---
⭐ Support
If you found this project useful, consider starring the repository on GitHub.
