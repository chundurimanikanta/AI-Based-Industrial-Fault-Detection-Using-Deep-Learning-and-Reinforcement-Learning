# AI-Based Industrial Fault Detection Using Deep Learning and Reinforcement Learning

## Project Overview

Industrial quality inspection is an important process in manufacturing industries. Identifying defective products at an early stage helps improve product quality, reduce manufacturing losses, and minimize manual inspection efforts.

This project presents an AI-based Industrial Fault Detection System that uses Deep Learning and Reinforcement Learning techniques to identify whether an industrial product is **Good (Non-Defective) or Defective** based on its surface image.

The project implements and compares seven different AI architectures to study their performance in binary industrial defect classification using the MVTec Defect Detection Dataset.

## Objectives

- Develop an automated industrial defect detection system using AI.
- Classify product images into Good and Defective categories.
- Implement multiple Deep Learning architectures.
- Explore Reinforcement Learning approaches for image classification.
- Compare model performance using standard evaluation metrics.
- Identify the best-performing architecture through experimental comparison.

## Models Implemented

This project implements seven different models:

### 1. ResNet50 – Transfer Learning
Uses a pretrained ResNet50 architecture with ImageNet weights. The model initially freezes the pretrained layers and subsequently fine-tunes the top 30 layers to improve classification performance.

### 2. MobileNetV2 – Transfer Learning
Uses MobileNetV2 as a pretrained feature extractor. Its lightweight architecture makes it suitable for applications where computational efficiency is important.

### 3. Custom CNN
A custom Convolutional Neural Network consisting of multiple convolutional blocks, batch normalization, activation functions, and classification layers to learn defect-related image features.

### 4. CNN-LSTM
Combines Convolutional Neural Networks with Long Short-Term Memory networks. CNN extracts spatial features from images, while LSTM processes the extracted features as a sequence.

### 5. CNN-GRU
Combines CNN feature extraction with a Bidirectional GRU architecture to process spatial feature sequences and perform binary classification.

### 6. Deep Q-Network (DQN)
Explores a Reinforcement Learning-based classification approach using a frozen MobileNetV2 feature extractor. The DQN agent predicts Good or Defective and receives positive or negative rewards based on prediction correctness.

### 7. Actor-Critic (A2C)
Implements an Actor-Critic reinforcement learning approach. The Actor learns the classification policy, while the Critic estimates the value of the current state.

## Dataset

**Dataset:** MVTec Anomaly Detection Dataset

The dataset contains industrial product and texture images with normal and defective samples.

For this project, the original dataset structure is converted into two categories:

- Good – Non-defective product images.
- Defective – Images containing defects.

The project uses binary classification rather than individual defect-type classification.

Dataset information:
https://www.mvtec.com/company/research/datasets/mvtec-ad

## Technologies and Libraries

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## Methodology

1. Dataset preparation and extraction.
2. Conversion of the original dataset into Good and Defective categories.
3. Image resizing to 224 × 224 pixels.
4. Normalization of image pixel values.
5. Data augmentation using random flipping, rotation, zooming, and contrast adjustment.
6. Training of seven different AI architectures.
7. Model evaluation using test data.
8. Performance comparison and visualization.

## Evaluation Metrics

The implemented evaluation process includes:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- Training and Validation Accuracy
- Training and Validation Loss

The final comparison section generates a model performance table, accuracy comparison chart, grouped architecture comparison, and heatmap-style visualization.

## Project Structure

```text
AI-Industrial-Fault-Detection/
│
├── fault_detection.ipynb
├── README.md
├── requirements.txt
├── dataset/
│   └── README.md
└── results/
    └── model_comparison.png
```

## How to Run

This notebook is designed for Google Colab.

1. Download or clone this repository.
2. Open Google Colab.
3. Upload `fault_detection.ipynb`.
4. Upload the MVTec dataset ZIP file to your Google Drive.
5. Update the dataset ZIP path in the notebook if required.
6. Run the setup and dataset preparation cells.
7. Execute each model section in sequence.
8. Run the final comparison section to view the results.

## Expected Output

The system produces:

- Good or Defective classification predictions.
- Model evaluation reports.
- Confusion matrices.
- Training and validation performance graphs.
- Comparison of all seven implemented models.
- Best-performing model identification based on test accuracy.

## Applications

- Industrial manufacturing quality inspection.
- Automated product surface inspection.
- Manufacturing defect screening.
- AI-assisted quality control.
- Research and experimentation in computer vision.

## Future Enhancements

- Extend binary classification to individual defect-type identification.
- Implement real-time camera-based inspection.
- Develop a web-based interface using Streamlit.
- Explore model optimization for edge deployment.
- Add explainable AI techniques for visual defect interpretation.

## Conclusion

This project explores the application of Deep Learning and Reinforcement Learning techniques in industrial fault detection. By implementing seven different architectures and comparing their performance, the project provides a comparative study of different AI approaches for automated binary defect classification.

The proposed system demonstrates how computer vision and AI techniques can support automated quality inspection in manufacturing environments.

## Author

**Chunduri Manikanta**

AI & Robotics | Engineering Student

## Disclaimer

This project is developed for academic and research purposes. The model's predictions should be validated before being used in actual industrial quality-control environments.
