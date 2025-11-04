# 🐱 Cat Skin Disease Detection with YOLOv11 (TensorFlow Lite for Android)

> **Optimized for mobile inference on Android devices using TensorFlow Lite + GPU Delegate**  
> Built for real-time, offline detection of feline skin conditions — no cloud required.

---

## 📚 Dataset

Trained and evaluated using the **Cat Skin Disease** dataset from Roboflow:  
🔗 [https://universe.roboflow.com/your-workspace/cat-skin-disease](https://universe.roboflow.com/your-workspace/cat-skin-disease)

- **1,872 images** across 5 classes:  
  `Flea Allergy Dermatitis`, `Miliary Dermatitis`, `Feline Acne`, `Ringworm`, `Hot Spots`  
- **Split**: 80% train / 10% val / 10% test  
- **Resolution**: 640×640  
- **Augmentations**: Random brightness, contrast, rotation, flip, blur

---

## 🧠 Model Training

- **Framework**: YOLOv11 (Ultralytics)  
- **Hardware**: NVIDIA RTX 3090  
- **Epochs**: 150 | **Batch**: 16 | **Image Size**: 640×640  
- **Optimizer**: AdamW | **LR**: 0.001 (cosine decay)

### Training Command
```bash
yolo train model=yolov11n.pt data=cat-skin-disease.yaml epochs=150 imgsz=640 batch=16 optimizer=AdamW lr0=0.001
