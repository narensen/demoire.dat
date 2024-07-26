# DeNoisy.dat
Provides edge over Traditional CNN and GANs in accuracy and efficiency

# Image Restoration with Deformable Attention Transformer

This project implements an image restoration model using a Deformable Attention Transformer (DAT) architecture. The model is designed to remove moiré patterns from images using the UHDM dataset.

## Purpose of DAT

The Deformable Attention Transformer (DAT) is used in this project for image restoration, specifically for removing moiré patterns from images. DAT combines the strengths of transformer architectures with deformable convolutions, making it particularly effective for image processing tasks. Here's why DAT is useful for this purpose:

1. Flexible Feature Extraction: The deformable convolutions allow the model to adaptively adjust its receptive field, capturing complex patterns and artifacts like moiré more effectively.

2. Long-range Dependencies: The transformer architecture enables the model to capture long-range dependencies in the image, which is crucial for understanding and removing global patterns like moiré.

3. Attention Mechanism: The self-attention mechanism helps the model focus on the most relevant parts of the image for restoration, improving its ability to distinguish between moiré patterns and actual image content.

4. Adaptability: DAT can adapt to various types and scales of moiré patterns, making it more versatile than fixed-architecture models.

5. High-quality Restoration: By combining these advanced techniques, DAT aims to produce high-quality restored images with minimal artifacts and preserved details.

   
## Features

- Deformable Attention Transformer (DAT) architecture
- Squeeze-and-Excitation blocks for feature recalibration
- Residual connections for improved gradient flow
- Multi-head self-attention mechanism
- Custom image restoration head

## Requirements

- Python 3.x
- PyTorch
- torchvision
- PIL
- scipy
- numpy

## Installation

1. Clone this repository:
`git clone https://github.com/yourusername/image-restoration-dat.git`
`cd image-restoration-dat`

2. Install the required packages:
`pip install torch torchvision Pillow scipy numpy`

## Usage

1. Prepare your dataset:
- Place your training images in the `UHDM/train` directory
- Ensure that for each moiré image (`*_moire.jpg`), there's a corresponding ground truth image (`*_gt.jpg`)

2. Run the training script:
`python train.py`

3. The trained model will be saved as `model.pth`

## Model Architecture

The DAT model consists of:
- Deformable Transformer Encoder
- Deformable Transformer Decoder
- Image Restoration Head

The model uses squeeze-and-excitation blocks, residual connections, and multi-head self-attention mechanisms to effectively remove moiré patterns from images.

## Evaluation Metrics

The model's performance is evaluated using the following metrics:
- Peak Signal-to-Noise Ratio (PSNR)
- Structural Similarity Index (SSIM)
- Visual Information Fidelity (VIF)
- Custom Moiré Metric

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for d
