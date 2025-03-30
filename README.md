# Comparison of Connectivity in Image Segmentation

## Overview
This project demonstrates the use of **connectedness** for image segmentation in binary images. It focuses on comparing **4-connectivity** and **8-connectivity**, widely used methods to identify connected components in an image. By visualizing the results side by side, the project showcases how different connectivity rules affect segmentation outcomes.

## Features
- Binary image thresholding to simplify segmentation.
- **4-connectivity**:
  - Groups pixels based on horizontal and vertical adjacency.
- **8-connectivity**:
  - Groups pixels based on horizontal, vertical, and diagonal adjacency.
- Color-coded visualization for connected components.

## Requirements
- Python 3.x
- OpenCV library (`cv2`)
- NumPy library (`numpy`)
- Matplotlib library (`matplotlib`)

## Installation
Run the following commands to install the required libraries:
```bash
pip install opencv-python
pip install numpy
pip install matplotlib
```

## Usage
1. Place the input image in the project directory.
2. Update the `image_path` variable in the code with the name of your image file.
3. Run the script to generate the segmentation results and visualizations:
```bash
python connectivity_comparison.py
```

## Output
The script produces the following visualizations:
1. **Original Image**: Displays the grayscale input image.
2. **Binary Image**: Shows the binarized version of the input image after thresholding.
3. **4-Connectivity Segmentation**: Illustrates connected components using 4-connectivity rules.
4. **8-Connectivity Segmentation**: Illustrates connected components using 8-connectivity rules.

The connected components are visualized with random colors to highlight distinct regions.

## Notes
- **Connectivity Difference**:
  - **4-connectivity** is stricter and may result in smaller connected regions as it ignores diagonal relationships.
  - **8-connectivity** is more flexible and often results in larger connected regions due to diagonal inclusion.
- You can experiment with different threshold values to analyze how segmentation changes.

## Future Enhancements
- Add support for **custom connectivity rules** (e.g., extended connectivity beyond 8-connected neighborhoods).
- Apply connected component analysis to multi-channel (color) images for advanced segmentation.
