# Multi-Task U-Net for Breast Ultrasound Image Analysis

This project implements a U-Net model in PyTorch for both semantic segmentation and classification of breast tumors in ultrasound images. The model is trained on the Breast Ultrasound Images (BUSI) dataset to identify tumor regions and classify them into one of three categories: Normal, Benign, or Malignant.
The project includes the complete training pipeline in a Jupyter Notebook (UNET.ipynb) and a ready-to-use interactive web demo powered by Gradio (app.py).

<img width="874" height="454" alt="Screenshot 2025-12-03 221230" src="https://github.com/user-attachments/assets/f5065e73-5c83-4e5a-bdaf-3a9ece30fbfc" />

Key Features:

1) Multi-Task Learning: The model simultaneously performs segmentation (identifying tumor pixels) and classification (diagnosing the image).
2) Stable U-Net Architecture: The U-Net implementation includes Batch Normalization in each convolutional block to ensure stable and efficient training, preventing issues like vanishing/exploding gradients.
3) Robust Training Strategy: A pre-training phase is used to initialize the segmentation head before introducing the classification task. This stabilizes the multi-task learning process.
4) Advanced Data Augmentation: The training pipeline utilizes the Albumentations library for a rich set of augmentations (ElasticTransform, flips, rotations, brightness/contrast adjustments), making the model more robust and reducing overfitting.
5) Combined Loss Function: A sophisticated loss function combines Dice Loss and weighted Binary Cross-Entropy (BCE) for the segmentation task, alongside a standard Cross-Entropy Loss for classification.
6) Interactive Demo: The final trained model is deployed in a user-friendly web interface using Gradio, allowing for easy testing with new images.
7) Comprehensive Evaluation: The model's performance is measured using standard metrics: Dice Score & IoU for segmentation, and Accuracy, F1-score, Precision, Recall & MCC for classification.

Model Performance
--- Segmentation Performance ---
1) Average Dice Score: 0.7183
2) Average IoU (Jaccard) Score: 0.5757

--- Classification Performance ---
1) Accuracy: 0.7949
2) Weighted F1-score: 0.7944
3) Weighted Precision: 0.8063
4) Weighted Recall: 0.7949
5) Matthews Correlation Coefficient (MCC): 0.667

<img width="640" height="547" alt="download (7)" src="https://github.com/user-attachments/assets/8809e0b6-1ae2-4f4d-a51d-3f8ff4e72331" />


Use the Google Drive link for the Pth file:

Link: https://drive.google.com/drive/folders/1WL8g-ovjVJMrdgIYq8Yn4QDnvqTnOWh7?usp=sharing
