# Computer Vision for Vegetation Detection with Satellite Imagery

Notebook for analyzing images and measuring the percentage of blue pixels in each file. The workflow scans common image formats, applies an HSV blue mask, saves a CSV summary, and can also display thumbnail overlays for quick visual inspection.

---

## Table of Contents

- [Overview](#overview)
- [What it does](#what-it-does)
- [Output](#output)
- [Requirements](#requirements)
- [How to use](#how-to-use)
- [Directory structure](#directory-structure)
- [License](#license)

---

## Overview

This project provides a simple yet effective computer vision pipeline for detecting blue pixels in satellite or aerial imagery. It is particularly useful for vegetation detection, water body identification, or any application where blue spectral signatures are of interest. The notebook processes a folder of images, applies an HSV colour mask to isolate blue regions, and generates a CSV summary with quantitative metrics.

---

## What it does

- **Reads images** from a specified directory
- **Supports multiple formats**: `jpg`, `jpeg`, `png`, `tif`, `tiff`
- **Detects blue areas** using an HSV (Hue, Saturation, Value) threshold
- **Cleans the mask** with basic morphological operations (erosion and dilation) to reduce noise
- **Exports results** to a CSV file with statistics for each image
- **Shows preview overlays** with the masked blue regions for quick visual inspection

---

## Output

The notebook writes a CSV file in the same image folder:

```
blue_percent_results.csv
```

### CSV columns

| Column | Description |
|--------|-------------|
| `file name` | Name of the image file |
| `percent blue` | Percentage of blue pixels in the image |
| `number of blue pixels` | Total count of pixels classified as blue |
| `total pixel count` | Total number of pixels in the image |

---

## Requirements

The notebook uses the following Python libraries:

- `opencv-python-headless` – image processing and computer vision
- `numpy` – numerical operations
- `pandas` – data handling and CSV export
- `matplotlib` – visualisation and previews

If any of these are missing, the notebook tries to install them automatically.

---

## How to use

1. Open the notebook: `imagensvnsp.ipynb`

2. Make sure your images are located in the input directory:

   ```
   d:\aguadoce\ImagensVNSP
   ```

3. Run the first cell to generate the CSV summary with blue pixel percentages.

4. Run the second cell to preview the images with blue overlays (optional).
