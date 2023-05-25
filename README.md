# Automatic Detection of Plastic and Paper on Conveyor Belt
The repository contains models for automatic detection and classification of plastic and paper waste on a conveyor belt. The goal is to develop a systemthat can identify different types of derbis on the belt and make decisions on whether to discard each object. The models included in this repository are YOLOv8n, Detection Transformer by Facebook and YOLO NAS.

## Table of Contents
1. [Creating the Dataset](#creating-the-dataset)
2. [YOLOv8n](#yolo8)
3. [Detection Transformer by Facebook](#detection-transformer-by-facebook)
4. [YOLO NAS](#yolo-nas)
5. [Results and Conclusion](#results-and-conclusion)


## 1. Creating the dataset <a name="#creating-the-dataset"></a>
### 1.1 Problem 
The objective is to create a system for the automatic detection of various types of waste on a conveyor belt. The system needs to identify the presence of trash, classify each object individually, and make informed decisions on whether to discard the object or not. For simplicity, the classification task focuses on plastic and paper waste.
### 1.2 Labeling own photo 

We labeled 345 photos using a computer vision annotation [tool](https://app.cvat.ai/tasks?page=1). The annotated photos are representative of the waste objects we aim to detect. 

<img src = "https://github.com/BGDNick/trash/blob/main/labeled_photo.png" width="800" height="800" />
                    
## 2. YOLOv8n <a name="#yolo8"></a>
The [notebook](https://github.com/BGDNick/trash/blob/main/Yolo8_Detector.ipynb) describes the procedure for training and validation

Here you can see the results:

<img src = "https://github.com/BGDNick/trash/blob/main/YOLO8_losses.png" width="800" height="300" />

<img src = "https://github.com/BGDNick/trash/blob/main/YOLO8_detection.png" width="800" height="800" />

## 3. Detection Transformer by Facebook <a name="#detection-transformer-by-facebook"></a>
The [notebook](https://github.com/BGDNick/trash/blob/main/DETR_and_YoloNAS_Detectors.ipynb) describes the procedure for training and validation

Here you can see the results:

<img src = "https://github.com/BGDNick/trash/blob/main/DETR_detection.png" width="800" height="800" />

## 4. YOLO NAS <a name="#yolo-nas"></a>
The [notebook](https://github.com/BGDNick/trash/blob/main/DETR_and_YoloNAS_Detectors.ipynb) describes the procedure for training and validation

Here you can see the results:

<img src = "https://github.com/BGDNick/trash/blob/main/YOLO_NAS_detection.png" width="800" height="800" />

## 5. Results and conclusion <a name="#results-and-conclusion"></a>

Model | Time in ms | mAP50 | mAP50-95 
--- | --- | --- | --- 
YOLOv8n | 50 | 0.98 | 0.85 
DETR | 250 | 0.84 | 0.82
YOLO NAS | 1170 | 0.89 | 0.71

Based on our work, we found that YOLOv8n is better suited for this task, as it demonstrated faster processing times and higher quality results.


