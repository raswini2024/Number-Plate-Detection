#  License Plate Detection using OpenCV and EasyOCR

This project detects license plates from vehicle images using **image processing techniques** and extracts text using **EasyOCR**, a deep learning-based Optical Character Recognition library.

---

##  Objective

To build a Python-based tool that:
- Detects a license plate from an image using **OpenCV** techniques.
- Extracts text from the plate using **EasyOCR** (which uses a pre-trained deep learning model).
- Displays the detected number plate text and region visually.

---

##  Technologies & Libraries Used

| Tool | Purpose |
|------|---------|
| Python | Programming Language |
| OpenCV | Image processing & contour detection |
| EasyOCR | Text detection and recognition |
| NumPy | Matrix operations |
| imutils | Image resizing & manipulation |
| Matplotlib | Image display |

---

##  Methodology (Step-by-Step)

###  1. **Image Input**
- Load the vehicle image using OpenCV.

###  2. **Preprocessing**
- Convert image to grayscale.
- Apply Bilateral Filtering to preserve edges and reduce noise.

###  3. **Edge Detection**
- Use **Canny Edge Detection** to find sharp edges.

###  4. **Contour Detection**
- Find all contours in the edge image.
- Sort and filter to get rectangular contours which likely contain the plate.

###  5. **License Plate Localization**
- Approximate the contour to find a polygon (ideally with 4 corners).
- Crop that region of interest (ROI) from the original image.

###  6. **Text Detection with EasyOCR**
- Apply EasyOCR to the cropped region.
- Extract and display the license plate number.

###  7. **Display Output**
- Annotate the image with detected text and bounding boxes.

---

##  Model Details

- **EasyOCR** internally uses a **CRNN (Convolutional Recurrent Neural Network)** architecture with **CTC Loss**.
- It is pre-trained on multiple languages and scripts.
- No training or dataset preparation is required for this project.

---
