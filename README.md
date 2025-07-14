# Edge AI: Image Classification using TensorFlow Lite

## Overview
This project demonstrates how to train a lightweight image classification model for identifying recyclable items, convert it to TensorFlow Lite format, and simulate edge deployment using Google Colab.

## Tools Used
- TensorFlow 2.x
- TensorFlow Lite
- Google Colab
- (Optional) Raspberry Pi (for real deployment)

## Dataset
We used a custom/small image dataset (e.g., `recyclable` vs `non-recyclable`). The dataset was loaded, split into training and testing sets, and preprocessed for image classification.

## Model Training
A simple image classification model was trained using TensorFlow's high-level APIs.

## Conversion
The trained model was converted into `.tflite` format using:
```python
converter = tf.lite.TFLiteConverter.from_keras_model(model)
tflite_model = converter.convert()
