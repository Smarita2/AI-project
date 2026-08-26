# PixelReduce – Image Compression and Optimization System

**PixelReduce** is an image compression and optimization system developed using **Python**. The project is designed to reduce the file size of digital images while maintaining an acceptable level of visual quality.

The system provides a simple and user-friendly interface where users can upload an image, process it, view the optimized result, compare the original and compressed images, and download the optimized image.

## Project Overview

Images with high resolution and large file sizes require more storage space and can take longer to upload, download, or share. PixelReduce addresses this problem by applying image processing and compression techniques to reduce image size efficiently.

The project demonstrates an image optimization workflow consisting of:

1. Uploading an image
2. Reading and processing the image
3. Applying image compression techniques
4. Reducing the image file size
5. Maintaining acceptable visual quality
6. Comparing the original and optimized images
7. Downloading the compressed image

The main objective is to achieve a suitable balance between **image quality and file-size reduction**.

## Project Objectives

The major objectives of PixelReduce are:

* To reduce the storage size of digital images.
* To optimize images for faster uploading and sharing.
* To maintain acceptable image quality after compression.
* To provide a simple and user-friendly image processing interface.
* To demonstrate practical applications of image processing using Python.

## Key Features

* **Image Upload** – Allows users to upload images for processing.
* **Image Processing** – Processes the uploaded image using image processing techniques.
* **Image Compression** – Reduces the file size of the image.
* **Image Comparison** – Allows comparison between the original and optimized image.
* **File Size Analysis** – Shows the difference in file size before and after optimization.
* **Image Download** – Allows users to download the optimized image.
* **Interactive Interface** – Provides a simple interface using Streamlit.

## Project Structure

```text
AI-project/
│
└── PixelReduce/
    │
    ├── app.py                  # Main application
    ├── requirements.txt        # Required Python libraries
    └── README.md               # Project documentation
```

## Technologies Used

The project is developed using the following technologies:

| Technology                      | Purpose                                      |
| ------------------------------- | -------------------------------------------- |
| **Python**                      | Core programming language                    |
| **Streamlit**                   | Development of the interactive web interface |
| **Pillow (PIL)**                | Image processing and manipulation            |
| **Image Processing Techniques** | Image optimization and compression           |

The required Python libraries are listed in the `requirements.txt` file.

## Installation

### 1. Clone the Repository

Clone the project from GitHub:

```bash
git clone https://github.com/Smarita2/AI-project.git
```

Navigate to the PixelReduce project directory:

```bash
cd AI-project/PixelReduce
```

### 2. Create a Virtual Environment

Create a Python virtual environment:

```bash
python -m venv venv
```

Activate the virtual environment.

**Windows:**

```bash
venv\Scripts\activate
```

**Linux/macOS:**

```bash
source venv/bin/activate
```

### 3. Install Dependencies

Install the required packages using:

```bash
pip install -r requirements.txt
```

## Running the Application

After installing the dependencies, run the Streamlit application using:

```bash
streamlit run app.py
```

After executing the command, Streamlit will provide a local URL. Open the URL in a web browser to access the PixelReduce application.

## System Workflow

The overall workflow of PixelReduce can be represented as:

```text
                 ┌─────────────────┐
                 │  Upload Image   │
                 └────────┬────────┘
                          ↓
                 ┌─────────────────┐
                 │ Image Processing│
                 └────────┬────────┘
                          ↓
                 ┌─────────────────┐
                 │   Compression   │
                 └────────┬────────┘
                          ↓
                 ┌─────────────────┐
                 │ Optimized Image │
                 └────────┬────────┘
                          ↓
                 ┌─────────────────┐
                 │ Compare Results │
                 └────────┬────────┘
                          ↓
                 ┌─────────────────┐
                 │ Download Image  │
                 └─────────────────┘
```

## How the System Works

PixelReduce follows a straightforward image optimization process.

### Step 1: Image Upload

The user selects and uploads an image through the application interface.

### Step 2: Image Processing

The uploaded image is read and processed using Python's image processing capabilities.

### Step 3: Compression

Compression and optimization techniques are applied to reduce the image's file size while attempting to preserve its visual appearance.

### Step 4: Result Generation

The processed image is generated and displayed to the user.

### Step 5: Comparison

The original and optimized images can be compared to observe the effect of compression and the reduction in file size.

### Step 6: Download

The user can download the optimized image for further use.

## Image Optimization

The effectiveness of image compression depends on several factors, including:

* Original image size
* Image resolution
* Image format
* Image dimensions
* Compression settings
* Required output quality

Greater compression can produce a smaller file size, but excessive compression may reduce visual quality. Therefore, PixelReduce focuses on achieving a practical balance between **compression and quality**.

## Required Files

| File               | Description                                                  |
| ------------------ | ------------------------------------------------------------ |
| `app.py`           | Main application containing the PixelReduce implementation   |
| `requirements.txt` | Contains the Python dependencies required to run the project |
| `README.md`        | Provides documentation and instructions for the project      |

## Example Use Cases

PixelReduce can be useful in situations where reducing image size is important, such as:

* Optimizing images for websites
* Reducing images before sharing
* Saving storage space
* Reducing upload size
* Improving image transfer speed
* Managing collections of large images

## Important Note

The level of compression and resulting image quality may vary depending on the input image and its characteristics. Images with different formats, resolutions, and dimensions may produce different compression results.

The goal of the system is not simply to achieve the smallest possible file size, but to obtain a **reasonable reduction in size while maintaining acceptable image quality**.

## Team Members

This project was developed as a group project by:

* **Shine Pandey**
* **Smarita Karkee**
* **Sampada K.C.**
* **Tabita Mali**

## Project Purpose

PixelReduce was developed as an **academic project** to demonstrate the practical application of **Python, image processing, compression techniques, and interactive application development**.
