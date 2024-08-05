# Panorama Image Stitching

This project implements a panorama image stitching algorithm using computer vision techniques. The main components of the project include Harris corner detection, feature description, feature matching, and image warping to create panoramic images.

## Features

- Harris corner detection
- Simple descriptor and HOG (Histogram of Oriented Gradients) descriptor for feature description
- Feature matching using descriptor distances
- RANSAC (Random Sample Consensus) for robust estimation of affine transformation
- Image warping and blending to create panoramas

## Files

- `Harris.py`: Main script for running the panorama stitching process
- `panorama.py`: Contains implementations of core algorithms
- `utils.py`: Utility functions for image processing and visualization

## Dependencies

- NumPy
- SciPy
- scikit-image
- Matplotlib

## Usage

To run the panorama stitching process:

1. Ensure all dependencies are installed.
2. Place your input images in the same directory as the scripts.
3. Modify the `Harris.py` script to use your input images.
4. Run the `Harris.py` script:

```
python Harris.py
```

## Implementation Details

### Harris Corner Detection

The `harris_corners` function in `panorama.py` implements the Harris corner detection algorithm. It computes the Harris corner response map using the formula R = det(M) - k * (trace(M)^2).

### Feature Description

Two feature descriptors are implemented:

1. `simple_descriptor`: Normalizes image patches and flattens them into 1D arrays.
2. `hog_descriptor`: Implements the Histogram of Oriented Gradients (HOG) descriptor.

### Feature Matching

The `match_descriptors` function matches feature descriptors between two images based on the ratio of distances to the closest and second-closest matches.

### RANSAC

The `ransac` function implements the Random Sample Consensus algorithm to find a robust affine transformation between two sets of matched keypoints.

### Image Warping and Blending

The `warp_image` function in `utils.py` applies the computed affine transformation to warp images. The final panorama is created by blending the warped images.
