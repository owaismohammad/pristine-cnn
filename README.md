# 🌊 Water Quality Prediction Model

This project contains a TensorFlow-based Convolutional Neural Network (CNN) model designed to predict water quality through image classification. The model was developed for the *Xylem India Hackathon 2024*.

## 📂 Data Preparation

The dataset includes water sample images categorized into two classes: clean and not_clean. These images were sourced from:

- 🌐 The Internet
- 🛰️ Google Earth
- 🧪 Real-life water samples

The images are stored in separate folders: clean and not_clean.

### 🔗 [Download the Dataset Here](https://drive.google.com/drive/folders/1m6iHzfI5Roy4-1j7Fbvhd5J6ljrlgwzl?usp=drive_link)

## 🧠 Model Architecture

The model uses the following layers:

1. *Conv2D Layer 1:* 16 filters, (3x3) kernel, ReLU activation
2. *MaxPooling2D Layer:* (2x2) pooling
3. *Conv2D Layer 2:* 16 filters, (3x3) kernel, ReLU activation
4. *AveragePooling2D Layer:* (2x2) pooling
5. *Flatten Layer:* Converts the 3D tensor to a 1D vector
6. *Dense Layer 1:* 128 units, ReLU activation
7. *Dense Layer 2:* 64 units, ReLU activation
8. *Dense Layer 3:* 32 units, ReLU activation
9. *Dense Layer 4:* 16 units, ReLU activation
10. *Output Layer:* 1 unit, Sigmoid activation (for binary classification)

![Model Architecture](https://i.imgur.com/gVmbPcZ.jpeg)

## ⚙️ Training Details

- *Optimizer:* SGD with a learning rate of 0.01
- *Loss Function:* Binary Crossentropy
- *Metrics:* Accuracy
- *Class Weights:* Adjusted to handle class imbalance using sklearn.utils.class_weight

## 🎯 Training Process

The model was trained in three stages:

- *First round:* 10 epochs with class weights.
- *Second round:* 2 additional epochs.
- *Third round:* 3 additional epochs.

## 📊 Evaluation

After training, the model's performance can be evaluated using:

- *Loss Curves:* Tracks the decrease in loss during training and validation.
- *Accuracy Curves:* Visualizes the improvement in accuracy over epochs.
- *Confusion Matrix:* Analyzes the model's ability to distinguish between clean and not clean samples.
- *ROC Curves:* Highlights the trade-off between sensitivity and specificity at various thresholds.

## 📈 Visualizations

1. *Loss Curves:*
   
   ![Loss Curve](https://i.imgur.com/CKBSIrB.jpeg)
   
2. *Accuracy Curves:*
   
   ![Accuracy Curve](https://i.imgur.com/TUmNvAD.jpeg)
   
3. *Confusion Matrix:*
   
   ![Confusion Matrix](https://i.imgur.com/C9F7t3O.jpeg)
   
4. *ROC Curves:*
   
   ![ROC Curve](https://i.imgur.com/SwnUoeL.jpeg)

## 🔢 Block Diagram

![Block Diagram1](https://i.imgur.com/kJUIYCK.jpeg)
![Block Diagram2](https://i.imgur.com/EXPIAay.jpeg)

## 🏆 Conclusion

This model successfully classifies water samples into clean and not_clean categories, contributing to automated water quality assessment efforts.
