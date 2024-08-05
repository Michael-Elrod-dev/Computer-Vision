# Facial Detection and Analysis Project

This project implements facial detection and analysis using computer vision techniques. It includes functionality for HOG (Histogram of Oriented Gradients) feature extraction, sliding window detection, image pyramids, and visualization of results.

## Features

- HOG feature extraction from facial images
- Sliding window detection for face localization
- Image pyramid implementation for multi-scale detection
- Visualization tools for displaying results

## Files

- `util.py`: Utility functions for reading facial labels and loading face images
- `visualization.py`: Functions for plotting and visualizing results
- `detection.py`: Core detection algorithms including HOG feature extraction, sliding window, and image pyramid
- `Face.py`: Main script demonstrating the usage of the detection and visualization functions

## Dependencies

- NumPy
- scikit-image
- Matplotlib
- SciPy

## Usage

1. Ensure all dependencies are installed.
2. Place facial images in the `./face` directory.
3. Run `Face.py` to execute the facial detection and analysis pipeline.

## Example Usage

```python
from detection import *
from visualization import *
from util import *

# Load face images
image_paths = fnmatch.filter(os.listdir('./face'), '*.jpg')
face_shape, avg_face = load_faces(image_paths, len(image_paths))

# Extract HOG features
face_feature, face_hog = hog_feature(avg_face)

# Perform sliding window detection
image = io.imread('image_0001.jpg', as_gray=True)
score, r, c, response_map = sliding_window(image, face_feature, stepSize=30, windowSize=face_shape)

# Perform pyramid detection
max_score, maxr, maxc, max_scale, max_response_map = pyramid_score(image, face_feature, face_shape, stepSize=30, scale=0.8)

# Visualize results
plot_part3_2(image, max_scale, face_shape[1], face_shape[0], maxc, maxr, max_response_map)
```
