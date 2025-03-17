# Hole-detection-on-metal-parts-using-YOLO-models

## 📌 Project Overview
This project focuses on detecting different types of holes (e.g., **threaded, non-threaded**) on metal parts using **YOLO (You Only Look Once)** object detection models. Due to limited labeled data, **data augmentation** techniques were applied to enhance the dataset before training the model.

## 🚀 Workflow
### 1️⃣ **Data Collection & Annotation**
- Hand-annotated metal part images using **LabelImg** to create bounding boxes for different hole types.
- Saved annotations in YOLO format (TXT files with class labels and coordinates).

### 2️⃣ **Data Augmentation**
- Used **Albumentations** to generate augmented images while preserving bounding box information.
- Applied transformations such as rotation, flipping, brightness adjustments, and scaling to improve model generalization.

### 3️⃣ **Model Training**
- Trained a **YOLOv5 model** on the annotated dataset.
- Fine-tuned hyperparameters (batch size, learning rate, IoU threshold) for optimal performance.
- Utilized **pretrained weights** to enhance accuracy due to the small dataset size.

### 4️⃣ **Inference & Output Generation**
- Ran inference on test images to detect holes and classify them correctly.
- Exported results in **JSON format**, containing:
  - Detected hole type
  - Confidence score
  - Bounding box coordinates

## 🔥 Challenges & Solutions
| **Challenge** | **Solution** |
|--------------|-------------|
| Limited dataset | Used **data augmentation** to expand training data |
| Maintaining bounding box integrity | Used **Albumentations** to ensure bounding boxes adapt correctly to transformations |
| Model overfitting | Used **pretrained YOLO weights** and **regularization techniques** |

## 📊 Results
- Achieved **high detection accuracy** with minimal false positives.
- Successfully classified **threaded & non-threaded holes** with **YOLOv5**.
- **Exported detection results** in structured **JSON format** for easy integration.

## 📂 File Structure
```
├── data/
│   ├── images/              # Raw & Augmented images
│   ├── labels/              # YOLO annotation TXT files
├── models/
│   ├── yolov5/              # YOLOv5 model files
├── results/
│   ├── output_json/         # Detected results in JSON format
│   ├── visualization/       # Images with bounding boxes
├── training_script.py       # YOLO training script
├── inference.py             # Model inference script
├── requirements.txt         # Dependencies
├── README.md                # Project Documentation
```

## 🛠️ Tech Stack
- **Python**
- **YOLOv5** (Ultralytics)
- **Albumentations** (Data Augmentation)
- **LabelImg** (Annotation Tool)

## 🎯 Future Improvements
- Train on a **larger dataset** for better generalization.
- Experiment with **YOLOv8** for improved accuracy.
- Deploy the model using **Flask/FastAPI** for real-time detection.

## 📩 Contact
For any queries or collaborations, feel free to reach out! 😊
