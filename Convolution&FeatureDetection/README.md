# Image Processing Tools

This repository contains a collection of Python functions for basic image processing operations, with a focus on convolution and cross-correlation techniques.

## Features

- Naive 2D convolution implementation
- Optimized 2D convolution
- Zero-padding for images
- Zero-mean cross-correlation

## Requirements

- Python 3.x
- NumPy

## Usage

### Convolution

```python
from filters import conv_nested, conv_fast

# Load your image as a numpy array
image = ...

# Define your kernel
kernel = np.array([
    [1, 0, -1],
    [2, 0, -2],
    [1, 0, -1]
])

# Perform convolution
result_nested = conv_nested(image, kernel)
result_fast = conv_fast(image, kernel)
```

### Zero-Padding

```python
from filters import zero_pad

padded_image = zero_pad(image, pad_height, pad_width)
```

### Zero-Mean Cross-Correlation

```python
from filters import zero_mean_cross_correlation

result = zero_mean_cross_correlation(image1, image2)
```

## Function Descriptions

- `conv_nested(image, kernel)`: Performs 2D convolution using nested loops.
- `zero_pad(image, pad_height, pad_width)`: Adds zero-padding to an image.
- `conv_fast(image, kernel)`: Performs 2D convolution using optimized NumPy operations.
- `zero_mean_cross_correlation(f, g)`: Performs zero-mean cross-correlation between two images.
