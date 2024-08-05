# Optical Flow and Feature Tracking

This project implements various optical flow and feature tracking algorithms, primarily focusing on the Lucas-Kanade method and its variations. It provides tools for detecting keypoints in images, tracking them across frames, and visualizing the results.

## Features

- Implementation of the Lucas-Kanade optical flow algorithm
- Iterative and pyramidal Lucas-Kanade methods
- Feature detection using Harris corner detector
- Feature tracking across multiple frames
- Visualization of keypoints and optical flow vectors
- Simple object tracking implementation

## Dependencies

- Python 3.x
- NumPy
- scikit-image
- Matplotlib
- IPython (for notebook-style visualizations)

## Usage

1. Ensure all dependencies are installed.
2. Place your image sequences in the `images` directory.
3. Run the main script:

```
python Lukas.py
```

4. The script will generate visualizations of the detected keypoints, optical flow vectors, and tracked features.

## File Structure

- `Lukas.py`: Main script containing the implementation and visualization code
- `motion.py`: Contains core implementations of optical flow algorithms
- `utils.py`: Utility functions for loading images, visualizing results, etc.

## Implementation Details

The project includes the following key components:

1. **Basic Lucas-Kanade Method**: Estimates optical flow vectors for detected keypoints between two consecutive frames.
2. **Iterative Lucas-Kanade Method**: Refines the optical flow estimates through multiple iterations.
3. **Pyramidal Lucas-Kanade Method**: Implements a multi-scale approach for handling larger displacements.
4. **Feature Tracking**: Tracks detected keypoints across multiple frames, handling occluded or lost points.
5. **Object Tracking**: A simple implementation of object tracking using the Lucas-Kanade method.
