🩺 Skin Lesion Classification using ViT-Ensemble and Advanced Deep Learning Techniques
<div align="center">
![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Deep%20Learning-orange)
![Kaggle](https://img.shields.io/badge/Platform-Kaggle-20BEFF)
![Dataset](https://img.shields.io/badge/Dataset-HAM10000-green)
![Validation Accuracy](https://img.shields.io/badge/Validation%20Accuracy-80.66%25-success)
</div>
---
📌 Overview
This project presents a deep learning pipeline for skin lesion classification using the HAM10000 dataset. The goal is to classify dermoscopic images into 7 different lesion categories and support early identification of potentially dangerous skin conditions.
The notebook implements an advanced training workflow that combines:
EfficientNetB0-based pretrained models
Ensemble learning
Strong image augmentation
MixUp regularization
Focal loss
Class weighting
Mixed precision training
Fine-tuning for improved validation performance
---
🎯 Objective
Skin lesion classification is a challenging computer vision task because dermoscopic images often contain:
large variations in color and texture,
blurry lesion boundaries,
class imbalance,
visually similar lesion types.
This project addresses those challenges by using an ensemble of deep learning models and several modern training techniques to improve robustness and generalization.
---
🧠 Model Summary
The notebook builds a 3-model ensemble using EfficientNetB0 as the feature extractor backbone. Each model is trained with:
heavy data augmentation,
dropout regularization,
focal loss,
class weights,
MixUp augmentation.
The final prediction is obtained by averaging the output probabilities from all ensemble members.
---
✨ Key Features
HAM10000 skin lesion dataset
7-class classification
Pretrained EfficientNetB0 backbone
Ensemble of 3 deep learning models
Random flip, rotation, zoom, translation, and contrast augmentation
MixUp augmentation
Class imbalance handling using class weights
Focal loss for hard examples
Mixed precision training for faster GPU utilization
Fine-tuning stage for improved performance
Confusion matrix and classification report visualization
---
📂 Dataset
This project uses the HAM10000 dataset, which contains dermoscopic images of common pigmented skin lesions.
Classes in the dataset
Actinic keratosis
Basal cell carcinoma
Benign keratosis
Dermatofibroma
Melanocytic nevus
Melanoma
Vascular lesion
The dataset is organized from the metadata file and split into training and validation folders before model training.
---
🔄 Training Pipeline
1. Data Organization
The images are copied into class-wise folders based on the metadata CSV file.
2. Data Augmentation
The training pipeline applies:
horizontal and vertical flips
rotation
zoom
translation
contrast adjustment
3. Regularization
To improve generalization, the model uses:
MixUp augmentation
class weights
focal loss
dropout
4. Ensemble Training
Three pretrained EfficientNetB0 models are trained and their outputs are averaged for the final prediction.
5. Fine-Tuning
The ensemble is fine-tuned with a very small learning rate to stabilize training and improve validation performance.
---
📊 Results
The final notebook achieved:
Metric	Value
Validation Accuracy	80.66%
Number of Classes	7
Image Size	224 × 224
The notebook also generates:
confusion matrix
classification report heatmap
sample prediction visualizations
---
🛠 Technologies Used
Python
TensorFlow / Keras
NumPy
Pandas
Matplotlib
Seaborn
Scikit-learn
Kaggle GPU environment
---
📁 Repository Structure
```text
skin-lesion-classification/
├── skin-lesion-classification.ipynb
├── README.md
├── requirements.txt
├── images/
│   ├── confusion_matrix.png
│   ├── classification_report.png
│   └── sample_predictions.png
└── models/
    └── vit_ensemble_finetuned.keras
```
---
🚀 How to Run
1. Clone the repository
```bash
git clone https://github.com/your-username/skin-lesion-classification.git
cd skin-lesion-classification
```
2. Install dependencies
```bash
pip install -r requirements.txt
```
3. Prepare the dataset
Download the HAM10000 dataset and place it in the expected Kaggle or local directory structure.
4. Run the notebook
Open the notebook in Jupyter or Kaggle and execute the cells sequentially.
---
📈 Future Improvements
Possible next steps for this project include:
trying Vision Transformers with stronger attention mechanisms,
using higher-resolution input images,
class-wise calibration analysis,
Grad-CAM visualizations for interpretability,
deployment as a web app using Streamlit or Gradio,
cross-validation instead of a single train/validation split.
---
👨‍💻 Author
Akash Senigarapu  
Artificial Intelligence and Machine Learning  
CBIT, Hyderabad
---
📜 License
This project is intended for educational and research purposes.
---
🙏 Acknowledgements
HAM10000 dataset contributors
TensorFlow and Keras communities
Kaggle for the GPU training environment
