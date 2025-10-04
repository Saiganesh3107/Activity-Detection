# 🎥 Activity Detection Project  

![Python](https://img.shields.io/badge/Python-3.7%2B-blue)  
![YOLO](https://img.shields.io/badge/YOLOv8-Object%20Detection-green)  
![Status](https://img.shields.io/badge/Status-Active-brightgreen)  
![License](https://img.shields.io/badge/License-MIT-orange)  

A **video-based activity detection system** that uses **YOLOv8** and action classification logic to detect and summarize human activities from videos.  
The system identifies actions like *cycling, eating, using a laptop, calling,* etc., and generates an **annotated summary video**.  

---

## 📑 Table of Contents  

1. Overview  
2. Features  
3. Project Structure  
4. Requirements & Setup  
5. Usage  
6. How it Works  
7. Output / Examples  
8. Tips & Troubleshooting  
9. Future Improvements  
10. License & Acknowledgements  

---

## 🧠 Overview  

This project performs **activity detection** on input videos by combining:  

- **YOLOv8** for person/object detection  
- **Custom logic / classification** for human activity recognition  
- **Video summarization** to highlight detected actions  

It can run in **real-time** (webcam/stream) or on pre-recorded videos.  

---

## ✅ Features  

- Detects & classifies multiple human activities in videos  
- Supports offline video processing (MP4 files included)  
- Saves summarized annotated output videos  
- Modular design → swap models / extend activity classes  
- Lightweight YOLOv8 models for faster inference  

---

## 📁 Project Structure  

```
/
├── calling - 1.mp4
├── cycling.mp4
├── eating.mp4
├── laughing and dancing and drinking.mp4
├── using_laptop.mp4
├── yolov8n.pt              # YOLOv8 pretrained weights
├── nano_best_1.pt          # Fine-tuned weights
├── project - 2 (2).ipynb   # Main notebook (detection + summarization)
└── README.md               # Documentation
```  

---

## 🛠 Requirements & Setup  

### Prerequisites  
- Python 3.7+  
- Jupyter Notebook (or Colab)  
- GPU (CUDA) optional but recommended  

### Install dependencies  

```
pip install opencv-python-headless
pip install ultralytics
pip install numpy
pip install matplotlib
pip install torch torchvision
```

### Clone the Repository  

```
git clone https://github.com/Saiganesh3107/Activity-Detection.git
cd Activity-Detection
```

---

## 🎬 Usage  

### Option 1: Run via Notebook  

1. Open `project - 2 (2).ipynb`  
2. Run cells in order:  
   - Load libraries & models  
   - Set input video path  
   - Run detection + summarization  
   - Save / view results  

### Option 2: (If converted to script)  

```
python detect_activity.py --input cycling.mp4 --output summary.mp4
```

---

## 🧩 How it Works  

1. **Frame Extraction** → Read video frame by frame  
2. **YOLOv8 Detection** → Detect humans & relevant objects  
3. **Activity Classification** → Map detected actions (e.g. *cycling, using laptop*)  
4. **Temporal Smoothing** → Avoid flickering predictions across frames  
5. **Summarization** → Merge detected segments → output summary video  

---

## 🎯 Output / Examples  

Sample inputs & outputs:  

- `cycling.mp4` → Detected *Cycling*  
- `using_laptop.mp4` → Detected *Using Laptop*  
- `calling - 1.mp4` → Detected *Calling*  

📌 Output: Annotated video with bounding boxes + labels for detected activities  

---

## 🚧 Future Improvements  

- Add more activities (e.g., sports actions, office tasks)  
- Use advanced action recognition models (3D CNNs, transformers)  
- Add **pose estimation** for fine-grained recognition (e.g., OpenPose, Mediapipe)  
- Support **live webcam / CCTV feeds**  
- Web-based interface for easy upload & results viewing  

---

## 📜 License & Acknowledgements  

- **License:** MIT (open-source, free to modify)  
- **Credits:**  
  - Ultralytics YOLOv8  
  - OpenCV, PyTorch, Numpy, Matplotlib  

---
 
