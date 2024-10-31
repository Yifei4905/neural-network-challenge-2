# neural-network-challenge-2
## Project Overview

This project implements a neural network model with TensorFlow’s Keras to predict employee **Attrition** and **Department** using classification techniques. The solution includes data preprocessing, a branched model architecture, and an analysis of evaluation metrics for imbalanced data.

## Table of Contents

- [Dataset](#dataset)
- [Preprocessing](#preprocessing)
- [Model Architecture](#model-architecture)
- [Training and Evaluation](#training-and-evaluation)
- [Evaluation Metrics](#evaluation-metrics)
- [Improvements](#improvements)
- [References](#references)

## Dataset

The dataset includes employee records with `Attrition` and `Department` as target variables. The selected input features include 12 columns, with a key feature, `Overtime`, converted to numeric for compatibility with the model.

## Preprocessing

1. **Data Preparation**: Loaded data from CSV and extracted `Attrition` and `Department` as targets.
2. **Feature Selection**: Chose 12 columns for the input data (`X`) and converted categorical values where needed.
3. **Scaling and Encoding**:
   - Applied `StandardScaler` for data standardization.
   - Encoded targets with `OneHotEncoder` for multi-class compatibility.

## Model Architecture

This branched neural network model was designed in **TensorFlow Keras**:
- **Shared Layers**: Two hidden layers shared between both outputs.
- **Separate Output Layers**:
  - `Attrition`: Binary classification with **sigmoid** activation.
  - `Department`: Multi-class classification with **softmax** activation.

## Training and Evaluation

- **Training**: The model was trained on 100 epochs using the training data.
- **Evaluation Results**:
  - **Attrition Accuracy**: 81.2%
  - **Department Accuracy**: 51.9%

## Evaluation Metrics

Due to data imbalance, accuracy alone may not capture model effectiveness. Additional metrics like **Precision, Recall, and F1-Score** can give better insights into performance, particularly for underrepresented classes. A **confusion matrix** can further clarify prediction strengths across classes.

## Improvements

1. **Additional Features**: Including fields like education level or certifications may improve Department predictions.
2. **Class Balancing**: Addressing imbalances, especially for smaller classes like Human Resources, could enhance the model’s generalization.
3. **Hyperparameter Tuning**: Optimizing settings like learning rate and layer sizes can improve accuracy.
4. **Advanced Techniques**: Ensemble methods or alternative architectures might boost performance, especially for multi-class targets.

## References

This project builds on foundational code and exercises provided by the Columbia AI Bootcamp, with extensions and refinements for this specific dataset and prediction task.