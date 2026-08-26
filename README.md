# 🎨 PixelReduce

# Image Compression via K-Means Color Quantization

PixelReduce is an image compression and optimization system that uses **K-Means color quantization** to reduce the number of colors in an image while preserving its overall visual appearance.

The project is developed as a **Streamlit web application**. It clusters image pixels in RGB color space and replaces each pixel with the corresponding cluster's centroid color.

# Project Overview

Digital images often contain thousands or millions of different colors. Many of these colors may be visually similar and unnecessary for representing the image.

PixelReduce uses **K-Means clustering** to group similar RGB colors into a smaller number of representative colors. Each pixel is then replaced by the centroid color of the cluster to which it belongs.

The user can control the number of colors using the **K value**, allowing them to choose the desired balance between image quality and color reduction.

# Features

- **Adjustable Color Count** – Supports K values from **2 to 64**.
- **Automatic Downscaling** – Large images are automatically downscaled to improve processing performance.
- **Pixel Sampling** – Samples pixels when the number of pixels exceeds 20,000.
- **PSNR Quality Metric** – Calculates Peak Signal-to-Noise Ratio to evaluate image quality.
- **Estimated Size Reduction** – Provides an estimate of image size reduction.
- **Color Palette Extraction** – Displays representative colors with their HEX codes.
- **Posterize Mode** – Provides a bold and artistic appearance.
- **Median-Cut Comparison** – Allows comparison with PIL's built-in median-cut quantization.
- **PNG Download** – Allows users to download the processed image.

# How It Works

# 1. Image Preprocessing

The uploaded image is converted into an appropriate RGB representation. Large images are automatically downscaled to a suitable working dimension.

# 2. Pixel Sampling

If the image contains more than **20,000 pixels**, a representative sample of pixels is selected for training the K-Means model.

This reduces computation time while still providing a representative set of colors.

# 3. K-Means Clustering

K-Means clustering is applied to the RGB pixel values.

```text
K-Means
n_clusters = K
initialization = k-means++

The algorithm groups similar colors into K clusters.

4. Color Quantization

Each cluster has a centroid color representing the average RGB color of that cluster.

Every pixel in the image is assigned to its nearest cluster and replaced with its cluster's centroid color.

Original Colors
       ↓
RGB Pixel Values
       ↓
K-Means Clustering
       ↓
K Representative Colors
       ↓
Replace Pixels with Centroid Colors
       ↓
Compressed Image
5. Quality Evaluation

The compressed image is compared with the original image using PSNR (Peak Signal-to-Noise Ratio).

A higher PSNR generally indicates that the compressed image is closer to the original image in terms of pixel-level quality.

6. Color Palette

The representative centroid colors are extracted and displayed as a color palette along with their HEX color codes.

System Workflow
                  ┌──────────────────┐
                  │   Upload Image   │
                  └────────┬─────────┘
                           ↓
                  ┌──────────────────┐
                  │ Image Preprocess │
                  └────────┬─────────┘
                           ↓
                  ┌──────────────────┐
                  │ Pixel Sampling   │
                  └────────┬─────────┘
                           ↓
                  ┌──────────────────┐
                  │ K-Means Clustering│
                  └────────┬─────────┘
                           ↓
                  ┌──────────────────┐
                  │ Color Quantization│
                  └────────┬─────────┘
                           ↓
              ┌────────────┴────────────┐
              ↓                         ↓
     ┌─────────────────┐       ┌─────────────────┐
     │ Quality / PSNR  │       │ Color Palette   │
     └─────────────────┘       └─────────────────┘
              │                         │
              └────────────┬────────────┘
                           ↓
                  ┌──────────────────┐
                  │ Optimized Image  │
                  └────────┬─────────┘
                           ↓
                  ┌──────────────────┐
                  │   PNG Download   │
                  └──────────────────┘
Tech Stack
Technology	Purpose
Python	Core programming language
Streamlit	Interactive web application interface
NumPy	Numerical operations and pixel data manipulation
Pillow (PIL)	Image loading and processing
Scikit-learn	K-Means clustering implementation

Tech Stack: Python · Streamlit · NumPy · Pillow · Scikit-learn

Project Structure
AI-project/
│
├── .gitignore
├── README.md
├── app.py
└── requirements.txt
Installation
1. Clone the Repository
git clone https://github.com/Smarita2/AI-project.git
2. Navigate to the Project Directory
cd AI-project
3. Create a Virtual Environment
python -m venv venv
4. Activate the Virtual Environment

Windows:

venv\Scripts\activate

Linux/macOS:

source venv/bin/activate
5. Install Dependencies
pip install -r requirements.txt
Running the Application

Start the Streamlit application using:

streamlit run app.py

After running the command, Streamlit will provide a local URL. Open the URL in a web browser to access the application.

Adjusting the Compression

The K value controls the number of representative colors used in the compressed image.

Lower K
Lower K
   ↓
Fewer Colors
   ↓
Greater Color Reduction
   ↓
Lower Visual Detail
Higher K
Higher K
   ↓
More Colors
   ↓
Better Color Representation
   ↓
Closer to Original Image

PixelReduce supports:

K = 2 to 64

This allows users to experiment with different levels of color quantization.

Quality Measurement

PixelReduce uses PSNR (Peak Signal-to-Noise Ratio) as a quality metric.

PSNR measures the difference between the original image and the compressed image.

Higher PSNR → Compressed image is more similar to the original.
Lower PSNR → Greater difference from the original image.

The PSNR value helps users understand the trade-off between color reduction and image quality.

Color Palette

After K-Means clustering, the application extracts the cluster centroids and displays them as the image's representative color palette.

Each color is presented using its HEX code, making it easy to identify and reuse the dominant colors generated by the compression process.

Posterize Mode

PixelReduce also provides a Posterize Mode for users who want a more visually distinctive result.

Instead of focusing only on compression, posterization reduces the number of distinct tones and creates a bold, simplified, artistic appearance.

Median-Cut Comparison

PixelReduce optionally provides a comparison with PIL's median-cut quantization.

This allows users to compare two different approaches to reducing the number of colors in an image.

Original Image
      │
      ├───────────────┐
      ↓               ↓
 K-Means          Median-Cut
      ↓               ↓
Quantized         Quantized
  Image              Image
      │               │
      └───────┬───────┘
              ↓
        Compare Results
Example Use Cases
Reducing image color complexity
Optimizing images for storage
Preparing images for web applications
Creating simplified color palettes
Generating posterized or artistic images
Studying image compression techniques
Demonstrating K-Means clustering in image processing
Important Note

The compression result depends on factors such as the original image, resolution, color distribution, and selected K value.

A smaller K value produces fewer representative colors and can create a stronger color reduction or artistic effect, while a larger K value generally preserves more color information.

Therefore, PixelReduce focuses on demonstrating the trade-off between color reduction, image quality, and computational efficiency.

Required Files
File	Description
app.py	Main Streamlit application containing the image compression implementation
requirements.txt	Contains the required Python dependencies
README.md	Project documentation and usage instructions
#Team Members

This project was developed as a group project by:

Shine Pandey
Smarita Karkee
Sampada K.C.
Tabita Mali
#Project Purpose
PixelReduce was developed as an academic project to demonstrate the practical application of K-Means clustering, image processing, color quantization, and Python-based application development.
The project provides hands-on implementation of an image compression technique while allowing users to explore the relationship between number of colors, image quality, and compression.

