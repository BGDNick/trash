# Our models to detect plastic and papar on the conveyer belt
## 1. Creating the dataset
### 1.1 Problem
We neeed to create a system for automatic detection of different types of waste on the conveyor belt. There are types of debris to be sorted from the belt and which must continue on their way. The model is required to detect the presence of trash on the conveyor belt, then classify each object individually and decide whether to discard the object or not. To simplify the task, we will classify only plastic and paper.
### 1.2 Labeling own photo 
Using computer vision annotation [tool](https://app.cvat.ai/tasks?page=1) 345 photos were labeled

<img src = "https://github.com/BGDNick/trash/blob/main/labeled_photo.png" width="800" height="800" />
                    
## 2. YOLO8
The [notebook](https://github.com/BGDNick/trash/blob/main/Yolo8_Detector.ipynb) describes the procedure for training and validation

Here you can see the results:

<img src = "https://github.com/BGDNick/trash/blob/main/YOLO8_losses.png" width="800" height="300" />

<img src = "https://github.com/BGDNick/trash/blob/main/YOLO8_detection.png" width="800" height="800" />

## 3. Detection Transformer by Facebook
The [notebook](https://github.com/BGDNick/trash/blob/main/DETR_and_YoloNAS_Detector.ipynb) describes the procedure for training and validation

Here you can see the results:

<img src = "https://github.com/BGDNick/trash/blob/main/DETR_detection.png" width="800" height="800" />

## 4. YOLO NAS
The [notebook](https://github.com/BGDNick/trash/blob/main/DETR_and_YoloNAS_Detector.ipynb) describes the procedure for training and validation

Here you can see the results:

<img src = "https://github.com/BGDNick/trash/blob/main/YOLO_NAS_detection.png" width="800" height="800" />

## 5. Results and conclusion

Model | Time in ms | mAP50 | mAP50-95 
--- | --- | --- | --- 
YOLO8 | 50 | 0.98 | 0.85 
DETR | 250 | 0.84 | 0.82
YOLO NAS | 1170 | 0.89 | Nan

In our work, we found that YOLO8 is better suited for our task and showed better results in speed in quality


