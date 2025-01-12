# Advanced Neural Network Models for 3D Lane Prediction and Object Detection  

## Overview  
This project explores neural network-based solutions for key challenges in autonomous driving:
- **Lane Topology Prediction**
- **Object Detection**
- **3D Centerline Prediction**

<img src="https://as1.ftcdn.net/v2/jpg/09/18/55/70/1000_F_918557045_d9MFziMNRUbe3tuCzJ8uZQEM3hzIWM5K.jpg" alt="Sample Image" style="width:100%; height:auto;">

Leveraging datasets like **OpenLaneV2**, the project implements and evaluates models including CNNs, YOLO, and Vision Transformers to enhance the understanding of lane networks and improve object detection capabilities.

---

## Research Goals
**Lane Topology Prediction:**

Predict adjacency between lane segments in road networks.
Train and compare models like MLPs, CNNs, and Graph Neural Networks (optional).

**Object Detection on Merged Views:**

Merge camera views into front and rear perspectives.
Train object detection models (e.g., YOLO) to identify objects in these views.

**3D Centerline Prediction:**

Use advanced CNN and Vision Transformer models to predict 3D centerline points from images.
Evaluate predictions with metrics like Frechet Distance and Chamfer Distance.

**3D Positional Encoding:**

Assign unique 3D coordinates to detected objects around a vehicle to create spatial awareness.

---

## Objectives  
### **Research Assignments**
#### **Assignment 1: Lane-Lane Topology Prediction**
- **Goal:** Predict adjacency between lane segments in a road network.  
- **Approach:**  
  - Input: 3D centerline points for each lane segment.  
  - Ground Truth: Lane-lane adjacency matrix.  
  - Models:  
    - MLP (Feed-Forward Network) or CNN.  
    - Optional: Graph Neural Networks for enhanced performance.  
  - Evaluation: Binary classification for lane adjacency.

#### **Assignment 2: Object Detection on Merged Views**
- **Goal:** Detect objects in merged front and rear views of images.  
- **Tasks:**  
  - Merge frames into **front views** and **rear views** using multiple camera angles.  
  - Train or fine-tune a **CNN (e.g., YOLO)** for object detection.  
  - Bonus:  
    - Remove artifacts using camera parameters and feature maps.  
    - Create a **360° Annular Panoramic View**.  

#### **Assignment 3: 3D Centerline Prediction**
- **Goal:** Predict 3D centerline points from input images and annotations.  
- **Approach:**  
  - Models: Pre-trained **VGG-16** and **ResNet-50**, modified for regression.  
  - Metrics:  
    - **Mean Squared Error (MSE)** for loss.  
    - **Frechet Distance** and **Chamfer Distance** for evaluation.  
  - Dataset: Subset of **OpenLaneV2**.  

---

### **Final Research Project**
#### **Milestone 1: Positional Encoding for Object Detection**  
- **Goal:** Implement a 3D space around the ego center of the vehicle to uniquely encode all detected objects.  
- **Example:** Assign unique coordinates to bounding boxes relative to the vehicle's position at the origin `(0,0,0)`.

#### **Milestone 2: Vision Transformer for 3D Centerline Prediction**  
- **Goal:** Use a Vision Transformer model to predict 3D centerline points.  
- **Evaluation:**  
  - Metrics: Frechet Distance, Chamfer Distance.  
  - Visualize the projected points on input images.  

---

## Dataset  
The project uses the **OpenLaneV2** dataset for lane annotations, object detection, and 3D centerline prediction.  
- **Download Links:**  
  - [OpenLaneV2 Dataset Documentation](https://github.com/OpenDriveLab/OpenLane-V2/blob/master/data/README.md#download)  
  - [Sample Dataset for Centerline Tutorial](https://drive.google.com/file/d/1Ni-L6u1MGKJRAfUXm39PdBIxdk_ntdc6/view)  
  - [SubsetA Image Dataset](https://drive.google.com/file/d/1jio4Gj3dNlXmSzebO6D7Uy5oz4EaTNTq/view)  

---
## Project Workflow
**Step 1: Data Preprocessing**
Merge and preprocess image frames to create combined views.
Extract 3D centerline points and annotations for training and evaluation.

**Step 2: Model Training**
Lane-Lane Topology Prediction: Train MLP, CNN, and optionally Graph Neural Networks.
Object Detection: Fine-tune YOLO or custom CNNs on merged views.
3D Centerline Prediction: Train pre-trained CNNs or Vision Transformers.

**Step 3: Evaluation**
Evaluate models using:
Binary classification metrics for topology prediction.
Detection accuracy for object detection.
Frechet Distance and Chamfer Distance for 3D centerline predictions.

**Step 4: Visualization**
Visualize lane annotations, detected objects, and 3D centerlines on input images.

---

## Results  
- **Topology Prediction:**  
  - MLP and CNN models achieved reasonable accuracy in predicting adjacency between lane segments.  
  - Graph Neural Networks (optional) demonstrated better performance in capturing complex road networks.  
- **Object Detection:**  
  - Merged front and rear views successfully trained object detection models with YOLO.  
  - Bonus tasks enhanced the quality of visualizations and panoramic views.  
- **3D Centerline Prediction:**  
  - Vision Transformers outperformed traditional CNN-based regression models in predicting 3D centerline points.  
  - Evaluation metrics (Frechet Distance and Chamfer Distance) highlighted the precision of predictions.  

---

## Acknowledgments
Special thanks to Professor Dino Konstantopoulos and the teaching team of INFO6106 Neural Networks for their support and guidance.
