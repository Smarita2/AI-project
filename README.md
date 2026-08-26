#🎨 PixelReduce
Image Compression via K-Means Color Quantization
Project Overview

PixelReduce is an image compression and optimization system that uses K-Means color quantization to reduce the number of colors in an image while preserving its overall visual appearance.

Features
Adjustable Color Count – Supports K values from 2 to 64.
Automatic Downscaling – Large images are automatically downscaled for better performance.
Pixel Sampling – Samples pixels when the image contains more than 20,000 pixels.
PSNR Quality Metric – Measures the quality of the compressed image.
Estimated Size Reduction – Estimates the reduction in image size.
Color Palette Extraction – Displays representative colors with HEX codes.
Posterize Mode – Creates a bold, simplified artistic appearance.
Median-Cut Comparison – Compares K-Means with PIL's median-cut quantization.
PNG Download – Allows users to download the processed image.
How It Works
1. Image Preprocessing

The uploaded image is converted into an appropriate RGB representation. Large images are automatically downscaled to improve processing performance.

2. Pixel Sampling

If the image contains more than 20,000 pixels, a representative sample of pixels is selected for training the K-Means model.

3. K-Means Clustering

K-Means clustering groups similar RGB pixel colors into K clusters.

4. Color Quantization

Each pixel is replaced by the centroid color of its assigned cluster, reducing the number of distinct colors.

5. Quality Evaluation

The compressed image is compared with the original image using PSNR (Peak Signal-to-Noise Ratio).

6. Color Palette Extraction

The representative centroid colors are extracted and displayed along with their HEX color codes.

System Workflow
Upload Image
      ↓
Image Preprocessing
      ↓
Pixel Sampling
      ↓
K-Means Clustering
      ↓
Color Quantization
      ↓
Quality / PSNR
      ↓
Color Palette
      ↓
Optimized Image
      ↓
PNG Download
Tech Stack
Technology	Purpose
Python	Core programming language
Streamlit	Web application interface
NumPy	Numerical and pixel operations
Pillow (PIL)	Image processing
Scikit-learn	K-Means clustering
Project Structure
AI-project/
│
├── .gitignore
├── README.md
├── app.py
└── requirements.txt
Installation
Clone the Repository
git clone https://github.com/Smarita2/AI-project.git
Create Virtual Environment
python -m venv venv
Activate Virtual Environment

Windows:

venv\Scripts\activate

Linux/macOS:

source venv/bin/activate
Install Dependencies
pip install -r requirements.txt
Running the Application
streamlit run app.py
Adjusting the Compression

The K value determines the number of representative colors.

Lower K
Fewer Colors
     ↓
Greater Color Reduction
     ↓
Lower Visual Detail
Higher K
More Colors
     ↓
Better Color Representation
     ↓
Higher Visual Quality
Quality Measurement

PixelReduce uses PSNR (Peak Signal-to-Noise Ratio) to measure the similarity between the original and compressed images.

Higher PSNR → Better similarity to the original.
Lower PSNR → Greater difference from the original.
Posterize Mode

Posterize Mode reduces the number of distinct tones to produce a bold, simplified, artistic appearance.

Median-Cut Comparison

PixelReduce provides an optional comparison between:

Original Image
      ↓
 ┌──────────────┐
 ↓              ↓
K-Means     Median-Cut
 ↓              ↓
Quantized    Quantized
 Image         Image
 └──────┬───────┘
        ↓
 Compare Results
Example Use Cases
Image color reduction
Image optimization
Storage optimization
Web image preparation
Color palette generation
Artistic posterization
Learning K-Means clustering
Studying image compression
Project Purpose

PixelReduce was developed as an academic project to demonstrate the practical application of K-Means clustering, image processing, color quantization, and Python-based web application development.

Team Members
Shine Pandey
Smarita Karkee
Sampada K.C.
Tabita Mali
