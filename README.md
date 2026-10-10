# Computer Vision Learning

A hands-on repository documenting my journey into computer vision with **Python, OpenCV, and NumPy**. It starts from the pixel level and builds toward object detection and deep learning.

![Python](https://img.shields.io/badge/Python-3.14-blue)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green)
![NumPy](https://img.shields.io/badge/NumPy-Arrays-orange)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)

---

## Overview

Every computer vision model starts with image data. This repository focuses on understanding how images are represented, manipulated, and prepared before any model is applied. Each concept is implemented in code and documented in a Jupyter notebook.

---

## What's Covered

### 1. Images as Data
- Built a 10×10 NumPy array and set pixel values by hand to draw a smiley face
- Understood grayscale images as matrices of intensity values (0-255)

### 2. Image Basics with OpenCV
- Loading images with `cv2.imread()`
- Displaying images with `cv2.imshow()` and Matplotlib
- Handling the BGR vs. RGB channel order difference
- Reading image dimensions with `.shape` (height, width, channels)

### 3. Resizing and Saving
- Resizing to exact dimensions with `cv2.resize()`
- Scaling with `fx` and `fy` factors
- Choosing interpolation methods (`INTER_AREA`, `INTER_LINEAR`, `INTER_CUBIC`, `INTER_NEAREST`)
- Saving results with `cv2.imwrite()`

### 4. Cropping
- Cropping with NumPy slicing: `img[y1:y2, x1:x2]`
- Selecting regions interactively with `cv2.selectROI()`

### 5. Video Basics
- Reading video frames with `cv2.VideoCapture()`

### 6. Color Spaces
Converted one image across six representations to see how each encodes the same scene:

| Color Space | Channels | Typical Use |
|-------------|----------|-------------|
| BGR | Blue, Green, Red | OpenCV's default format |
| RGB | Red, Green, Blue | Display with Matplotlib and most libraries |
| Grayscale | Intensity | Edge detection, simpler processing |
| HSV | Hue, Saturation, Value | Color-based segmentation |
| LAB | Lightness, A, B | Color analysis |
| YCrCb | Luma, Cr, Cb | Image and video processing |

> **Note:** `cv2.imshow()` treats every 3-channel image as BGR, so RGB, HSV, LAB, and YCrCb arrays look unusual when displayed directly. The underlying data is correct; only the channel meaning differs.

---

## Project Structure

```
computer_vision_learning/
├── data/               # Sample images and video used in the notebooks
├── notebooks/
│   └── images.ipynb    # Main notebook with all experiments
├── requirements.txt    # Python dependencies
└── README.md
```

---

## Getting Started

### Prerequisites
- Python 3.10 or newer
- Git

### Installation

```bash
# Clone the repository
git clone https://github.com/QaziMahadAhmad/computer_vision_learning.git
cd computer_vision_learning

# Create and activate a virtual environment
python -m venv .venv
source .venv/bin/activate        # On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### Run the Notebook

```bash
jupyter notebook notebooks/images.ipynb
```

Or open `notebooks/images.ipynb` in VS Code with the Jupyter extension.

> **Tip:** Update the image paths in the notebook to match your local directory. If `cv2.imshow()` windows cause problems in Jupyter, run the code as a regular Python script or display images with Matplotlib.

---

## Tech Stack

- **Python**
- **OpenCV** for image and video processing
- **NumPy** for array operations
- **Matplotlib** for visualization
- **Jupyter Notebook** for interactive experiments

---

## Roadmap

- [x] Pixels and NumPy image arrays
- [x] Loading, resizing, cropping, and saving images
- [x] Video capture basics
- [x] Color spaces
- [ ] Drawing shapes and text on images
- [ ] Thresholding and filtering
- [ ] Edge detection
- [ ] Contours and shape detection
- [ ] Face detection
- [ ] Object detection with YOLO

---

## About

I'm learning computer vision through practical implementation, one concept at a time. This repository is updated as I progress.

**Author:** Qazi Mahad Ahmad
**GitHub:** [@QaziMahadAhmad](https://github.com/QaziMahadAhmad)

Feedback and suggestions are welcome.
