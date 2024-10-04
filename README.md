# Grad-CAM

Grad-CAM (Gradient-weighted Class Activation Mapping) visualizes important regions in images that influence deep learning model predictions.

## Features

- Highlights regions of interest for CNNs.
- Supports popular architectures (e.g., VGG, ResNet).
- Easy integration with PyTorch.

## Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/sushilashrestha/Grad_CAM.git
cd Grad_CAM
pip install -r requirements.txt
```

## Usage

1. **Import and load model:**

   ```python
   import torch
   from grad_cam import GradCAM

   model = ...  # Load your model
   model.eval()
   ```

2. **Prepare input:**

   ```python
   input_image = ...  # Load and preprocess your image
   ```

3. **Generate heatmap:**

   ```python
   grad_cam = GradCAM(model=model, target_layer='last_conv_layer')
   heatmap = grad_cam(input_image, target_class=class_index)
   ```

4. **Overlay heatmap:**

   ```python
   # Resize and overlay heatmap on the original image
   ```

