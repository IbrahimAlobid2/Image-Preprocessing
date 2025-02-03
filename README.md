# 1-image_Pre-process
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

______________________________________________________
# 2_Filters_Edge_Detection

## Filters
In addition to taking advantage of color information, we also have knowledge about patterns of grayscale intensity in an image. Intensity is a measure of light and dark similar to brightness, and we can use this knowledge to detect other areas or objects of interest.
For example, you can often identify the edges of an object by looking at an abrupt change in intensity which happens when an image changes from a very dark to light area.

##  Fourier Transforms

## High and low frequency
____________________________________________
### Creating a Filter, Edge Detection  (High-pass Filters)
#### laplacian
#### sobelx and sobely 
#### prewitt_x and prewitt_y
### Test performance with a high-pass filter 
______________________________________________________
### Low-pass Filters

#### Gaussian Blur 

______________________________________________________
## High and Low Pass Filters
Now, you might be wondering, what makes filters high and low-pass; why is a Sobel filter high-pass and a Gaussian filter low-pass?

Well, you can actually visualize the frequencies that these filters block out by taking a look at their fourier transforms. The frequency components of any image can be displayed after doing a Fourier Transform (FT). An FT looks at the components of an image (edges that are high-frequency, and areas of smooth color as low-frequency), and plots the frequencies that occur as points in spectrum. So, let's treat our filters as small images, and display them in the frequency domain!
______________________________________________________

#  Canny edge detection

# Edges to Boundaries and Shapes
## Hough Lines

## Find lines using a Hough transform

## Hough Circle Detection

______________________________________________________

# Canny Edge Detection in Action
it's time to use it to find the edges of the lane lines in an image of the road. So let's give that a try.


______________________________________________________



# Dilation and Erosion


Dilation and erosion are known as **morphological operations.** They are often performed on binary images, similar to contour detection. Dilation enlarges bright, white areas in an image by adding pixels to the perceived boundaries of objects in that image. Erosion does the opposite: it removes pixels along object boundaries and shrinks the size of objects.

______________________________________________________
 
# Image segmentation 

Now that we are familiar with a few simple feature types, it may be useful to look at how we can group together different parts of an image by using these features. Grouping or segmenting images into distinct parts is known as image segmentation.
## 1- Finding Contours

## 2- K-means Clustering

______________________________________________________
# 3_Feature_Extraction

## 1- Corner Detection

### Harris Corner Detection

## 2_ Image pyramids

Take a look at how downsampling with image pyramids works.



# Feature Extraction
### 1 _ Feature Extraction
The purpose of this section is to implement a function to extract features from an image. A feature is a point of interest in an image defined by its image pixel coordinates. A descriptor is an n-dimensional vector that summarizes the image information around the detected feature. The following figure illustrates these properties.

### Here is a  common feature detectors:
* Scale-Invariant Feature Transform (SIFT)
* Oriented FAST and Rotated BRIEF (ORB)



### 2 - Feature Matching

The purpose of this section is to implement a function to match features in a sequence of images. Feature matching is the process of establishing correspondences between two images of the same scene.

The Brute-Force matcher compares one descriptor in the first image to all descriptors in the second image. The algorithm then matches the descriptor with the shortest distance to the descriptor in the first image.

FLANN stands for Fast Library for Approximate Nearest Neighbors. It contains a collection of algorithms optimized for fast neighbor search in datasets and high dimensional features.

# Histograms of Oriented Gradients (HOG)

As we saw with the ORB algorithm, we can use keypoints in images to do keypoint-based matching to detect objects in images. These type of algorithms work great when you want to detect objects that have a lot of consistent internal features that are not affected by the background. For example, these algorithms work well for facial detection because faces have a lot of consistent internal features that don’t get affected by the image background, such as the eyes, nose, and mouth. However, these type of algorithms don’t work so well when attempting to do more general object recognition.


