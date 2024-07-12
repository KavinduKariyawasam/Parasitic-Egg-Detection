# Parasitic Egg Detection and Classification in Microscopic Images

**Authors:** Kariyawasam KKD , Nimnaka KWH  
**Department of Electronic and Telecommunications, University of Moratuwa**  
**Project Repository:** [GitHub](https://github.com/KavinduKariyawasam/Parasitic-Egg-Detection)

## Overview

Intestinal parasitic infections are a major global health challenge, affecting 1.5 billion people worldwide, especially children. These infections cause severe health issues such as diarrhea, malnutrition, and anemia. Traditional diagnostic methods are time-consuming and impractical for on-site use.

This project aims to automate the detection and identification of parasitic eggs in microscopic images using machine learning and computer vision techniques. By leveraging the "Chula-ParasiteEgg-11" dataset, which consists of 11,000 images covering 11 types of parasitic eggs, we aim to enhance the accuracy and efficiency of diagnoses, particularly in resource-constrained regions.

## Method

### Data Preprocessing
- **Gaussian Blur:** Applied to reduce noise and smooth out images.
- **Dataset Structuring:** Organized into training, validation, and test sets.
- **Label Generation:** Labels created in YOLO format, specifying object class, and bounding box coordinates.
- **Configuration:** YAML configuration file created for model training.

### Model
We utilized YOLOv8 (You Only Look Once version 8) for this project, a state-of-the-art object detection and image segmentation model known for its high speed and accuracy.

- **Architecture:** Comprises 24 convolutional layers, four max-pooling layers, and two fully connected layers. Utilizes techniques like batch normalization and dropout for regularization.
- **Training:** The model was trained using the Chula-ParasiteEgg-11 dataset, employing a pre-trained YOLOv8 model initialized with weights optimized on a diverse range of object recognition tasks.

![YOLOv8 Architecture](/images/architecture_yolo_v8.jpg)

### Model Performance
- **Speed:** YOLOv8 processes images at 45 Frames Per Second (FPS).
- **Accuracy:** Demonstrates high precision and minimal background errors.
- **Generalization:** Capable of performing well across various domains due to improved generalization in newer YOLO versions.

### Evaluation
- **Validation:** The model's predictions closely match ground truth labels.
- **Loss Curves:** Monitored box loss, classification loss, and objectness loss during training.
- **Metrics:** Precision, recall, and F1 confidence curves used to evaluate performance.
- **Confusion Matrix:** Most classifications were correct, indicating good model performance.

## Results

The YOLOv8 model showed excellent performance in detecting and classifying parasitic eggs in microscopic images. Validation results indicate high accuracy and reliable predictions, making it a suitable tool for real-time diagnostic applications in healthcare, especially in regions with limited resources.
