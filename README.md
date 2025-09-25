


---

# YOLO Car License Plate Detection

This repository contains a **Jupyter Notebook** demonstrating how to train and run a YOLO-based object detection model to locate and crop vehicle license plates from images or video.

## Features

* 🚗 **Automatic License Plate Detection** – Detects car plates in real time or from still images.
* ⚡ **YOLOv8 Framework** – Uses the latest Ultralytics YOLO implementation.
* 🖼 **Dataset Preparation** – Includes guidance for labeling and splitting your custom dataset.
* 📊 **Evaluation & Visualization** – Precision/recall metrics, bounding-box overlays, and sample results.

## Quick Start

> **Requirements**
>
> * Python ≥ 3.9
> * Jupyter Notebook
> * [Ultralytics YOLO](https://docs.ultralytics.com/) (`pip install ultralytics`)
> * `opencv-python`, `matplotlib`, `numpy`

### 1️⃣ Clone and Install

```bash
git clone https://github.com/<your-username>/yolo-car-plates.git
cd yolo-car-plates
pip install -r requirements.txt
```

### 2️⃣ Launch the Notebook

```bash
jupyter notebook yolo-car-plates.ipynb
```

Follow the cells to:

1. Prepare or download a labeled car-plate dataset (e.g., YOLO format).
2. Train or fine-tune YOLOv8 on your dataset.
3. Evaluate the model and visualize predictions.

### 3️⃣ Quick Inference (Command Line)

After training and saving a model checkpoint (e.g., `runs/detect/train/weights/best.pt`):

```bash
yolo detect predict model=runs/detect/train/weights/best.pt source=path/to/test_image.jpg
```

Results (images with bounding boxes) will appear in `runs/detect/predict/`.

## Repository Structure

```
├── yolo-car-plates.ipynb   # Main notebook (training + inference)
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```

## Customization

* Adjust YOLO hyperparameters (`data.yaml`, image size, epochs) to match your dataset.
* Integrate live webcam or video streams by setting `source=0` or a video file path.

---

Would you like me to generate a starter `requirements.txt` for YOLOv8, OpenCV, and notebook dependencies?
