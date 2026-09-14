# Hand-written-digit-recognition

## DADS6003 Machine Learning — Homework 2

### Author: Student ID: 6820422031 , Mr.Ratthaphong Somtid (Dab)

This project focuses on improving a handwritten digit classification model for digits **0–9**.

The project begins with the Logistic Regression implementation provided by the professor and investigates how to improve its ability to recognize **genuinely unseen handwriting**.

---

## Project Objective

The objective is not simply to obtain high accuracy on the original train/test split.

The professor's baseline model already achieves very high accuracy on the small supplied dataset. However, when new handwritten digit images are introduced, the model may make incorrect predictions.

Therefore, the main goal of this project is:

> **Improve the generalization performance of the handwritten digit classifier on new, unseen handwriting.**

---

## Baseline Model

The original workflow provided by the professor is:

1. Read handwritten digit images in grayscale.
2. Resize every image to `28 × 28` pixels.
3. Flatten each image into `784` pixel features.
4. Use the folder name (`0`–`9`) as the class label.
5. Split the dataset into training and testing sets.
6. Train a Logistic Regression classifier.
7. Evaluate the model using classification accuracy.
8. Use the trained model to classify additional handwritten digit images.

The baseline image representation is therefore:

```text
Image
  ↓
Grayscale
  ↓
Resize to 28 × 28
  ↓
Flatten
  ↓
784 pixel features
  ↓
Logistic Regression
  ↓
Predicted digit: 0–9