# Digital Image Processing — Lab 01

## Introduction

This repository contains the implementation of **Lab 01: Introduction to Digital Image Processing using Python**.

The lab introduces the basic concepts of digital images, image representation, pixels, RGB channels, grayscale images, sampling, quantization, and basic image manipulation using Python.

## Technologies & Libraries

* Python
* NumPy
* Matplotlib
* Pillow (PIL)
* OpenCV

## Installation

Install the required libraries using:

```bash
pip install numpy matplotlib pillow opencv-python
```

## Experiments

### Experiment 1 — Create a Simple Digital Image

Created a simple grayscale image using a NumPy array and displayed it using Matplotlib.

### Experiment 2 — Grayscale Gradient

Generated grayscale gradient images using different intensity ranges.

### Experiment 3 — Load a Real Image

Loaded and displayed a real image using Pillow.

### Experiment 4 — Image Dimensions

Examined the image shape, dimensions, channels, and data type.

### Experiment 5 — Examine Pixel Values

Accessed individual pixel values and examined their RGB/RGBA components.

### Experiment 6 — Display RGB Channels

Extracted and separately displayed the Red, Green, and Blue channels.

### Experiment 7 — RGB to Grayscale

Converted a color image into grayscale using Pillow and OpenCV.

### Experiment 8 — Image Size and Number of Pixels

Calculated the image height, width, and total number of pixels.

### Experiment 9 — Access and Modify Pixels

Accessed individual pixels and modified specific pixels and regions of the image.

### Experiment 10 — Cropping

Cropped a selected region from the image using NumPy slicing.

### Experiment 11 — Resizing

Resized an image using OpenCV.

### Experiment 12 — Sampling

Applied different sampling factors to demonstrate changes in spatial resolution.

### Experiment 13 — Quantization

Applied quantization to reduce the number of intensity levels in a grayscale image.

### Experiment 14 — Save Processed Image

Saved the processed/quantized image using Pillow.

---

# Lab Tasks

## Task 1 — Image Information

Loaded an image and displayed its:

* Width
* Height
* Number of channels
* Data type
* Number of pixels

## Task 2 — Pixel Analysis

Selected five pixels from the image and displayed their intensity/RGB values.

## Task 3 — RGB Channels

Extracted and separately displayed:

* Red Channel
* Green Channel
* Blue Channel

## Task 4 — Image Manipulation

Performed the following operations:

1. Cropped the central region
2. Resized the image to **256 × 256**
3. Converted it to grayscale
4. Saved the final result

## Task 5 — Sampling

Generated image versions using sampling factors:

* 1
* 2
* 4
* 8

This demonstrates how reducing the number of spatial samples affects image resolution and detail.

## Task 6 — Quantization

Quantized a grayscale image using:

* 256 intensity levels
* 64 intensity levels
* 16 intensity levels
* 8 intensity levels
* 4 intensity levels
* 2 intensity levels

This demonstrates how reducing the number of intensity levels affects image brightness and the number of visible shades.

---

# Important Concepts

### Sampling

Sampling determines **how many spatial samples/pixels are used to represent an image**.

> Sampling → Number of pixels / spatial resolution

### Quantization

Quantization determines **how many intensity or brightness values each pixel can have**.

> Quantization → Pixel brightness/intensity levels

### Sampling vs Quantization

| Concept      | Controls                              |
| ------------ | ------------------------------------- |
| Sampling     | Number of pixels                      |
| Quantization | Number of intensity/brightness levels |

For example:

* Sampling factor 8 → fewer spatial samples/pixels
* Quantization level 2 → only two intensity levels

---

# PIL vs OpenCV

Both Pillow (PIL) and OpenCV can be used for image processing, but they have different strengths.

### Pillow (PIL)

Commonly used for simple image handling and manipulation:

```python
from PIL import Image

image = Image.open("sample.jpg")
```

### OpenCV

Commonly used for image processing and computer vision:

```python
import cv2

image = cv2.imread("sample.jpg")
```

One important difference is color channel order:

* PIL/Matplotlib → RGB
* OpenCV → BGR

When displaying an OpenCV image with Matplotlib, conversion may be required:

```python
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
```

---

# Learning Outcomes

After completing this lab, I learned how to:

* Represent images using NumPy arrays
* Understand pixels and image dimensions
* Work with RGB and RGBA channels
* Convert RGB images to grayscale
* Access and modify individual pixels
* Crop and resize images
* Understand sampling and spatial resolution
* Understand quantization and intensity levels
* Save processed images
* Perform basic image processing using Pillow and OpenCV

---

# Repository Structure

```text
Digital-Image-Processing-Lab-01/
│
├── Lab_01.ipynb
├── sample.jpg
├── quantized_image.jpg
├── task4_result.jpg
└── README.md
```

> File names may vary depending on the implementation.

---

## Conclusion

This lab provides a foundation for understanding **Digital Image Processing** using Python. It covers the fundamental concepts required for working with digital images and introduces practical image processing techniques using NumPy, Matplotlib, Pillow, and OpenCV.
