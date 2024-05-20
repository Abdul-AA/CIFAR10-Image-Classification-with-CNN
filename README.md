# Convolutional Neural Network for CIFAR10 Image Classification
## Introduction

This project explores the implementation and evaluation of a Convolutional Neural Network (CNN) for image classification on the CIFAR-10 dataset. The CIFAR-10 dataset consists of 60,000 32x32 color images in 10 classes, with 50,000 training images and 10,000 test images. The aim is to design a CNN architecture that achieves comparable performance with the known benchmark.
## CNN Architecture and Training
The implemented CNN architecture includes three convolutional layers with batch normalization and max pooling, followed by two fully connected layers with dropout for regularization. The model was trained using the PyTorch Lightning framework, incorporating data augmentation techniques such as random horizontal flipping and random cropping to enhance generalization. Early stopping and model checkpointing were utilized to monitor and optimize the training process, ensuring the best-performing model is saved and training is halted when the validation accuracy stops improving.

## Results
The CNN achieved the following metrics on the CIFAR-10 test set:
- **Test Accuracy**: 82.20%, indicating the proportion of correctly classified images out of the total.
- **Test Precision**: 82.29%, measuring the average accuracy of the positive predictions for the multiclass classification task.
- **Test Recall** 82.23, measuring the average percentage of retreived instances across all 10 classes
- **Test F1 Score**: 82.00%, reflecting the balance between precision (correct positive predictions) and recall (retrieved relevant instances) across all 10 classes.


These metrics demonstrate the robustness of the CNN model. They essentially indicate that the model performs well in predicting each class in the dataset. However, the performance, while solid, could be further improved. The state-of-the-art Vision Transformer (ViT-H/14) model achieves a top-1 accuracy of 99.5% on CIFAR-10. Achieving similar levels of performance would require a more complex neural network, which would be computationally expensive.

In this project, striking a balance between model complexity, resource requirements, and performance was crucial.
