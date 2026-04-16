# 🔢 Handwritten Digit Classification using CNN (PyTorch)

This project builds a Convolutional Neural Network (CNN) using PyTorch to classify handwritten digits (0–9) from grayscale images.

---

# 📌 Project Overview

The goal of this project is to develop a deep learning model capable of recognizing handwritten digits using convolutional neural networks.

Dataset used:
- sklearn Digits Dataset
- 1797 grayscale images
- Image size: 8×8 pixels
- 10 classes (digits 0–9)

---

# 📊 Dataset Information

Total samples: 1797  
Image shape: 8 × 8  
Channels: 1 (Grayscale)  
Number of classes: 10  

Pixel values range:

0 → 16

After normalization:

0 → 1

---

# 🔍 Exploratory Data Analysis (EDA)

Performed:

- Visualized sample digit images
- Checked class distribution
- Analyzed pixel value distribution
- Verified pixel ranges
- Confirmed balanced dataset

---

# ⚙️ Data Preprocessing

Steps performed:

- Normalized pixel values (divided by 16)
- Reshaped images:(1797, 8, 8) → (1797, 1, 8, 8)

  ---

- Split dataset:

Training set:

1437 samples  

Test set:

360 samples  

- Converted data into PyTorch tensors

---

# 🧠 CNN Model Architecture

```python
Conv2d(1 → 8, kernel_size=3)

ReLU()

MaxPool2d(2)

Flatten()

Linear(72 → 32)

ReLU()

Linear(32 → 10)

Model type:

Convolutional Neural Network (CNN)

Loss Function:

CrossEntropyLoss

Optimizer:

Adam (lr=0.001)

Training:

200 epochs
```
# 📉 Training Performance
Loss steadily decreased:

Example:

Epoch 0 → Loss ≈ 2.07
Epoch 100 → Loss ≈ 0.62
Epoch 195 → Loss ≈ 0.25

This indicates successful learning.
---
# 📊 Model Evaluation
Accuracy:
CNN Accuracy: 94%

Confusion Matrix

The model correctly classified most digits with minimal confusion.

Most confusion occurred between visually similar digits:
	•	8 and 1
	•	9 and 8
	•	2 and 3
  
  ---
  # 📈 Classification Report
  Average Scores:
  Precision: 0.94  
  Recall: 0.94  
  F1-score: 0.94
  ---
 # 🖼️ Sample Predictions

Displayed predicted digits alongside true labels to visually validate model performance.

Example:

P:7 T:7 → Correct
P:3 T:2 → Misclassified
---
# 🚀 Technologies Used
	•	Python
	•	PyTorch 
	•	NumPy
	•	Matplotlib
	•	Seaborn
	•	Scikit-learn
  ---

