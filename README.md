# ExtractText_From_Imgaes
To create your personal GitHub project for extracting text from images using Python, OpenCV, and Tesseract, you can follow these steps:

### 1. **Project Setup on GitHub**:
- **Repository Name**: `text-extraction-from-images`
- **Description**: A Python project that extracts text from images using OpenCV, Tesseract OCR, and a Tkinter-based GUI.
- **License**: MIT License (or any other license you prefer)
- **Readme**: Add the following content to the README file.

### 2. **Project Description for README**:

---

# Text Extraction from Images using OpenCV and Tesseract OCR

## Overview

This project demonstrates how to extract text from images using Python. It uses **OpenCV** for image processing, **Tesseract OCR** for optical character recognition, and **Tkinter** for creating a simple graphical user interface (GUI) to upload and extract text from images.

## Key Features
- **Libraries Used**:
  - OpenCV for image processing
  - Tesseract OCR for text recognition
  - Tkinter for the GUI
- **Easy to Use**: Just upload an image and extract the text from it with a button click.
- **Supports Multiple Image Formats**: Works with .jpg, .png, .bmp, and .tiff formats.

## Project Approach

### Tesseract OCR
Tesseract is an open-source engine for optical character recognition (OCR). It efficiently reads and extracts text from images and is easy to use within Python. This project integrates it with OpenCV to pre-process the images and Tkinter for the GUI interface.

### Steps for Text Extraction
1. **Image Upload**: The user uploads an image through a dialog box.
2. **Image Pre-processing**: OpenCV resizes and converts the image from BGR (OpenCV format) to RGB (for Tesseract OCR).
3. **Text Extraction**: The `pytesseract.image_to_data()` function extracts the text from the image and prints it on the screen.

## Requirements
- Python 3.x
- OpenCV
- Tesseract OCR
- Tkinter (included with Python)
- Pillow (Python Imaging Library)

## Installation

1. **Install the Required Libraries**:
   ```
   pip install opencv-python pytesseract Pillow
   ```
   
2. **Tesseract Installation**:
   Download and install Tesseract from [here](https://github.com/tesseract-ocr/tesseract).

   Set the `tesseract_cmd` path in the code:
   ```python
   pytesseract.pytesseract.tesseract_cmd = 'C:\\Program Files\\Tesseract-OCR\\tesseract.exe'
   ```

## Usage

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/text-extraction-from-images.git
   ```

2. **Run the Script**:
   Open a terminal, navigate to the project directory, and run the `main.py` script:
   ```bash
   python main.py
   ```

3. **Upload an Image**:
   - Click the **Upload an Image** button.
   - Select an image from your computer.
   - Click **Extract Text** to display the extracted text on the GUI.

## Explanation of Code

- **OpenCV for Image Pre-processing**: 
  We use OpenCV's `cv2.imread()` to read the image and `cv2.resize()` to resize it. 
  The image is then converted from BGR to RGB using `cv2.cvtColor()` because Tesseract expects RGB images.

- **Tesseract for Text Extraction**:
  We use the `pytesseract.image_to_data()` function, which returns the extracted text from the image in a structured format.

- **Tkinter for GUI**:
  Tkinter provides an easy-to-use interface for selecting images and displaying the extracted text. It handles image uploads through `filedialog.askopenfilename()` and displays the result in labels.

## Project Output

After running the script, a GUI window will appear. You can upload an image, and the extracted text will be printed on the screen.

