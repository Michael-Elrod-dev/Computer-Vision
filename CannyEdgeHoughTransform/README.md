# Canny Edge Detection

This project implements the Canny edge detection algorithm along with additional image processing techniques like the Hough transform. It's designed for educational purposes and demonstrates various steps involved in edge detection and line detection in images.

## Features

- Canny edge detection algorithm implementation
- Gaussian smoothing
- Gradient calculation
- Non-maximum suppression
- Double thresholding
- Edge tracking by hysteresis
- Hough transform for line detection
- Visualization of intermediary and final results

## Requirements

- Python 3.x
- NumPy
- Matplotlib
- scikit-image

## Usage

1. Ensure you have all the required libraries installed:

   ```
   pip install numpy matplotlib scikit-image
   ```

2. Place your input images in the `images/objects/` directory.

3. Run the `CannyEdge.py` script:

   ```
   python CannyEdge.py
   ```

4. The script will process the images and display the results, including:
   - Original and smoothed images
   - Gradient magnitudes and directions
   - Non-maximum suppressed edges
   - Final detected edges
   - Hough transform results (if applicable)

## File Structure

- `CannyEdge.py`: Main script for running the edge detection and visualization
- `edge.py`: Contains implementations of various image processing functions

## Customization

You can adjust parameters in the `CannyEdge.py` file to experiment with different results:

- `kernel_size` and `sigma` for Gaussian smoothing
- `high` and `low` thresholds for edge detection
- Parameters for the Hough transform
