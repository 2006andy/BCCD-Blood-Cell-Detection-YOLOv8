
# BCCD Blood Cell Detection based on YOLOv8
> 基于YOLOv8的血涂片血细胞检测与计数项目

## Project Background
Manual blood cell counting under microscope is time-consuming and has subjective bias in clinical laboratory. This project uses YOLOv8 object detection model to identify and count Platelets, Red Blood Cells (RBC) and White Blood Cells (WBC) from blood smear images, exploring the application of computer vision in medical laboratory testing.

## Dataset
BCCD (Blood Cell Count and Detection) public blood smear dataset
- Training set: 291 images
- Validation set: 73 images
- Categories: Platelets, RBC, WBC

## Environment
- Python 3.10
- Ultralytics YOLOv8
- ONNX Runtime
- OpenCV

## Experiment Setting
- Backbone: YOLOv8n (nano lightweight model)
- Epochs: 50
- Image size: 640×640

## Result
| Metric | Value |
| ---- | ---- |
| mAP50 (Overall) | 0.931 |
| mAP50 (WBC) | 0.986 |
| mAP50 (RBC) | 0.904 |
| mAP50 (Platelets) | 0.904 |
CPU inference speed: ~27ms per image (PyTorch), ~35ms per image (ONNX Runtime)

## Pipeline
1. Dataset preparation & yaml configuration
2. YOLOv8 model training and validation
3. Visual prediction on blood smear images
4. Export PyTorch `.pt` model to ONNX format
5. ONNX Runtime cross-framework inference test

## Visualization
Training loss & metric curve, confusion matrix, detection samples are stored in `images/` folder.

## Limitation & Future Work
Limitation: BCCD is a small public dataset. Dense overlapping red blood cells easily cause missed detection. Image staining and shooting conditions are relatively single.
Future work: Add attention mechanism, use real clinical hospital blood smear data, build simple GUI for easy use.

## Commands
All running commands are saved in logs/run_commands.txt
