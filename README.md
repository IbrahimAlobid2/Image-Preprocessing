# Image-Preprocessing
This repository focuses on various image preprocessing techniques to enhance image analysis. Below are the key steps and features implemented:

## Color Threshold
Applying color thresholding techniques to isolate specific color ranges and filter out unwanted regions in an image.

## HSV Color Space
Using the HSV (Hue, Saturation, Value) color space for better color segmentation and analysis.

### Create a Mask
Generating masks based on specific color ranges to isolate objects of interest.

## Mask and Add a Background Image
Applying a mask to an image and blending it with a background image to enhance visualization.

### Convert from RGB to HSV
Converting images from the RGB color space to HSV for more effective color-based processing.

### Define Pink and Hue Selection Thresholds
Setting thresholds to detect specific hues, such as pink, to identify and extract relevant regions.

## Mask the Image
Using the defined thresholds and HSV color space to create a binary mask for segmentation.

## Feature Extraction
Extracting meaningful features from the processed images to facilitate further analysis.

## Extracting the Average Brightness Using the V Channel
We implemented a feature to calculate the **average brightness** of an image using the **V (Value) channel** in the HSV color space. The V channel represents the brightness of each pixel.

### Calculation Process:
1. Convert the image to HSV color space.
2. Extract the **V channel** (brightness component).
3. Sum up all pixel values in the **V channel**.
4. Divide the sum by the total number of pixels to obtain the **average brightness**.

This feature provides an objective measurement of an image's brightness, which can be useful for various applications, including image enhancement and classification.
