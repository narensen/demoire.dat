# DeNoisy.dat
Provides edge over Traditional CNN and GANs in accuracy and efficiency

# Image Restoration with Deformable Attention Transformer

This project implements an image restoration model using a Deformable Attention Transformer (DAT) architecture. The model is designed to remove moiré patterns from images using the UHDM dataset.

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
