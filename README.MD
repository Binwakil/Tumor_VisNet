# TumorVisNet: Hybrid CNN + ViT Model for Enhanced Brain Tumor Segmentation

## Overview

**TumorVisNet** is a hybrid architecture that combines Convolutional Neural Networks (CNNs) and Vision Transformers (ViTs) to improve segmentation of brain tumors. This repository implements TumorVisNet, including preprocessing, training, and evaluation workflows. The model processes multimodal MRI data and achieves state-of-the-art performance on the BraTS2021 dataset.

The code and detailed implementation are publicly available at [TumorVisNet GitHub Repository](https://github.com/Binwakil/Tumor_VisNet).

---

## Features
- **Data Preprocessing**: Resizes, normalizes, crops, and augments MRI data for training.
- **Model Architecture**: Combines U-Net-based CNN for local feature extraction with ViTs for global context modeling.
- **Training Workflow**: Uses a custom `DataGenerator` and hybrid loss function for robust training.
- **Visualization**: Generates segmentation overlays, confusion matrices, and prediction comparisons.

---

## Project Structure

```
TumorVisNet/
├── Data/
│   ├── BraTS2021/                # Dataset directory
├── Models/
│   ├── Trained_CNN_Model.h5      # Trained model
├── Visualization/
│   ├── *.png                     # Saved visualizations (e.g., confusion matrices, segmentation overlays)
├── TumorVisNet.ipynb             # Jupyter Notebook with preprocessing, model, and training
├── README.md                     # Project documentation
```

---

## Installation and Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/Binwakil/Tumor_VisNet.git
   cd Tumor_VisNet
   ```

2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Download the BraTS2021 dataset and place it in the `Data/BraTS2021` directory.

---

## How to Run

### Preprocessing
- Use the Jupyter Notebook `TumorVisNet.ipynb` to preprocess MRI scans.
- Resizes input images to 128x128 pixels and normalizes intensity values.

### Model Training
- Train the TumorVisNet model using the provided notebook.
- The trained model is saved as `Models/Trained_CNN_Model.h5`.

### Visualization
- Generate segmentation overlays for specific cases.
- Compare predictions against ground truth masks in the `Visualization` folder.

---

## Results

TumorVisNet achieves state-of-the-art performance on the BraTS2021 dataset:

| Metric            | Value    |
|-------------------|----------|
| **Dice Coefficient** | 0.9031 |
| **Sensitivity**    | 0.993    |
| **Specificity**    | 0.998    |

### Example Visualizations

Predicted segmentation mask for a sample patient:

![Example Prediction](https://github.com/Binwakil/Tumor_VisNet/raw/main/Visualization/prediction_case_00495.png)

---

## Citation

If you use TumorVisNet, please cite:
```
@misc{TumorVisNet2025,
  author = {Almustapha A. Wakili},
  title = {TumorVisNet: Hybrid CNN + ViT for Brain Tumor Segmentation},
  year = {2025},
  publisher = {GitHub},
  howpublished = {\url{https://github.com/Binwakil/Tumor_VisNet}},
}
```

---
