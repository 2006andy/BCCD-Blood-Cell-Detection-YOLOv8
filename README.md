# Blood Cell Microscopic Image Detection System | YOLOv8 + Gradio Web Deployment
> Interdisciplinary Project: Medical Laboratory Morphology + Computer Vision
> An auxiliary screening and automatic counting system for blood smear images

## 📌 Background
Manual microscopic examination of blood smears is time-consuming, repetitive, and susceptible to subjective variation. This project develops a lightweight AI-assisted detection system based on object detection. It can localize, classify and automatically count red blood cells, white blood cells and platelets, exploring the practical value of computer vision in preliminary hematological screening.

## ⚙️ Workflow
1. Dataset Preprocessing: Convert annotation format, split train/validation sets and clean data to meet YOLO format requirements
2. Model Training & Tuning: Train YOLOv8n lightweight detector, evaluate model performance, export weights to ONNX for cross-platform lightweight inference
3. Web Application Development: Build an interactive inference interface with Gradio. The system runs locally and can be accessed directly via browser
4. Inference Output: Upload blood smear micrographs. The model outputs bounding boxes, cell categories and statistical count table automatically

## ✨ Features
- Multi-class detection: Identify WBC, RBC and platelets simultaneously
- Lightweight deployment support: ONNX export for future edge-device deployment
- User-friendly web interface: One-click upload and inference with visualized results
- Fully reproducible pipeline: Open-source codes covering data processing, training, evaluation and web inference

## 📷 Demo Screenshot
![Demo Interface](./demo.png)

## 🛠 Environment
```bash
pip install ultralytics gradio pandas opencv-python
