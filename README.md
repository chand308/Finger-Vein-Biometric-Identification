
# Finger Vein Biometric Identification Using CNN

This project focuses on building a robust biometric identification system using infrared images of finger veins. Unlike traditional fingerprint-based systems, this approach provides enhanced hygiene and security by utilizing unique vein patterns.

---

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Model Architecture](#model-architecture)
- [Training and Validation](#training-and-validation)
- [Results](#results)
- [Limitations](#limitations)
- [How to Use](#how-to-use)
- [References](#references)

---

## Introduction

Biometric systems are essential for secure authentication. Traditional methods, such as fingerprint recognition, face hygiene concerns and tampering risks. This project uses infrared finger vein images, which are unique and captured without physical contact.

---

## Dataset

The dataset comprises infrared finger vein images collected from 123 volunteers. Each volunteer provided images for four fingers (left index, left middle, right index, and right middle) across multiple sessions.

### Sample Images

#### 1. Raw Infrared Finger Vein Image
![Infrared Finger Vein Image](images/page_3_image_1.png)

#### 2. Preprocessed Vein Pattern
This pattern is extracted from the raw data, highlighting the vein structure.
![Preprocessed Vein Pattern](images/page_3_image_2.png)

---

## Data Preprocessing

1. **Resizing**: All images were resized to 100x100 pixels.
2. **Normalization**: Pixel values were normalized to a range of [0, 1].
3. **Data Augmentation**: Techniques such as flipping, rotation, and zooming increased dataset diversity.

---

## Model Architecture

The CNN model was designed with:
1. **Convolutional Layers**: To extract features.
2. **MaxPooling Layers**: To reduce spatial dimensions.
3. **Fully Connected Layers**: To classify individuals based on vein patterns.

---

## Training and Validation

The model was trained with:
- Optimizer: Adam
- Loss Function: Categorical Crossentropy
- Metrics: Accuracy

### Training and Validation Accuracy
![Training and Validation Accuracy](images/page_4_image_1.png)

### Model Loss Per Epoch
Include your plotted image for model loss here:
![Model Loss Per Epoch](images/your_loss_plot_image.png)

---

## Results

1. **Test Accuracy**: 80.44%
2. **Classification for Specific IDs**: Achieved high accuracy for IDs 22 and 43.
3. **Confusion Matrix**:
![Confusion Matrix](images/page_4_image_2.png)

---

## Limitations

1. **Runtime**: Training takes ~6 hours for 100 epochs.
2. **Scalability**: Model complexity grows with the number of classes or higher resolution images.

---

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/chand308/Finger-Vein-Biometric-Identification.git
   cd Finger-Vein-Biometric-Identification
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Organize the dataset:
   ```
   data/
   ├── class1/
   │   ├── image1.jpg
   │   ├── image2.jpg
   ├── class2/
   │   ├── image1.jpg
   │   ├── image2.jpg
   ```

4. Run the training script:
   ```bash
   python finger_vein_project.py
   ```

---

## References

1. Mohd Shahrimie Mohd Asaari et al., *Band Limited Phase Only Correlation and Width Centroid Contour Distance for finger-based biometrics*.
2. Ismail Boucherit et al., *Finger vein identification using deeply-fused Convolutional Neural Network*.
