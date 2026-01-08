# Automated-Quality-Inspection-System
## Introduction
This project implements an **Automated Quality Inspection System for Manufacturing**
using deep learning and computer vision techniques.

The system focuses on detecting defects in Printed Circuit Boards (PCBs) automatically
to reduce manual inspection effort and improve manufacturing quality.
A YOLOv8 object detection model is used to identify and localize different PCB defects
from images.

3️⃣ Dataset Description
## Dataset
This project uses a **Pascal VOC format dataset** for quality inspection.

- Dataset Type: Pascal VOC
- Annotation Format: XML
- Image Type: PCB images
- Total Images: 693
- Total Defect Instances: 2,953

4️⃣ Defect Classes
## Defect Classes
The dataset contains the following six defect classes:
- missing_hole
- mouse_bite
- open_circuit
- short
- spur
- spurious_copper
  <img width="700" height="277" alt="Screenshot 2026-01-08 030925" src="https://github.com/user-attachments/assets/9bb5cbe0-a0b0-4f72-be27-b614cfb2648b" />


5️⃣ Annotation Conversion (Pascal VOC → YOLO)
## Annotation Conversion
The original annotations were provided in Pascal VOC XML format.
These annotations were converted into YOLO format to train the YOLOv8 model.
Each YOLO label file contains class ID and normalized bounding box coordinates.

## Dataset and Annotation Verification
Before training the YOLOv8 model, the dataset and XML annotations were verified
to ensure correctness and completeness.

The verification process confirmed:
- Total XML files: 693
- Total defect bounding boxes: 2,953
- Total defect classes: 6

This step ensures that the Pascal VOC annotations were successfully parsed
and are suitable for training.
<img width="1093" height="154" alt="Screenshot 2026-01-08 065609" src="https://github.com/user-attachments/assets/2a05ec21-30ad-4b70-9d3d-9a2a1063c28f" />

6️⃣ Model Training 📸
## Model Training
The YOLOv8 model was trained using Google Colab as part of the automated
quality inspection system.
The training process shows epoch-wise progress, loss values, and evaluation metrics.
🔽 IMAGE HERE:
<img width="700" height="277" alt="image" src="https://github.com/user-attachments/assets/46286540-c4df-4992-9678-dca6c3078270" />

7️⃣ Detection Results 📸
## Detection Results
The trained YOLOv8 model was used to perform inference on PCB images.
During inference, the model processed 693 images and detected PCB defects
along with prediction time per image, demonstrating real-time capability.
<img width="700" height="277" alt="image" src="https://github.com/user-attachments/assets/6ff1792f-87b0-48ce-8bee-98a52dddf7a3" />
<img width="947" height="521" alt="Screenshot 2026-01-08 074145" src="https://github.com/user-attachments/assets/09431816-2ee0-43fe-b3f3-614aa34baec7" />

8️⃣ Defect Localization and Severity Assessment
## Defect Localization and Severity Assessment
For each detected defect:
- Center pixel coordinates (x, y) were calculated
- Severity was estimated based on bounding box area:
  - Low
  - Medium
  - High
    
 9️⃣Conclusion
## Conclusion
This project demonstrates an **Automated Quality Inspection System for Manufacturing**
using YOLOv8 and a Pascal VOC dataset.
The system successfully detects PCB defects and can help manufacturers
improve quality control while reducing manual inspection.

🔟 Tools and Technologies
## Tools and Technologies
- Python
- YOLOv8 (Ultralytics)
- Google Colab
- OpenCV
- Pascal VOC Dataset

PCB-Defect-Detection/
│
├── README.md
├── data.yaml
│
├── images/
│   ├── training_logs.png        ← (Colab training screenshot)
│   ├── results.png              ← (YOLO training graph)
│   ├── inference_result.png     ← (YOLO output image with boxes)
│
├── notebook.ipynb               ← (Colab notebook)
└── pcb_yolo_dataset/
    ├── images/
    └── labels/















