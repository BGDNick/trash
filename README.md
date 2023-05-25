# Our models to detect plastic and papar on the conveyer belt
## 1. Creating the dataset
### 1.1 Problem
We neeed to create a system for automatic detection of different types of waste on the conveyor belt. There are types of debris to be sorted from the belt and which must continue on their way. The model is required to detect the presence of trash on the conveyor belt, then classify each object individually and decide whether to discard the object or not. To simplify the task, we will classify only plastic and paper.
### 1.2 Labeling own photo 
Using computer vision annotation [tool](https://app.cvat.ai/tasks?page=1) 345 photos were labeled

<img src = "https://github.com/BGDNick/trash/main/labeled_photo.png" width="300" height="300" />


                           
## 2. YOLO8
The [notebook](https://github.com/BGDNick/trash/main/Yolo8_Detector.ipynb) describes the procedure for training and validation

Here you can see the results:

<img src = "https://github.com/BGDNick/trash/main/YOLO8_losses.png" width="800" height="300" />

<img src = "https://github.com/BGDNick/trash/main/YOLO8_detection.png" width="300" height="300" />

## 3. Detection Transformer by Facebook

## 4. YOLO NAS
