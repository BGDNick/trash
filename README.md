# Our models to detect plastic and papar on the conveyer belt
## 1. Creating the dataset
### 1.1 Problem
We neeed to create a system for automatic detection of different types of waste on the conveyor belt. There are types of debris to be sorted from the belt and which must continue on their way. The model is required to detect the presence of trash on the conveyor belt, then classify each object individually and decide whether to discard the object or not. To simplify the task, we will classify only plastic and paper.
### 1.2 Labeling own photo 
Using computer vision annotation [tool](https://app.cvat.ai/tasks?page=1) 300 photos were labeled

<img src = "https://github.com/Anilian/my_education/blob/main/YOLO/cvat_label.png" width="300" height="300" />


                           
## 2. YOLO8
The [notebook](https://github.com/Anilian/my_education/blob/main/YOLO/train_yolov8.ipynb) describes the procedure for training and validation
Additional training files [yolov8x-seg_custom.yaml](https://github.com/Anilian/my_education/blob/main/YOLO/yolov8x-seg_custom.yaml),[custom_data.yaml](https://github.com/Anilian/my_education/blob/main/YOLO/custom_data%20(1).yaml)

Using a step-by-step guide we trained the model on 50 epochs. It took about 25 minutes and obtained the following metrics.

<img src = "https://github.com/Anilian/my_education/blob/main/YOLO/results.png" width="800" height="300" />

The predictions on the test sample showed excellent results

<img src = "https://github.com/Anilian/my_education/blob/main/YOLO/228.jpg" width="300" height="300" />

## 3. Detection Transformer by Facebook

## 4. YOLO NAS
