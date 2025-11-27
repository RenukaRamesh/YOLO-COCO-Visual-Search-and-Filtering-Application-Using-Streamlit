# YOLO COCO Visual Search Application (Streamlit)

## 1. Project Title

**YOLO-COCO Visual Search and Filtering Application Using Streamlit**

## 2. Introduction

This project provides a complete visual search engine built using a YOLOv11 model trained on the COCO dataset. Through a Streamlit-based interface, users can:

* Run object detection on folders of images
* Auto-generate metadata (classes, bounding boxes, counts)
* Load metadata without rerunning inference
* Search images by class filters (OR / AND)
* Apply count-based constraints
* Display results in a clean, responsive image grid
* Export filtered results as JSON

The entire system works on **CPU**, making it lightweight and easy to deploy.

## 3. Dataset & YOLO Model Details

### COCO Dataset

* 80 object classes
* 118k+ training images
* 5k validation images
* Included demo subset: **coco-val-2017-500**

### YOLO Model

* Model used: **YOLOv11m.pt**
* Pretrained on **COCO 2017**
* Supports 80 classes
* CPU compatible

## 4. Environment Setup

Install all dependencies:

```
pip install -r requirements.txt
```

Required packages include:

* streamlit
* ultralytics
* pillow
* pyyaml

## 5. CPU-Only Execution

The model automatically runs on CPU. Ensure this is set in `src/inference.py`:

```
device='cpu'
```

No CUDA or GPU setup required.

## 6. Running in VS Code (Conda Recommended)

Create and activate environment:

```
conda create -n yolosearch python=3.10 -y
conda activate yolosearch
pip install -r requirements.txt
```

Run the app:

```
streamlit run app.py
```

Optional (custom port):

```
streamlit run app.py --server.port 8080
```

## 7. Deployment (Streamlit Cloud)

1. Push repo to GitHub
2. Go to Streamlit Cloud
3. Link repo
4. Set entry point as `app.py`

Runs fully on CPU on the cloud.

## 8. Output Sections to Add Screenshots

Below placeholders will help you add screenshots later.

### **a. VS Code Terminal Output**

(Add screenshot under this section)

### **b. Web UI – Metadata Load & Search Page**

(Add screenshot here)

### **c. Object Detection Results (Grid View)**

(Add screenshot here)

### **d. JSON Export / Search Filters Section**

(Add screenshot here)

## 9. Enhancements Included

* Full metadata extraction
* Advanced search engine (OR / AND logic)
* Count-based filters
* Optimized responsive grid
* Highlighting matched classes
* Session-state based UI persistence

## 10. Conclusion

This project demonstrates how to build an efficient visual search system using YOLOv11 and Streamlit. The metadata-driven search allows fast filtering without rerunning inference. The system can be expanded for:

* Custom YOLO models
* Recommendation systems
* Large-scale retrieval engines
* Visual indexing pipelines

This architecture keeps the workflow simple, CPU-friendly, and highly extendable.
