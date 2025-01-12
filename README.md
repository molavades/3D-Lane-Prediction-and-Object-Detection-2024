# Advanced Neural Network Models for 3D Lane Prediction and Object Detection  

## Overview  
This project explores neural network-based solutions for key challenges in autonomous driving:
- **Lane Topology Prediction**
- **Object Detection**
- **3D Centerline Prediction**

Leveraging datasets like **OpenLaneV2**, the project implements and evaluates models including CNNs, YOLO, and Vision Transformers to enhance the understanding of lane networks and improve object detection capabilities.

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

## Project Structure  
