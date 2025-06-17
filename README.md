# automated-medical-image-diagnosis-ai
An AI-powered medical diagnostic system that utilizes deep learning models (VGG16 and U-Net) to detect and segment diseases in X-ray and MRI images. The project also integrates explainable AI and bias mitigation strategies to ensure fairness and transparency. 
Table of Contents

Overview

Objectives

Dataset

Methodology

Classification Model

Segmentation Model

Explainable AI

Bias Mitigation

Project Structure

Installation

Usage

Evaluation Metrics

Ethical Considerations

License

Author

Overview

This project aims to develop a robust AI system that automates medical diagnosis by analyzing medical imaging formats such as X-rays and MRIs. It applies transfer learning techniques for binary classification of brain tumors and advanced segmentation networks (U-Net) for tumor localization. The system also incorporates explainable AI (Grad-CAM, attention mechanisms) and fairness analysis to assess and reduce demographic bias.

Objectives

Build an AI diagnostic system compatible with multiple formats (X-ray and MRI).

Integrate explainable AI tools to enhance interpretability of model predictions.

Implement bias mitigation strategies to ensure fair treatment across patient groups.

Evaluate model performance against current state-of-the-art techniques.

Assess clinical value based on accuracy, usability, and interpretability.

Dataset

Classification Dataset: Brain MRI Images for Brain Tumor Detection

Segmentation Dataset: BraTS 2020 Dataset

All datasets are publicly available and used under academic research licenses. See data/README.md for download instructions.

Methodology

Classification Model

Model: Transfer learning using pre-trained VGG16

Task: Binary classification (tumor present/absent)

Framework: TensorFlow/Keras

Techniques: Data augmentation, freezing pre-trained layers, softmax output

Segmentation Model

Model: U-Net architecture

Task: Pixel-wise brain tumor segmentation

Implementation: Custom Keras model with encoder-decoder and skip connections

Loss Functions: Dice Loss, IoU Loss

Explainable AI

Techniques: Grad-CAM, Layer-wise Relevance Propagation, Attention U-Net

Tools: Saliency Maps, Heatmap Visualization

Purpose: Improve transparency of model predictions for clinical trust

Bias Mitigation

Sources of Bias: Dataset imbalance, scanner variability, demographic underrepresentation

Strategies:

Data balancing via augmentation

Fairness-aware training objectives

Separate validation on underrepresented groups

Project Structure

automated-medical-image-diagnosis-ai/
│
├── data/                     # Dataset references and usage notes
├── notebooks/               # Jupyter notebooks for EDA, training
├── src/                     # Source code scripts
│   ├── preprocessing.py
│   ├── model_vgg16.py
│   ├── model_unet.py
│   ├── evaluation.py
│   └── utils.py
├── outputs/                 # Results: models, plots
├── reports/                 # Dissertation summary or presentation slides
├── requirements.txt         # Python dependencies
├── LICENSE                  # MIT License
├── .gitignore               # Files/folders to ignore
└── README.md                # Project overview

Installation

git clone https://github.com/yourusername/automated-medical-image-diagnosis-ai.git
cd automated-medical-image-diagnosis-ai
pip install -r requirements.txt

Usage

Run the following scripts:

Classification: python src/model_vgg16.py

Segmentation: python src/model_unet.py

Visualize results and predictions in notebooks under notebooks/

Evaluation Metrics

Classification: Accuracy, Precision, Recall, F1-Score

Segmentation: Dice Coefficient, Intersection over Union (IoU), Hausdorff Distance

Fairness: Disparate Impact, Equal Opportunity

Ethical Considerations

Data Privacy: Only anonymized, publicly available datasets used

Transparency: XAI tools integrated for interpretability

Non-Clinical Use: Research purposes only, not for diagnostic use

LicenseAuthor

Sagayanathan Joseph NainarMSc Data Analytics – Class of 2025University for the Creative Arts (UCA)

This project is licensed under the MIT License - see the LICENSE file for details.

