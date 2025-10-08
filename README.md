# Malaria Cell Classification Using Deep Learning
---
This project implements a convolutional neural network (CNN) using transfer learning with VGG19 and EfficientNetB3 architectures to classify cell images as either 'Parasitized' or 'Uninfected' with malaria.

## Objectives

- Develop an accurate and efficient deep learning model for malaria cell classification.  
- Utilize transfer learning from pre-trained CNN architectures (**VGG19**, **EfficientNetB3**).  
- Evaluate model performance using accuracy and loss metrics.

---

**Dataset Source:**  (https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria)

### Dataset Classes

| Class Label   | Description |
|----------------|--------------|
| **Uninfected** | Healthy cell image without malaria parasite |
| **Parasitized** | Cell image containing malaria parasite |

###  Data Preprocessing
- Resize all images to **224 × 224 pixels**.  
- Normalize pixel values (0–1 scaling).  
- Split dataset into **training**, **validation**, and **test** sets.  
---

## Model Overview

Two CNN architectures are fine-tuned using transfer learning:

1. **VGG19**  
2. **EfficientNetB3**
 

## ⚙️ Model Training Configuration

| Parameter | Value |
|------------|--------|
| Optimizer | Adam |
| Loss Function | Categorical Crossentropy |
| Epochs | 30 |
| Batch Size | 32 |
| Evaluation Metric | Accuracy |

**Training Strategy:**
- The dataset is split into training, validation, and test sets.  
- - Model trained for **30 epochs** with **early stopping** and **learning rate scheduler**.  
- Performance is monitored using accuracy and loss curves.

---

## Model Evaluation

Model evaluation is performed using unseen test data to assess generalization ability.
Visualization tools such as **Matplotlib** are used to plot accuracy and loss trends over training epochs.

## Dependencies
- pandas
- numpy
- matplotlib
- tensorflow
