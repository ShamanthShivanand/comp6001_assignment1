# Investigating the Impact of Classical Image Deblurring on Cross-Domain Object Detection Performance

## Overview

This project investigates whether classical image restoration methods can improve downstream object detection performance on blurred images.

Motion blur reduces important visual information such as edges, texture, and object boundaries. This project compares blurred, restored, and sharp image domains using classical image restoration methods and YOLOv8 object detection.

The main focus is to determine whether visually improved images also improve machine learning performance.

---

## Research Questions

1. Can classical image restoration methods improve object detection performance on blurred images?

2. Which restoration method provides the best balance between image quality, runtime, and downstream detection performance?

3. How do models trained on sharp, blurred, and restored images perform across different image domains?

---

## Methods Used

### Image Restoration
- Wiener Filtering
- Richardson–Lucy Deconvolution

### Image Quality Metrics
- PSNR
- SSIM
- Laplacian Variance
- Runtime Comparison

### Object Detection
- YOLOv8n
- Precision
- Recall
- mAP@50
- mAP@50-95

---

## Dataset

This project uses:
- GoPro Deblur Dataset
- COCO Validation Images
- Custom train/validation/test subsets for YOLOv8 training

The full dataset is not included in this repository because of file size limitations.

You can download the datasets from:

- https://www.kaggle.com/datasets/rahulbhalley/gopro-deblur
- https://www.kaggle.com/datasets/jishnuparayilshibu/a-curated-list-of-image-deblurring-datasets

After downloading, place the dataset inside:

```text
data/
├── sharp/
├── blurred/
├── restored/
├── train/
├── val/
└── test/
