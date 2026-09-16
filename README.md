# Intel_Image_Classification_CNN_vs_VGG16_vs_MobileNetV2
Train and compare three architectures — a small baseline CNN, VGG16 (transfer learning) and MobileNetV2 (transfer learning) — on the same multi-class image classification task, then evaluate them not just on accuracy but on parameter count, model size, and inference speed. 
# Intel Image Classification — CNN vs VGG16 vs MobileNetV2

A comparative computer vision experiment evaluating a custom CNN,
VGG16 transfer learning, and MobileNetV2 transfer learning on the
Intel Image Classification dataset.

## Objective

The project investigates the trade-off between classification
performance and computational efficiency across three CNN
architectures.

The models are compared using:

- Test accuracy
- Parameter count
- Model size
- Inference time
- Confusion matrices
- Classification reports
- Error analysis

## Dataset

Intel Image Classification Dataset

Classes:

- Buildings
- Forest
- Glacier
- Mountain
- Sea
- Street

## Models

### 1. Baseline CNN

A custom CNN trained from scratch.

### 2. VGG16

ImageNet-pretrained VGG16 with the convolutional backbone frozen and a custom classification head.

### 3. MobileNetV2

ImageNet-pretrained MobileNetV2 with a frozen backbone, selected for its suitability for resource-constrained and edge-oriented applications.

## Methodology

- Image size: 150 × 150
- Batch size: 32
- Validation split: 15%
- Epochs: 10
- Data augmentation: horizontal flip, rotation, zoom
- Optimizer: Adam
- Loss: Sparse Categorical Crossentropy

## Results

<img width="670" height="213" alt="image" src="https://github.com/user-attachments/assets/ef71497b-fd04-4df6-8aa4-05929b3a9826" />

## Error Analysis

The project analyzes misclassified test images and examines
confusions between visually similar scene categories.

## Limitations

- VGG16 and MobileNetV2 backbones were frozen.
- Each model was trained for only 10 epochs.
- Inference measurements were obtained in Google Colab and may
  differ on actual edge hardware.

## Future Work

- Fine-tune pretrained layers
- Quantize MobileNetV2 using TensorFlow Lite
- Evaluate on an edge device
- Investigate additional augmentation strategies
- Compare accuracy-efficiency trade-offs after optimization

## Notebook

[Open in Google Colab](https://colab.research.google.com/drive/15YoH92aRf1wsLkI44BsHFInSYXOC02-7?usp=sharing)
